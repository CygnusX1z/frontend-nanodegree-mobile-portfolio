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
	<li>Resized the image _pizzaria.jpg_ from its original size of _2048 x 153_6 to _100 x 75_ px.</li>
    <li>Added <meta http-equiv="Cache-Control" content="max-age=600"/> (although admittedly it did not seem to make a difference)</li>
    <li>Minified _print.css_ (_print_mini.css_)</li>
    <li>Added _media="print"_ to _print_mini.css_ ref</li>
    <li>Inlined _Smartphones (portrait)_ script</li>
    <li>Added _async_ to script references</li>
    <li>Inlined _cb_ and _rf_ scripts</li>
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
 	<li>Moved _var dx_ outside the _for_ loop of _changePizzaSizes_ function</li>
 	<li>Moved _var newidth_ outside the _for_ loop of _changePizzaSizes_ function</li>
 	<li>Moved _document.querySelectorAll(".randomPizzaContainer")_ outside the _for_ loop and assigned it to a newly created variable array called _elements_</li>
 	<li>For _var i_ I assigned a beginning value of the _elements_ (randomPizzaContainer) instead of zero, as we will always have at least one. I then decremented</li>
 </ol>
 
 


