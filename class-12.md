# Images

#### You can control the size of an image using the width and height properties in CSS, just like you can for any other box.

* you need to determine the sizes of images:
    * small
    * medium
    * large

### Aligning images using CSS

        align-left 
        align-right

### Background Images
    
* `background-image`

### Repeating Images
* `background-repeat`
    * `repeat`
    * `repeat-x`
    * `repeat-y`
    * `no-repeat`
* `background-attachment`
    * `fixed`
    * `scroll`

### Background Position
* background-position
    * left top
    * left center
    * left bottom
    * center top
    * center center
    * center bottom
    * right top
    * right center
    * right bottom

### shorthand
* background
    * background-color
    * background-image
    * background-repeat
    * background-attachment
    * background-position


## CSS3: Gradients
* background-image

## Contrast of background images
* High Contrast
* Low Contrast
* Screen

---
---

# Practical Information
#### To wrap up the book we are going to look at some practical information that will help you launch a successful site.

## Search Engine Optimization(SEO)
* The Basics
* On-Page Techniques
* Off-Page Techniques

### On-Page SEO
1. Page Title
2. URL/Web Address
3. Headings
4. Text
5. Link Text
6. Image Alt Text
7. Page Descriptions

### How to Identify Keywords and Phrases
1. Brainstorm
2. Organize
3. Research
4. Compare
5. Refine
6. Map

### How Many People Are Coming to Your Site
* Visits
* Unique Visits
* Page Views
* Pages per Visit
* Average Time on Site
* Date Selector
* Export

### What Are Your Visitors Looking At?
* Pages
* Landing Pages
* Top Exit Pages
* Bounce Rate

### Where Are Your Visitors Coming From?
* Referrers
* Direct
* Search Terms
* Advanced Features

### Domain Names & Hosting
1. Domain name
2. Web hosting
    * Disk space
    * Bandwidth
    * Backups
    * Email accounts
    * Server-side languages and databases
3. Hosted Services

### FTP & Third Party Tools
* To transfer your code and images from your computer to your hosting company.

---
---

## Video and Audio APIs

|Prerequisites|Objective |
|----|----|	
|JavaScript basics (see [first steps](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps), [building blocks](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks), [JavaScript objects](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects)), the [basics of Client-side APIs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Introduction)| To learn how to use browser APIs to control video and audio playback.|

## HTML5 video and audio
#### The `<video>` and `<audio>` elements allow us to embed video and audio into web pages. As we showed in Video and audio content, a typical implementation looks like this:

        <video controls>
        <source src="rabbit320.mp4" type="video/mp4">
        <source src="rabbit320.webm" type="video/webm">
        <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
        </video>

## The HTMLMediaElement API
#### Part of the HTML5 spec, the HTMLMediaElement API provides features to allow you to control video and audio players programmatically — for example HTMLMediaElement.play(), HTMLMediaElement.pause(), etc. This interface is available to both `<audio>` and `<video>` elements, as the features you'll want to implement are nearly identical. Let's go through an example, adding features as we go.


![](https://mdn.github.io/learning-area/javascript/apis/video-audio/finished/video/sintel-short.mp4)

## Getting started
## Exploring the HTML
Open the HTML index file. You'll see a number of features; the HTML is dominated by the video player and its controls:

        <div class="player">
        <video controls>
            <source src="video/sintel-short.mp4" type="video/mp4">
            <source src="video/sintel-short.webm" type="video/webm">
            <!-- fallback content here -->
        </video>
        <div class="controls">
            <button class="play" data-icon="P" aria-label="play pause toggle"></button>
            <button class="stop" data-icon="S" aria-label="stop"></button>
            <div class="timer">
            <div></div>
            <span aria-label="timer">00:00</span>
            </div>
            <button class="rwd" data-icon="B" aria-label="rewind"></button>
            <button class="fwd" data-icon="F" aria-label="fast forward"></button>
        </div>
        </div>

## Exploring the CSS
##### Now open the CSS file and have a look inside. The CSS for the example is not too complicated, but we'll highlight the most interesting bits here. First of all, notice the .controls styling:

        .controls {
        visibility: hidden;
        opacity: 0.5;
        width: 400px;
        border-radius: 10px;
        position: absolute;
        bottom: 20px;
        left: 50%;
        margin-left: -200px;
        background-color: black;
        box-shadow: 3px 3px 5px black;
        transition: 1s all;
        display: flex;
        }

        .player:hover .controls, player:focus .controls {
        opacity: 1;
        }

##### Next, let's look at our button icons:

        @font-face {
        font-family: 'HeydingsControlsRegular';
        src: url('fonts/heydings_controls-webfont.eot');
        src: url('fonts/heydings_controls-webfont.eot?#iefix') format('embedded-opentype'),
                url('fonts/heydings_controls-webfont.woff') format('woff'),
                url('fonts/heydings_controls-webfont.ttf') format('truetype');
        font-weight: normal;
        font-style: normal;
        }

        button:before {
        font-family: HeydingsControlsRegular;
        font-size: 20px;
        position: relative;
        content: attr(data-icon);
        color: #aaa;
        text-shadow: 1px 1px 0px black;
        }

##### Last but not least, let's look at the CSS for the timer:

        .timer {
        line-height: 38px;
        font-size: 10px;
        font-family: monospace;
        text-shadow: 1px 1px 0px black;
        color: white;
        flex: 5;
        position: relative;
        }

        .timer div {
        position: absolute;
        background-color: rgba(255,255,255,0.2);
        left: 0;
        top: 0;
        width: 0;
        height: 38px;
        z-index: 2;
        }

        .timer span {
        position: absolute;
        z-index: 3;
        left: 19px;
        }

## Implementing the JavaScript
##### We've got a fairly complete HTML and CSS interface already; now we just need to wire up all the buttons to get the controls working.

##### 1. Create a new JavaScript file in the same directory level as your index.html file. Call it custom-player.js.

#####  2. At the top of this file, insert the following code:

        const media = document.querySelector('video');
        const controls = document.querySelector('.controls');

        const play = document.querySelector('.play');
        const stop = document.querySelector('.stop');
        const rwd = document.querySelector('.rwd');
        const fwd = document.querySelector('.fwd');

        const timerWrapper = document.querySelector('.timer');
        const timer = document.querySelector('.timer span');
        const timerBar = document.querySelector('.timer div');

##### 3. Next, insert the following at the bottom of your code:

        media.removeAttribute('controls');
        controls.style.visibility = 'visible';

## Playing and pausing the video

##### 1. First of all, add the following to the bottom of your code, so that the playPauseMedia() function is invoked when the play button is clicked:

        play.addEventListener('click', playPauseMedia);

##### 2. Now to define playPauseMedia() — add the following, again at the bottom of your code:

        function playPauseMedia() {
        if(media.paused) {
            play.setAttribute('data-icon','u');
            media.play();
        } else {
            play.setAttribute('data-icon','P');
            media.pause();
        }
        }

## Stopping the video
##### 1. Next, let's add functionality to handle stopping the video. Add the following addEventListener() lines below the previous one you added:

        stop.addEventListener('click', stopMedia);
        media.addEventListener('ended', stopMedia);

##### 2. Next, let's define stopMedia() — add the following function below playPauseMedia():

        function stopMedia() {
        media.pause();
        media.currentTime = 0;
        play.setAttribute('data-icon','P');
        }

## Seeking back and forth

##### 1. First of all, add the following two addEventListener() lines below the previous ones:

        rwd.addEventListener('click', mediaBackward);
        fwd.addEventListener('click', mediaForward);


##### 2. Now on to the event handler functions — add the following code below your previous functions to define mediaBackward() and mediaForward():

        let intervalFwd;
        let intervalRwd;

        function mediaBackward() {
        clearInterval(intervalFwd);
        fwd.classList.remove('active');

        if(rwd.classList.contains('active')) {
            rwd.classList.remove('active');
            clearInterval(intervalRwd);
            media.play();
        } else {
            rwd.classList.add('active');
            media.pause();
            intervalRwd = setInterval(windBackward, 200);
        }
        }

        function mediaForward() {
        clearInterval(intervalRwd);
        rwd.classList.remove('active');

        if(fwd.classList.contains('active')) {
            fwd.classList.remove('active');
            clearInterval(intervalFwd);
            media.play();
        } else {
            fwd.classList.add('active');
            media.pause();
            intervalFwd = setInterval(windForward, 200);
        }
        }

##### 3. Finally, we need to define the windBackward() and windForward() functions invoked in the setInterval() calls. Add the following below your two previous functions:

        function windBackward() {
        if(media.currentTime <= 3) {
            rwd.classList.remove('active');
            clearInterval(intervalRwd);
            stopMedia();
        } else {
            media.currentTime -= 3;
        }
        }

        function windForward() {
        if(media.currentTime >= media.duration - 3) {
            fwd.classList.remove('active');
            clearInterval(intervalFwd);
            stopMedia();
        } else {
            media.currentTime += 3;
        }
        }

## Updating the elapsed time

##### Add the following addEventListener() line just below the others:

        media.addEventListener('timeupdate', setTime);

##### Now to define the setTime() function. Add the following at the bottom of your file:

            function setTime() {
            let minutes = Math.floor(media.currentTime / 60);
            let seconds = Math.floor(media.currentTime - minutes * 60);
            let minuteValue;
            let secondValue;

            if (minutes < 10) {
                minuteValue = '0' + minutes;
            } else {
                minuteValue = minutes;
            }

            if (seconds < 10) {
                secondValue = '0' + seconds;
            } else {
                secondValue = seconds;
            }

            let mediaTime = minuteValue + ':' + secondValue;
            timer.textContent = mediaTime;

            let barLength = timerWrapper.clientWidth * (media.currentTime/media.duration);
            timerBar.style.width = barLength + 'px';
            }

## Fixing play and pause

##### First of all, add the following lines inside the stopMedia() function — anywhere will do:

        rwd.classList.remove('active');
        fwd.classList.remove('active');
        clearInterval(intervalRwd);
        clearInterval(intervalFwd);


## You can see alot information about Video and Audio from the  [link](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs)