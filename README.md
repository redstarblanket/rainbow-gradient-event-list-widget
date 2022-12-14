# Rainbow Gradient Event List Widget with Animated "Glitter" Effect - Customizable Width
Custom CSS and JSON for event list widgets that can be copied and pasted into the Streamlabs code editor.
- The CSS is what gives it its look. 
- The JSON will make it so you can adjust the width of the event list without having to touch the code.

https://user-images.githubusercontent.com/75779842/186792798-eb10efbf-bde3-4a51-966c-306eb895e5e5.mov

## Using it in Streamlabs

### 1. Copy the CSS code below
![ezgif com-gif-maker (3)](https://user-images.githubusercontent.com/75779842/186799330-7ffdc973-6b74-4c9e-9331-fcd60b463668.gif)

Or you can go to [style.css](https://github.com/redstarblanket/rainbow-gradient-event-list-widget/blob/dank/style.css) to copy it.

### 2. Make sure custom HTML/CSS is enabled in your Streamlabs event list dashboard

<img width="455" alt="Screen Shot 2022-08-25 at 8 13 19 PM" src="https://user-images.githubusercontent.com/75779842/186802029-3c3337eb-f833-4459-9f8e-c5b778fd7112.png">

### 3. Paste the code into the CSS section of the Streamlabs code editor (replace any pre-existing code)

![ezgif com-gif-maker (4)](https://user-images.githubusercontent.com/75779842/186803824-ca8deb75-6d3d-467e-8cf1-4c493a48cc3d.gif)

The widget will show up in the Streamlabs software when you add the event list as a browser source.

### 4. Copy the JSON code 
It is located beneath the CSS code, or you can go to [width.JSON](https://github.com/redstarblanket/rainbow-gradient-event-list-widget/blob/dank/width.JSON) to copy it.

### 5. Add custom fields and open up the custom fields editor

Click on the "Add Custom Fields" button located to the bottom right of the code editor.

<img width="600" alt="Screen Shot 2022-09-13 at 1 17 20 AM" src="https://user-images.githubusercontent.com/75779842/189836478-41642487-0421-43f6-8c40-685b9de168cd.png">

Then, click on the "Edit Custom Fields" button to open up the editor.

<img width="600" alt="Screen Shot 2022-09-13 at 1 07 54 AM" src="https://user-images.githubusercontent.com/75779842/189851097-f48aa8c6-06c8-4fed-8133-90d4a5b49637.png">


### 6. Paste the JASON code into the custom fields editor
It is okay to replace any existing code.

<img width="388" alt="Screen Shot 2022-09-13 at 2 30 00 AM" src="https://user-images.githubusercontent.com/75779842/189852166-b11fc426-e5bc-4634-bc1c-4c2a3985db73.png">

<img width="388" alt="Screen Shot 2022-09-13 at 2 49 53 AM" src="https://user-images.githubusercontent.com/75779842/189856969-a66a20b3-db0d-4d84-96d4-0655ba0433bd.png">


Click "Update" and the width slider will appear.

<img width="600" alt="Screen Shot 2022-09-13 at 2 33 08 AM" src="https://user-images.githubusercontent.com/75779842/189853026-110715f6-4cb0-4b5e-9ebd-5b23bfe6bbcb.png">


## Using it in OBS

To use the widget in OBS, copy the widget URL from the Streamlabs.com event list dashboard after the CSS has been pasted in the code editor.

<img width="951" alt="Screen Shot 2022-09-04 at 8 12 43 PM" src="https://user-images.githubusercontent.com/75779842/188347488-a64fefab-7281-4035-8da2-a82bc5d31e2f.png">

Add a new browser source then paste the URL into URL field

<img width="385" alt="Screen Shot 2022-09-04 at 8 22 57 PM" src="https://user-images.githubusercontent.com/75779842/188348972-5d990fa5-c9ed-431a-82d8-9ff199045f00.png"> <img width="440" alt="Screen Shot 2022-09-04 at 8 23 30 PM" src="https://user-images.githubusercontent.com/75779842/188349091-a17d0ba3-22bc-4ebc-b13d-189671925b9a.png">



## The CSS Code

```
@import url('https://fonts.googleapis.com/css2?family=Silkscreen&display=swap');

html, .widget-EventList li > div {
-webkit-transform: rotateX({rotate_x}) rotateY({rotate_y});
 transform: rotateX({rotate_x}) rotateY({rotate_y}); 
    
}

.widget-EventList, .widget-EventList * {
    box-sizing: border-box;
  	text-shadow: 4px 4px 12px #333;
}

.widget-EventList {
    font-weight: 700;
    font-size: 40px;
    font-family: 'Silkscreen', 'sans-serif';
    color: #ebf9ff;
    overflow: hidden;
    list-style: none;
    padding: 0;
    text-transform: uppercase;
    position: relative;

}

.widget-EventList li {
    width: {barWidth};
    position: relative;
  	-webkit-animation: myAnim 1.5s ease-in 0s 1 normal;
  					animation: myAnim 1.5s ease-in 0s 1 normal;
}

@-webkit-keyframes myAnim {
	0% {
		transform: translateY(-15px);
	}

	100% {
		transform: translateY(0px);
	}
}

@keyframes myAnim {
	0% {
		transform: translateY(-15px);
	}

	100% {
		transform: translateY(0px);
	}
}
.widget-EventList li > div:first-child {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border-radius: 10px;
    border: 3px solid rgba(235, 249, 255, 0.75);
    opacity: 0.7;
    -webkit-transition: opacity 0.5s linear 2s;
            transition: opacity 0.5s linear 2s;
}

.widget-EventList li > div:last-child {
    overflow: hidden;
    position: relative;
    margin-bottom: 4px;
    padding: 0 10px;
    opacity: 0.7;
    font-size: 0.9em;
    height: 1.2em;
    line-height: 1.2em;
}

.widget-EventList li:first-child > div:first-child {
    opacity: 1;
}

.widget-EventList li:first-child > div:last-child {
    -webkit-animation: growA 1.5s forwards;
  	animation: growA 1.5s forwards;
}


@-webkit-keyframes growA {
    0% {
        opacity: 0;
        font-size: 0em;
        height: 0em;
        line-height: 0em;
        margin-bottom: 0px;
        padding: 0;
    }

    100% {
        opacity: 1;
        font-size: 1em;
        height: 1.6em;
        line-height: 1.6em;
        margin-bottom: 4px;
        padding: 0 10px;
    }
}


@keyframes growA {
    0% {
        opacity: 0;
        font-size: 0em;
        height: 0em;
        line-height: 0em;
        margin-bottom: 0px;
        padding: 0;
    }

    100% {
        opacity: 1;
        font-size: 1em;
        height: 1.6em;
        line-height: 1.6em;
        margin-bottom: 4px;
        padding: 0 10px;
    }
}

.widget-EventList .tag {
    font-size: 0.6em;
    line-height: 0.6em;
    top: 0.4em;
    right: 0.3em;
    position: absolute;
}

.widget-EventList .message {
    padding-right: 3em;
    display: block;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}

.widget-EventList li {
    text-shadow: 0 0 1px rgba(0, 0, 0, 0.7), 0 0 2px rgba(0, 0, 0, 0.7), 0 0 3px rgba(0, 0, 0, 0.7);
}

.widget-EventList li > div:first-child {
  	
    background: url("https://raw.githubusercontent.com/redstarblanket/event-list-widget/dank/snowfall-glitter.gif"), linear-gradient(90deg, rgba(255,117,174,1) 0%, rgba(252,163,132,1) 15%, rgba(246,230,154,1) 32%, rgba(187,250,165,1) 50%, rgba(126,230,249,1) 67%, rgba(104,138,251,1) 83%, rgba(165,131,255,1) 100%);
}
```
## The JSON Code

```
{
    "barWidth": {
        "label": "Width",
        "type": "slider",
        "value": 600,
        "max": 800,
        "min": 600,
        "steps": 1
    }
}
```

![redStarMini](https://user-images.githubusercontent.com/75779842/186808377-9a416a1c-25af-4eae-8ae0-1c013dba15da.png)**Hippity Hoppity This Code Is OUR Property**

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/O4O5BY0J2)



