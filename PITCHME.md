### Machine learning for monitoring data
#### Time series anomaly detection

---

## Hello


- Monitoring and Automation SW Dev Team @Cegeka:
    * Thomas Coomans
    * Stefan Bucur
    * Guang Wei
    * \+ many more that are not here
- We create software projects that enhance our monitoring tools
- Tripled the number of monitored devices => a need for AI/ML

Note:

Hello,
We are the the Software Development Team that is part of the
larger Monitoring and Automation Team in Cegeka.
In the last few years, the number of devices that we are monitoring
has almost tripled, and this fact brought with it a whole new set of challenges.
One of the solutions for these challenges is Machine Learning.

---

### Why is it this way?
![jupyter-1](assets/xkcd-tasks.png)


Note:

This comic is on to something.
To make a software solution, you can usually describe at a high level what steps are needed.
But sometimes you don't know the steps at all.
Consider the following examples:
* finding if a photo is in a park
* finding if a picture is a bird
---

Finding if a photo is in a park

```python
1. Upload the picture
2. Find the latitude and longitude from EXIF data
3. Take a map of that area
4. If it's the right shade of green => it's a park

```

---

<iframe height="600" style="width: 100%;" scrolling="no" title="WmxBWz" src="//codepen.io/slbucur/embed/WmxBWz/?height=265&theme-id=0&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/slbucur/pen/WmxBWz/'>WmxBWz</a> by Stefan-Lucian Bucur
  (<a href='https://codepen.io/slbucur'>@slbucur</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


Note:

We implemented the solution ourselves. It took more than I would like to admit,
but because we knew the high level steps, it was mostly straight-forward.
---

Find if a picture is a bird

```python
1. Find the edges of the image
2. Find the basic shapes in it
3. If it has 3 triangles, it is probably a bird

```

Note:

I don't know about you, but I'm not very confident this is the right solution.

---

![Image](assets/bird-canny.png)
![Image](assets/triforce.png)

Note:

The steps mentioned above will probably find __some__ birds, but it would give a lot
of false positives and likely a lot of false negatives as well.

We can improve the algorithm by decomposing the image into smaller, more specific objects and basing our identification on them.

But you can probably guess this would be time consuming, and probably not very accurate either.

What's the solution?

Ideally we would make an algorithm that automatically learns how to find birds in
pictures, by training it with some manually labeled pictures.
Instead of programming with algorithms, we could program with data.
And that's what **machine learning** is :).

---

## Machine learning 101

---

Two main categories of ML:
- Supervised learning
- Unsupervised learning

---

@snap[north]
### Supervised learning
@snapend

Labeled data **=>** Create model **=>** Predict labels for data without labels

Note:

---

@snap[north]
Example
@snapend

<table style='font-size: 0.7em'>
  <tr>
    <th> Name </th>
    <th> Age </th>
    <th> Gender </th>
    <th> Ticket class </th>
    <th> Cabin number </th>
    <th> Survived </th>
  </tr>
  <tr>
    <td> Bill Smith </td>
    <td> 49 </td>
    <td> M </td>
    <td> 3rd </td>
    <td> 32C </td>
    <td> <b> No </b> </td>
  </tr>
  <tr>
    <td> Mandy Floyd </td>
    <td> 24 </td>
    <td> F </td>
    <td> 1st </td>
    <td> 2B </td>
    <td> <b> Yes </b> </td>
  </tr>
  <tr>
    <td> Carmen Floyd </td>
    <td> 22 </td>
    <td> F </td>
    <td> 1st </td>
    <td> 2D </td>
    <td> <b> Yes </b> </td>
  </tr>
</table>

---

What is the probability that Jack or Rose survived?
<table style='font-size: 0.7em'>
  <tr>
    <th> Name </th>
    <th> Age </th>
    <th> Gender </th>
    <th> Ticket class </th>
    <th> Cabin number </th>
    <th> Survived </th>
  </tr>
  <tr>
    <td> Jack Dawson </td>
    <td> 20 </td>
    <td> M </td>
    <td> 3rd </td>
    <td> 38D </td>
    <td> ? </td>
  </tr>
  <tr>
    <td> Rose DeWitt Bukater </td>
    <td> 17 </td>
    <td> F </td>
    <td> 1st </td>
    <td> 1A </td>
    <td> ? </td>
  </tr>
</table>

---


Note:

By using the extremely limited data set from the previous slide,
and our intuition, we notice two things:
* women and young people have a high survival rate (women and children first)
* passengers with better cabins also have a higher survival rate

From this we can conclude that James Cameron is a good statistician.

---

## Unsupervised learning

Trying to learn patterns in data, without having labels:
* clustering
* outlier detection
* data generation

---

### K-means

<iframe height="600" style="width: 100%;" scrolling="no" title="WmxBWz" src="https://slbucur.me/kmeans/" frameborder="no" allowtransparency="true" allowfullscreen="true">
</iframe>

<a href="http://web.stanford.edu/class/ee103/visualizations/kmeans/kmeans.html"> direct link <a>

Note:

K-means is a classic example of unsupervised learning.
If tries to find clusters in a data set, based on the distance between data items.
In this visualization, you can see the algorithm in practice for 2 dimensional points.
Since the algorithm is based on distance, you can use with a wide range of data types.
For example, you can group sentences together, with the distance between them
being the number of words they have in common.

---

### Monitoring data

---

We have two types of data:
* performance data
* events

Today we'll focus on performance data.

---

### Monitoring performance data

* metric or time series data
  * tuples of `(label, timestamp, value)`
* analyzes performance of hardware and software used throughout the data center
* easily displayed using line graphs

---

![Image](assets/osiris-throughput.png)

Note:

Network throughput graph represented by:
* inbound traffic: dark blue
* outbound traffic: light blue

---

### Our first use case for ML

* monthly availability reports generated by the networking team
* manually analysis of a subset of the network graphs:
  * sudden spikes or dips that could mean:
    * security breaches - rarely
    * incorrect device level configuration - often

---

* the number of devices tripled in the last few years
* manual analysis -> time consuming and error prone
* our task -> ** automate the anomaly detection process **

---

### Our approach

* proof of concept (POC) using a statistical model
* starting point for more complex models in the future.

---

### State of the art


* statistical models - unsupervised learning
* deep learning (neural networks) - supervised learning

---


### Statistical models

* a model is defined for the data
* one or multiple functions that depend on time
* the functions depend on multiple parameters (except time)
* to find them => we __train__ or __fit__ the model with our current data


---

Pros:
* fast
* easy to understand

Cons:
* cannot model complex data sets

---


Examples:
* STL decomposition - Seasonal Trend decomposition using Loess
* ARIMA – Auto Regressive Integrated Moving Average
* ETS decomposition – Error, Trend, Seasonality

---

### Deep learning models

* loosely imitate the human brain
* multiple linear models
  * one for each neuron in the network

---


Pros:
* can simulate very complex models

Cons:
* very slow time to train => more useful when having multiple metrics as inputs



