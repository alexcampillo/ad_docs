---
layout: post
title:  "Useful JQuery"
date:   2015-01-18 14:46:55
categories: jekyll update
---
JQuery is a JavaScript framework that makes manipulating DOM elements simple. It also simplifies other processes such as querying data from both the web or a database. Most modern front end frameworks either directly integrate with jQuery or rely on it as a foundation.

####Some advantages

  *  cross browser compatable
  *  less code
  *  great documentation/large user community
  *  flexible (plays nice with other frameworks)

##Getting Started
Include jQuery in the footer of your HTML document or the 'footer.html' file in the jekyll '_includes' folder. put your jQuery in a 'script.js' file, make sure it goes below the jQuery include file.

{% highlight html %}
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
<script src="js/script.js"></script>
{% endhighlight %}

Inside of your 'script.js' file wrap all of your jQuery in the following function.

{% highlight javascript %}
$(document).ready(function() {
	/* add your code here */
});
{% endhighlight %}

This ensures the code won't execute until after the HTML loads. If your jQuery loads first, it won't have any DOM elements to grab on to.

##Events
Events are website behavior triggered by a user's interaction. 

####Common events

{% highlight javascript %}
.click();
.submit();
.keypress();
{% endhighlight %}

####Event handlers
Event handlers are functions within the event that will execute upon a user's interaction with the selected DOM element.

##JQuery Methods
{% highlight javascript %}
.hide();
.show();
.toggle();
.addClass();
.removeClass();
.toggleClass();
{% endhighlight %}

####.hide()
hides the selected HTML element
{% highlight javascript %}
$('.DOMElement').submit(function() {
	$('.otherElement').hide();
}
{% endhighlight %}

####.show()
Shows the selected HTML element
{% highlight javascript %}
$('.DOMElement').click(function() {
	$('.otherElement').show();
}
{% endhighlight %}

####.toggle()
Alternates hiding and showing an element, typically used in hiding and showing navigation menu.
{% highlight javascript %}
$('.DOMElement').click(function() {
	$('.otherElement').toggle();
}
{% endhighlight %}

####.addClass()
Adds a CSS class to an element, good for error messages and confirmation forms. 
{% highlight javascript %}
$('.DOMElement').submit(function() {
	$('.otherElement').addClass('classToAdd');
}
{% endhighlight %}

####.removeClass()
Removes a class from an element, good for error messages and confirmation forms.
{% highlight javascript %}
$('.DOMElement').click(function() {
	$('.otherElement').removeClass('classToRemove');
}
{% endhighlight %}

####.toggleClass()
Alternates adding and removing a class from an element, good for error messages, confirmation forms, buttons, links, pictures and more.  'toggle()' and 'toggleClass()' are your workhorses in the DOM.
{% highlight javascript %}
$('.DOMElement').click(function() {
	$('.otherElement').toggleClass('classToToggle');
}
{% endhighlight %}
