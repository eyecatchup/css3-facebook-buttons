# CSS3 Facebook-style Buttons #

Examples: [nicolasgallagher.com/lab/css3-facebook-buttons/](http://nicolasgallagher.com/lab/css3-facebook-buttons/)

## IE CONDITION ##

To create background gradients for IE 9 and some older versions (8-11) of Opera, this fork uses base64 encoded strings of SVG data which are attached as background-image.

Therefore, and because IE 10 has its own vendor prefix, IE 9+ needs to override 'filter' to 'none'. Thus, you need to add the following condition in your head.

```css
<!--[if gte IE 9]>
  <style type="text/css">
    .uibutton {
      filter: none;
    }
  </style>
<![endif]-->
```

## Buttons ##

To create the default "button" add a class of `uibutton` to any appropriate element. To create the blue variant include the additional class `confirm`. To create the green variant include an additional class `special`.

    <a class="uibutton" href="#">Button</a>
    <button class="uibutton" type="submit">Button</button>
    <input class="uibutton" type="submit" value="Button">

## Larger buttons ##

To create larger buttons include an additional class of `large`

    <a class="uibutton large" href="#button">Search</a>
    
## Grouped buttons ##

To created grouped buttons wrap them in an element, or use a list, given the class 'uibutton-group'.
    
    <div class="uibutton-group">
        <a href="#button" class="uibutton">Dashboard</a>
        <a href="#button" class="uibutton">Inbox</a>
        <a href="#button" class="uibutton">Account</a>
        <a href="#button" class="uibutton">Logout</a>
    </div>
    
    <ul class="uibutton-group">
        <li><a href="#button" class="uibutton">Dashboard</a></li>
        <li><a href="#button" class="uibutton">Inbox</a></li>
        <li><a href="#button" class="uibutton">Account</a></li>
        <li><a href="#button" class="uibutton">Logout</a></li>
    </ul>

## Mixed groups ##

To display a toolbar of buttons and grouped buttons, use a wrapping element given the class `uibutton-toolbar`.

    <div class="uibutton-toolbar">
        <a href="#button" class="uibutton">Mark as unread</a>
        
        <div class="uibutton-group">
            <a href="#button" class="uibutton">Report spam</a>
            <a href="#button" class="uibutton">Delete</a>
        </div>
        
        <a href="#button" class="uibutton">Unsubscribe</a>
    </div>

## Buttons with icons ##

A range of icons can be added (only for links and buttons) by adding a class of `icon` and any one of the provided icon classes.

    <a href="#" class="button icon add">New message</a>

## Browser compatibility ##

Full support: Firefox 3.6+, Google Chrome 3+, Safari 3+, IE 5.5+, Opera 8+.
Note: Some CSS3 enhancements are not supported in older versions of Opera and IE. The use of icons is not supported in IE 5.5-7.

## License ##

Public domain: [http://unlicense.org](http://unlicense.org)