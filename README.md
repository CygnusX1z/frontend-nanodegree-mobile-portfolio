**frontend-nanodegree-mobile-portfolio-project4**
**Frontend Project 4**
=======
## Website Performance Optimization portfolio project


**index.html** is the start page. From index.html you can reach Build Your Own 2048! What the hell is a 2048? as well as the Pizzeria page. 
PageSpeed Insights for **index.html** 
<ul>
	<li>Mobile: 95/100</li>
	<li>Desktop: 97/100</li>
</ul>
To achieve these scores I 
<ol>
	<li>Resized the image pizzaria.jpg from its original size of 2048 x 1536 to 100 x 75 px</li>
    <li>Added _meta http-equiv="Cache-Control" content="max-age=600"_ (although admittedly it did not seem to make a difference)</li>
    <li>Minified print.css (print_mini.css)</li>
    <li>Added media="print" to print_mini.css ref</li>
    <li>In-lined Smartphones (portrait) script</li>
    <li>Added async to script references</li>
    <li>In-lined cb and rf scripts</li>
 </ol>
 
 **pizza.html** achieve an FPS of 60 consistently when scrolling
 To achieve this I 
 <ol>
 	<li>Reduced the size of _pizza.png_ as well as optimized for web using Adobe Image Ready 7</li>
 	<li>Minified _main.js_</li>
 	<li>Reduced the number of pizzas created from the original 200 down to 35</li>
 	<li>Added _requestAnimationFrame_ to scrolling event listener</li>
 	<li>Took _(document.body.scrollTop / 1250)_ out of the _for_ loop in the _phase_ variable and assigned it to a new variable called _top_ and put it outside the _for_ loop</li>
 	<li>In the _i_ var I assigned the beginning count to the length of the 'mover' items then decremented instead incremented </li>
 	<li>Added _"translateX("+left+") translateZ(0)";_ to _updatePosition_ function instead of using _items_ array</li>
 	
 </ol>
 
 **pizza.html** achieve 5ms or less when changing pizza sizes on slider. 
 <ol>
 	<li>Moved _var dx_ outside the _for_ loop of _changePizzaSizes_ function</li>
 	<li>Moved _var newidth_ outside the _for_ loop of _changePizzaSizes_ function</li>
 	<li>Moved _document.querySelectorAll(".randomPizzaContainer")_ outside the _for_ loop and assigned it to a newly created variable array called _elements_</li>
 	<li>For _var i_ I assigned a beginning value of the _elements_ (randomPizzaContainer) variable instead of zero, as we will always have at least one. I then decremented</li>
 </ol>
 
 **Resources**
 <ul>
 	<li><a href="https://developer.chrome.com/devtools/docs/demos/too-much-layout/index">Google Timeline demo</a></li>
 	<li><a href="https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Fcygnusx1z.github.io%2Ffrontend-nanodegree-mobile-portfolio-project4%2F&tab=mobile">PageSpeed Insights</a></li>
 	<li><a href="https://developer.chrome.com/devtools/docs/network">Evaluating network performance</a></li>
 	<li><a href="http://jscompress.com">jscompress.com</a></li>
 	<li><a href="http://jankfree.org/">jankfree</a></li>
 	<li><a href="http://www.smashingmagazine.com/2013/06/10/pinterest-paint-performance-case-study/">Gone In 60 Frames Per Second: A Pinterest Paint Performance Case Study</a></li>
 </ul>
 
 


