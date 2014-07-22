# slideshow
#### this is a simple lazyload image slideshow plugin which is developed based on jquery. 
#### you can develop more complicated slideshow plugin based on this.

#### online demo
http://tracylv.com
#### parameters:
```
var defaults =
{
    loop: true,

    //auto play
    autoplay: true,

    // duration: 5s
    duration: 5000
};

1. loop: if rotate all the slides in a circle.
2. autoplay: if auto rotate the slides without click left/right button.
3. duration: it's the duration for the autoplay. you can also seem it as the time of one slide showing when open autoplay.
```
#### usage:
1.include all the resources of slideshow in your page (need jquery)
```
<link type="text/css" href="../jquery.slideshow.css" rel="stylesheet" />

<script src="http://code.jquery.com/jquery-1.9.1.min.js" type="text/javascript"></script>
<script src="../jquery.slideshow.js" type="text/javascript"></script>
Note: don't forget the sprite images of this plugin, and adjust the relateive path of this images if need
```
2.add the below dom into your page, and update the images path.
```
<div class="slideshow">
	<a class="control prev" href="#" ></a>
	<a class="control next" href="#" ></a>
	<ul class="slide">
		<li><img src="imgs/slide1.jpg" width="700" height="400" /></li>
	</ul>
	<ul class="itemlist">
		<li class="current">
			<input type="hidden" class="img-src" img-src="imgs/slide1.jpg" />
		</li>
		<li>
			<input type="hidden" class="img-src" img-src="imgs/slide2.jpg" />
		</li>
		<li>
			<input type="hidden" class="img-src" img-src="imgs/slide3.jpg" />
		</li>
		<li>
			<input type="hidden" class="img-src" img-src="imgs/slide4.jpg" />
		</li>
		<li>
			<input type="hidden" class="img-src" img-src="imgs/slide5.jpg" />
		</li>
	</ul>
</div>
```
3.you can add more or reduce the slide item by controlling below dom's number.
```
<li>
	<input type="hidden" class="img-src" img-src="imgs/slide5.jpg" />
</li>
```
4.bind the behavior of the slideshow
```
<script type="text/javascript">
    $(function(){
	    $(".slideshow").slideshow();
	});
</script>
```
5.you can override the parameters like below
```
$(".slideshow").slideshow({loop:false, autoplay:false, duration:7000});
```
#### suggestion:
```
1. copy the css and js code of this plugin code into your own css and js file, because of this plugin's code is very little and it's not deserved to be loaded as a single file, it will increase the page load time in a way.
2. In order to avoid flicker when page load, try to give a container for this plugin and fixed a width, and adjust the left/right button's position according to your need with css.
```

