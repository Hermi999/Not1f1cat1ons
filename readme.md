# Not1f1cat1ons

Not1f1cat1ons is a JavaScript-Library for displaying notifications in your web application. 

### Version
0.1

### Installation
Add [jQuery] and Not1f1cat1ons to your html file:
```html
<script type="text/javascript" src="jquery-3.0.0.js"></script>
<script type="text/javascript" src="not1f1cat1ons-0.1.js"></script>
```

### Usage
Define the div element which should be used as notification element:
```html
<div class="notify1"></div>
```

Create elements which should be used for triggering the notficiations:
```html
<button id="demo1a">Event 1</button>
<button id="demo1b">Event 2</button>
<button id="demo1c">Event 3</button>
<button id="demo1c">Event 4</button>
```

Register the div element which should be used for displaying the notifications:
```javascript
var notify1 = new Not1f1cat1ons("notify1");
```

If the event occurs which should trigger the notification, call the "triggerNotification" function:
```javascript
$('#demo1a').click(function(){
  notify1.triggerNotification("success", "Successfully clicked on <i>div-Element</i>");
});
$('#demo1b').click(function(){
  notify1.triggerNotification("warning", "Warning. Clicked on <i>div-Element</i>");
});
$('#demo1c').click(function(){
  notify1.triggerNotification("alert", "Alert. Clicked on <i>div-Element</i>");
});
$('#demo1d').click(function(){
  notify1.triggerNotification("info", "Info. Clicked on <i>div-Element</i>");
});
```

### Configuration
##### Constructor

```javascript
function Not1f1cat1ons(element_class_name, animation, hidden_position, visible_position, default_style, success_style, alert_style, warning_style)
```
| Parameter          | Type          | Description  |
| ------------------ |---------------| -------------|
| element_class_name | String        | Class name of the element which should be used for the notifications, |
| animation          | object        | **show_duration** (Number) ... Defines how fast the animation for showing the notification should be. |
|                    |               | **visible_duration** (Number) ... Defines how long the notification should be shown. |
|                    |               | **hide_duration** (Number) ... Define how fast the animation for showing the notification should be. |
|                    |               | **direction** (String) ... Defines In which direction the notification element should be sliding when its getting visible. At the moment as animation type only 'sliding' is possible. |
| hidden_position    | object        | Defines where the notification element should be positioned when it's **not visible**. You can use css parameters like: **position, top, left, ...** |
| visible_position   | object        | Defines where the notification element should be positioned when it's **visible**. You can use css parameters like: **position, top, left, ...** |
| default_style      | object        | Changes the **default** style of the notification element. You can use any css parameters, but don't use the parameters for posistioning. |
| success_style      | object        | Changes the style of the notification element if the notification has type **success**. You can use any css parameters, but don't use the parameters for posistioning. |
| alert_style        | object        | Changes the style of the notification element if the notification has type **alert**. You can use any css parameters, but don't use the parameters for posistioning. |
| warning_style      | object        | Changes the style of the notification element if the notification has type **warning**. You can use any css parameters, but don't use the parameters for posistioning. |
| info_style      | object        | Changes the style of the notification element if the notification has type **info**. You can use any css parameters, but don't use the parameters for posistioning. |

##### triggerNotification

```javascript
function triggerNotification(type, html, style, animation)
```
| Parameter          | Type          | Description  |
| ------------------ |---------------| -------------|
| type               | String        | Type of the notification: **"success", "alert", "warning"**|
| html               | String        | Notification content in HTML or Text |
| style              | Object        | Overwrite style of the notification type for this single notification |
| animation          | Object        | Overwrite animation of the notification type for this single notification |

### License
MIT

### Author
Created by **[Hermann Wagner]**


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

[//]: # (Markdown Cheatsheet: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

   [jQuery]: <https://jquery.com/>
   [Hermann Wagner]: <mailto: hermann.wagner@rentog.com>
