
<!-- .slide: data-background-image="./assets/md/assets/kitchen-sink.jpg" data-background-size="100% 100%" data-background-position="center" data-background=" " data-background-repeat=" " data-background-transition="none" -->

<span class="menu-title" style="display: none">Introduction</span>

<div class="north headline span-80">
<span class="heading">The Kitchen Sink</span>
</div>

<div class="south byline">
A <span style="color: #e49436">Git</span>Pitch Feature Tour
</div>

---
<span class="menu-title" style="display: none">Theme Switcher</span>

### Slideshow Theme Switcher
<span class="help"><i class="fa fa-arrow-left" aria-hidden="true"> </i> The theme switcher is found inside the burger-menu.</span>

<div class="north-west span-25">
![Image](./assets/md/assets/theme-1.jpg)
</div>

<div class="north span-25">
![Image](./assets/md/assets/theme-2.jpg)
</div>

<div class="north-east span-25">
![Image](./assets/md/assets/theme-3.jpg)
</div>

<div class="south-west span-25">
![Image](./assets/md/assets/theme-4.jpg)
</div>

<div class="south span-25">
![Image](./assets/md/assets/theme-5.jpg)
</div>

<div class="south-east span-25">
![Image](./assets/md/assets/theme-6.jpg)
</div>

---
<!-- .slide: data-background="white" -->

<span class="menu-title" style="display: none">Go Fullscreen</span>

![Image](./assets/md/assets/fullscreen.png)
<br><br>
For the *best viewing experience*<br>press the **F** key to go fullscreen.

---

## Markdown Slides
<span class="tip">Press the Space or Down key for more details.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Markdown Docs](https://gitpitch.com/docs/markdown-features) for further details.
</div>

+++
<span class="menu-title" style="display: none">GFM</span>

#### Use GitHub Flavored Markdown
#### For Slide Content Creation

<br>

The *same syntax* you use to create project   
**READMEs** and **Wikis** for your Git repos.

---
<span class="menu-title" style="display: none">Inline Images</span>

## Image Slides
## [ Inline ]
<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Inline Image Docs](https://gitpitch.com/docs/image-features/inline) for further details.
</div>

+++
<span class="menu-title" style="display: none">Visual Statement</span>

#### Make A Visual Statement

<br>

Add *visual punch* to any slide<br>using inline images to tell your story.

+++
<span class="menu-title" style="display: none">Relative URLs</span>

<span class="tip">Inline Image at Git Repo <b>Relative URL</b></span>
<br>
![Image](./assets/md/assets/octocat-de-los-muertos.jpg)
<br>
<span class="help">the <b>Octocat-De-Los-Muertos</b> by [cameronmcefee](https://github.com/cameronmcefee</span>)

+++
<span class="menu-title" style="display: none">Absolute URLs</span>

<div class="west span-50">
<span class="tip">Inline Image at <b>Absolute URL</b></span>
<br>
![Image](./assets/md/assets/octocat-privateinvestocat.jpg)
<br>
<span class="help">the <b>Private Investocat</b> by [jeejkang](https://github.com/jeejkang</span>)
</div>

<div class="east span-50 fragment">
<span class="tip"><b>Animated GIFs</b> Work Too!</span>
<br>
![Image](./assets/md/assets/octocat-daftpunkocat.gif)
<br>
<span class="help">the <b>Daftpunktocat-Guy</b> by [jeejkang](https://github.com/jeejkang</span>)
</div>

---
<span class="menu-title" style="display: none">Background Images</span>

## Image Slides
## [ Background ]

<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Background Image Docs](https://gitpitch.com/docs/image-features/background) for further details.
</div>

+++
<span class="menu-title" style="display: none">Bold Statements</span>

#### Make A Bold Visual Statement

<br>

Use *size-optimized* background images<br>for *best Web viewing experience*.

+++
<!-- .slide: data-background-image="./assets/md/assets/robot.jpg" data-background-size="100% 100%" data-background-position="center" data-background=" " data-background-repeat=" " data-background-transition="none" -->

<span class="menu-title" style="display: none">Future Human</span>

+++
<!-- .slide: data-background-image="./assets/md/assets/127.jpg" data-background-size="100% 100%" data-background-position="center" data-background=" " data-background-repeat=" " data-background-transition="none" -->

<span class="menu-title" style="display: none">127.0.0.1</span>

+++
<!-- .slide: data-background-image="./assets/md/assets/supercar.jpg" data-background-size="100% 100%" data-background-position="center" data-background=" " data-state="bg-img-opacity-40" data-background-repeat=" " data-background-transition="none" -->

<span class="menu-title" style="display: none">Aesthetics</span>

<div class="north-west">
<span style="font-size: 2.5em">Beautiful?</span>
</div>

<div class="south aesthetics span-100">
It all comes down to the observer and aesthetics.
</div>

---

## Code Presenting
## Repo Source Files
<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Code Presenting Docs](https://gitpitch.com/docs/code-features) for further details.
</div>

+++

<span class='menu-title slide-title'>Source: Golang File</span>
```golang
package funding

type FundServer struct {
    Commands chan interface{}
    fund Fund
}

func NewFundServer(initialBalance int) *FundServer {
    server := &FundServer{
        // make() creates builtins like channels
        Commands: make(chan interface{}),
        fund: NewFund(initialBalance),
    }

    // Spawn off the server's main loop immediately
    go server.loop()
    return server
}

func (s *FundServer) loop() {
    // The built-in "range" clause can iterate
    // over channels, amongst other things
    for command := range s.Commands {
    
        // Handle the command
        
    }
}


```


<span class="code-presenting-annotation fragment current-only" data-code-focus="1,3-6">Present code found within any repo source file.</span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="8-18">Without ever leaving your slideshow.</span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="19-28">Using GitPitch code-presenting with (optional) annotations.</span>

---
<span class="menu-title" style="display: none">Present Static Block</span>

## Code Presenting
## Static Source Blocks
<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Code Presenting Docs](https://gitpitch.com/docs/code-features) for further details.
</div>

+++
<span class="menu-title slide-title">Source: JavaScript Block</span>

```javascript
// Include http module.
var http = require("http");

// Create the server. Function passed as parameter
// is called on every request made.
http.createServer(function (request, response) {
  // Attach listener on end event.  This event is
  // called when client sent, awaiting response.
  request.on("end", function () {
    // Write headers to the response.
    // HTTP 200 status, Content-Type text/plain.
    response.writeHead(200, {
      'Content-Type': 'text/plain'
    });
    // Send data and end response.
    response.end('Hello HTTP!');
  });

// Listen on the 8080 port.
}).listen(8080);
```

<span class="code-presenting-annotation fragment current-only" data-code-focus="1,2">You can present code inlined within your slide markdown too.</span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="9-17">Displayed using code-syntax highlighting just like your IDE.</span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="19-20">Again, all of this without ever leaving your slideshow.</span>

---
<span class="menu-title" style="display: none">Present GIST</span>

## Code Presenting
## GitHub GIST
<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Code Presenting Docs](https://gitpitch.com/docs/code-features) for further details.
</div>

+++

<span class='menu-title slide-title'>Source: Scala GIST</span>
```Scala
package io.onetapbeyond.lambda.spark.executor.examples

import io.onetapbeyond.lambda.spark.executor.Gateway._
import io.onetapbeyond.aws.gateway.executor._
import org.apache.spark._
import scala.collection.JavaConverters._

/*
 * TaskDelegation
 *
 * https://github.com/onetapbeyond/lambda-spark-executor
 *
 * A sample application that demonstrates the basic usage
 * of SAMBA to delegate selected Spark RDD tasks to execute
 * on AWS Lambda compute infrastructure in the cloud.
 */
object TaskDelegation {

  def main(args:Array[String]):Unit = {

    try {

      val sc = initSparkContext()

      /*
       * Initialize a basic batch data source for the
       * example by generating an RDD[Int].
       */
      val dataRDD = sc.parallelize(1 to BATCH_DATA_SIZE)

      /*
       * API_GATEWAY represents the API on the AWS API
       * Gateway implemented by an AWS Lambda function.
       * We register the gateway as a Spark broadcast
       * variable so it can be safely referenced later
       * within the Spark RDD.map operation that builds
       * our AWSTask.
       */
      val gateway = sc.broadcast(API_GATEWAY)

      /*
       * Map over dataRDD[Int] to produce an RDD[AWSTask].
       * Each AWSTask will execute an AWS Lambda function
       * exposed by the API_SCORE_ENDPOINT endpoint on the
       * AWS API Gateway.
       */
      val aTaskRDD = dataRDD.map(num => {

        AWS.Task(gateway.value)
           .resource(API_SCORE_ENDPOINT)
           .input(Map("num" -> num).asJava)
           .post()
      })

      aTaskRDD.foreach { aTask => println(aTask) }

      /*
       * Delegate aTaskRDD[AWSTask] execution to AWS Lambda
       * compute infrastructure to produce
       * aTaskResultRDD[AWSResult].
       */
      val aTaskResultRDD = aTaskRDD.delegate

      /*
       * As this is an example application we can simply use
       * the foreach() operation on the RDD to force the
       * computation and to output the results. And as we are
       * using a mock API on the AWS API Gateway there is no
       * response data, the result simply indicates success
       * or failure.
       */
      aTaskResultRDD.foreach { result => {
        println("TaskDelegation: compute score input=" +
          result.input + " result=" + result.success)
      }}

    } catch {
      case t:Throwable =>
        println("TaskDelegation: caught ex=" + t)
    }

  }

  def initSparkContext():SparkContext = {
    val conf = new SparkConf().setAppName(APP_NAME)
    new SparkContext(conf)
  }

  private val APP_NAME = "SAMBA Task Delegation Example"
  private val BATCH_DATA_SIZE = 10
  private val API_ID = "06ti6xmgg2"
  private val API_STAGE = "mock"
  private val API_SCORE_ENDPOINT = "/score"
  private val API_GATEWAY:AWSGateway =
    AWS.Gateway(API_ID).region(AWS.Region.OREGON)
                       .stage(API_STAGE)
                       .build()
}
```


<span class="code-presenting-annotation fragment current-only" data-code-focus="23">You can even present code found within any GitHub GIST.</span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="41-53">GIST source code is beautifully rendered on any slide.</span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="57-62">Code-presenting works seamlessly both online and offline.</span>

---
<span class="menu-title" style="display: none">Snap Layouts</span>

## Snap Layouts
<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Snap Layouts Docs](https://gitpitch.com/docs/layout-features) for further details.
</div>

+++
<span class="menu-title" style="display: none">Custom Placement</span>

#### Use Snap Layouts For Custom Placement<br>Of Slide Content On Any Slide

<br>

You can override the automatic slide layout<br>to bring your most creative ideas to life.

+++
<!-- .slide: data-background="#E6E8EC" -->

<span class="menu-title" style="display: none">Snap Layout Demo</span>

<div class="north-west">
<span style="font-size: 1.5em">GraphQL</span>
</div>

<div class="west graphql-details span-50">
GraphQL is a query language for APIs and a runtime for fulfilling those queries with your existing data. GraphQL provides a complete and understandable description of the data in your API, gives clients the power to ask for exactly what they need and nothing more, makes it easier to evolve APIs over time, and enables powerful developer tools.
</div>

<div class="east graphql-arch span-50">
![Image](./assets/md/assets/graphql.png)
</div>

+++
<!-- .slide: data-background="#E6E8EC" -->

<span class="menu-title" style="display: none">Snap Layout Demo</span>

<div class="north-east graphql-title span-50">
<span style="font-size: 1.5em">GraphQL</span>
</div>

<div class="east graphql-bullets span-50">
<ul class="">
<li class="   ">Query is a read-only operation</li>
<li class="   ">Mutation is a read-write operation</li>
<li class="   ">Resolver provides a mapping between a portion of a GraphQL operation and a backend handler</li>
<li class="   ">Schema defines what queries and mutations can be performed</li>
<li class="   ">Type defines the shape of response data that can be returned</li>
</ul>
</div>

<div class="west graphql-arch span-50">
![Image](./assets/md/assets/graphql.png)
</div>

---

## Markdown Fragments
<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Markdown Fragments Docs](https://gitpitch.com/docs/markdown-features/fragments) for further details.
</div>

+++

#### Reveal Slide Concepts Piecemeal
<span class="menu-title" style="display: none">Fragment Concepts</span>

<br>

Step through slide content in sequence   
to *slowly reveal* the bigger picture.

+++
<span class="menu-title" style="display: none">Mixed Content Fragments</span>

<div class="north-west">
JVM Polyglot Runtime
</div>

<div class="west">
<br>
<ul class=" ">
<li class="fragment  ">Java</li>
<li class="fragment  ">Groovy</li>
<li class="fragment  ">Kotlin</li>
<li class="fragment  ">Scala</li>
<li class="fragment  ">Clojure</li>
</ul>
</div>

<div class="east span-60 fragment">
![Image](./assets/md/assets/jvm.jpg)
</div>

+++
<span class="menu-title" style="display: none">Table Content Fragments</span>


<div class="north">
Table Data Fragments
</div>

<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>25</td>
  </tr>
  <tr class="fragment">
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
  <tr class="fragment">
    <td>John</td>
    <td>Doe</td>
    <td>43</td>
  </tr>
</table>

---

## Math Formulas Slides
<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Math Formulas Docs](https://gitpitch.com/docs/rich-media-features/math-formulas) for further details.
</div>

+++
<span class="menu-title" style="display: none">Beautiful Math</span>

#### Beautiful Math Rendered Beautifully

<br>

Use *TeX*, *LaTeX* and *MathML* markup   
powered by [MathJax](https://www.mathjax.org).

+++
<span class="menu-title" style="display: none">Sample</span>

`$$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$`

+++
<span class="menu-title" style="display: none">Sample</span>

`\begin{align}
\dot{x} & = \sigma(y-x) \\
\dot{y} & = \rho x - y - xz \\
\dot{z} & = -\beta z + xy
\end{align}`

+++
<span class="menu-title" style="display: none">Sample</span>

##### The Cauchy-Schwarz Inequality

`\[
\left( \sum_{k=1}^n a_k b_k \right)^{\!\!2} \leq
 \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
\]`

+++
<span class="menu-title" style="display: none">Inline Sample</span>

##### In-line Mathematics

This expression `\(\sqrt{3x-1}+(1+x)^2\)` is an example of an inline equation.

---

## Chart Slides
<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Charts Docs](https://gitpitch.com/docs/rich-media-features/charts) for further details.
</div>

+++
<span class="menu-title" style="display: none">Chart Types</span>

#### Chart Data Rendered Beautifully

<br>

Use *Bar*, *Line*, *Area*, and *Scatter* charts among many other chart types directly within your markdown, all powered by [Chart.js](http://www.chartjs.org).

+++
<span class="menu-title" style="display: none">Sample Line Chart</span>

<canvas data-chart="line">
<!--
{
 "data": {
  "labels": ["January"," February"," March"," April"," May"," June"," July"],
  "datasets": [
   {
    "data":[65,59,80,81,56,55,40],
    "label":"My first dataset","backgroundColor":"rgba(20,220,220,.8)"
   },
   {
    "data":[28,48,40,19,86,27,90],
    "label":"My second dataset","backgroundColor":"rgba(220,120,120,.8)"
   }
  ]
 },
 "options": { "responsive": "true" }
}
-->
</canvas>

+++
<span class="menu-title" style="display: none">Sample Bar Chart</span>

<canvas class="stretch" data-chart="horizontalBar">
<!--
{
 "data" : {
  "labels" : ["Grapefruit", "Orange", "Kiwi",
    "Blackberry", "Banana",
    "Blueberry"],
  "datasets" : [{
    "data": [48, 26, 59, 39, 21, 74],
    "backgroundColor": "#e49436",
    "borderColor": "#e49436"
  }]
  },
  "options": {
    "title": {
      "display": true,
      "text": "The most delicious fruit?",
      "fontColor": "gray",
      "fontSize": 20
    },
    "legend": {
      "display": false
    },
    "scales": {
      "xAxes": [{
        "ticks": {
            "beginAtZero": true,
            "max": 80,
            "stepSize": 10,
            "fontColor": "gray"
        },
        "scaleLabel": {
          "display": true,
          "labelString": "Respondents",
          "fontColor": "gray"
        }
      }],
      "yAxes": [{
        "ticks": {
            "fontColor": "gray"
        }
      }]
    }
  }
}
-->
</canvas>

---
<span class="menu-title" style="display: none">Embed Video</span>
## Video Slides
## [ Inline ]
<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Inline Video Docs](https://gitpitch.com/docs/rich-media-features/inline-videos) for further details.
</div>

+++
<span class="menu-title" style="display: none">YouTube, etc</span>

#### Bring Your Presentations Alive

<br>

Embed *YouTube*, *Vimeo*, *MP4* and *WebM*   
inline on any slide.

+++
<span class="menu-title" style="display: none">Fresh Guacamole</span>

#### Video Disabled

+++
<span class="menu-title" style="display: none">Gravity</span>

#### Video Disabled

+++
<span class="menu-title" style="display: none">Big Buck Bunny</span>

#### Video Disabled

---
<span class="menu-title" style="display: none">Background Videos</span>

## Video Slides
## [ Background ]
<span class="tip">Press the Space or Down key for a live demo.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Background Video Docs](https://gitpitch.com/docs/rich-media-features/background-videos) for further details.
</div>

+++
<span class="menu-title" style="display: none">Viewer Experience</span>

#### Maximize The Viewer Experience

<br>

Go fullscreen with *MP4* and *WebM* videos.

+++

#### Video Disabled

<span class="menu-title" style="display: none">Big Buck Bunny</span>

---
## <span class="notransform">PITCHME.yaml</span> Settings
<span class="tip">Press the Space or Down key for more details.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-90">
See the [GitPitch Settings Docs](https://gitpitch.com/docs/settings) for further details.
</div>

+++
<!-- .slide: data-background-image="./assets/md/assets/brand.jpg" data-background-size="100% 100%" data-background-position="center" data-background=" " data-background-repeat=" " data-background-transition="none" -->

<span class="menu-title" style="display: none">Custom Look and Feel</span>

<div class="north brand span-100">
Stamp Your Own Brand On Any Slideshow
<br><br>
<span class="brand-options">Use settings to activate a fixed slideshow theme, set a custom logo, custom layout, custom css, default background image, even your preferred code highlighting style and more.</span>
</div>

---
<span class="menu-title" style="display: none">Keyboard Controls</span>
## Slideshow Keyboard Controls
<span class="tip">Press the Space or Down key for more details.</span>

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

<div class="south doclink span-80">
See the [GitPitch Keyboard Controls Docs](https://gitpitch.com/docs/foundation-features/keyboard-controls) for further details.
</div>

+++
<span class="menu-title" style="display: none">Try Out Now!</span>

#### Try Out These Keyboard Controls Now!

<br>

| Mode | On Key | Off Key |
| ---- | :------: | :--------: |
| Fullscreen | F |  Esc |
| Overview | O |  O |
| Blackout | B |  B |
| Speaker View | S |  - |
| Help | ? |  Esc |


---
<span class="menu-title" style="display: none">Get The Word Out!</span>

<div class="south help docslink span-90">
For more details, examples, tips, and tricks see the [GitPitch Docs](https://gitpitch.com/docs)
</div>

## GO FOR IT.
## JUST ADD <span style="color: #e49436"><span class="notransform">PITCHME.md</span></span> ;)