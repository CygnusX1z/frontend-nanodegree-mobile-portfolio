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
    <li>Minimized _print.css_ (_print_mini.css_)</li>
    <li>Added _media="print"_ to _print_mini.css_ ref</li>
    <li>Inlined _Smartphones (portrait)_ script</li>
    <li>Added async to script references</li>
    <li>Inlined _cb_ and _rf_ scripts</li>
 </ol>
 
 **pizza.html** achieve an FPS of 60 consistently when scrolling
 To achieve this I 
 <ol>
 	<li>Reduced the size of pizza.png as well as optimized for web using Adobe Image Ready 7</li>
 	<li>Reduced the number of pizzas created from the original 200 down to 35</li>
 	<li></li>
 </ol>
 
 


