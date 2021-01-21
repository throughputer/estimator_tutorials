# Get your Estimator powered app running in 5 minutes
__Live Demo :__  __[click me!](https://estimatorlab.com/rps)__

### Prerequisite.

  - You must have your API key. Don't have one? Try playing with our demo apps on __[https://estimatorlab.com](https://estimatorlab.com/)__ to earn one.
  - Python3 installed. You can install it from https://www.python.org/downloads/

### Steps to get your app running

##### Step 1
Download or clone the repository

```sh
Download link
https://github.com/throughputer/estimator_tutorials/archive/main.zip
```
```sh
Clone command
$ git clone https://github.com/throughputer/estimator_tutorials.git
```
##### Step 2
change directory
```sh
$ cd rock-paper-scissor
```
##### Step 3
open the file ``` js/rps.js``` using any editor
```sh
$ vim js/rps.js
```

##### Step 4 
go the line number 90
```sh
 To utilize your access to a ThroughPuter Estimator microservice, provide your API key here, HOWEVER...
 IMPORTANT!!! It is your responsibility to keep your API key secret. This code is visible in a user's web browser,
 and this demo is not intended to be hosted publicly with your private key.
```
```js
this.prediction = new Prediction(
      4,
      true,
      `wss://passgraf.com:2083/ws/<Insert-your secret-token>`,
      predictionCB,
      { onopen: wsReady, onclose: onclosefn, onerror: onerrorfn }
    );
```
##### Step 5
Replace ```<Insert-your-API-key> ``` (so that the < > marks get eliminated) with your API key. 
You can find your API key at __[https://estimatorlab.com/estimator](https://estimatorlab.com/estimator)__ 

```
Note: Always keep your API key secret. This demo app is NOT built to be hosted publicly. Generally, unlike this demo, only the back end of your web application should connect to your private Estimator microservice.
```

##### Step 6
Start a python3 http server (or any http server). You can install Python3 from __[here](https://www.python.org/downloads/)__ 
```py
For mac/linux based systems
python3 -m http.server
```
```py
For windows based systems
py -m http.server
```

You should see the following, showing that your http server is running on Port 8000:
```sh
Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...
```
##### Step 7
Open your favorite browser and enter the URL:
```sh
http://localhost:8000/
```

Confirm that you have connected successfully with your Estimator microservice instance by playing more than four moves of Rock-Paper-Scissors to see that the AI is making moves. (Only after the first four plays is the Estimator trained to make predictions.)

#### All done!

You can see a RPS app running with your API key. Check your __[Dashboard](https://estimatorlab.com/dashboard)__ to view the number of calls made to the estimator microservice & keep track of your free credits consumption.
```Note: The first 3 clicks are used to train the online Machine Learning engine  and not counted towards your usage.```

## What's next?

Now you can try your hand at writing your own application. The available Estimator APIs are [documented here](https://github.com/throughputer/estimator_lib/blob/master/EstimatorAPI.md).

**Questions?** [Contact Us](https://estimatorlab.com/form)
