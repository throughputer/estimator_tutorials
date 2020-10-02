# Get your Estimator powered app running in 5 minutes
__Live Demo :__  __[click me!](https://estimatorlab.com/rock_paper_scissors/index.html)__

### Prerequisite.

  - You must have your secret token. Don't have? Try playing with our demo apps on __[estimatorlab.com](https://estimatorlab.com/)__ to get one.
  - Python3 installed . You can install it from https://www.python.org/downloads/
  - Magic

### Steps to get your app running

##### Step 1
clone the repository
```sh
$ git clone https://github.com/throughputer/estimator_tutorials.git
```
##### Step 2
change directory
```sh
$ cd rock-paper-scissor
```
##### Step 3
open the file ``` js/rps.js``` using any editor.
```sh
$ vim js/rps.js
```

##### Step 4 
go the line number 75
```js
this.prediction = new Prediction(
      4,
      true,
      `wss://passgraf.com:2083/ws/<Insert-your-secret-token>`,
      predictionCB,
      wsReady
    );
```
##### Step 5
Replace ```<Insert-your-secret-token> ``` with your secret token. 
You can find your secret token at __[estimatorlab.com/estimator](https://estimatorlab.com/estimator)__ 

##### Step 6
start a python3 http server (you can use any http server). You can install Python3 from __[here](https://www.python.org/downloads/)__ 
```py
python3 -m http.server
```

If you followed the each of the step, you will have a http server running on Port 8000
which would look like:
```sh
ashish@Ashishs-MacBook-Air rock-paper-scissor % python3 -m http.server
Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...
```
##### Step 6
Open your favorite browser and go type the URL
```sh
http://0.0.0.0:8000/   or    http://localhost:8000/
```

Let us know if you have any issue by sending an email at info@throughputer.com

We reply back to each email in 1 business day.

