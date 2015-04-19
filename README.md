# We Be Scrollin

##A stupid simple jquery plugin for animating scroll to targets via data-attributes.

Yep, that's right. Another freakin' animated scroll to target deal. We Be Scrollin is super slim (2 kbs) Jquery plugin enabled via data-attributes, with a few options for speed, easing integration, top offset, active classes, and a callback function.


## How's it Work Then?
Set up is super simple. Add the data-attribute `data-scroll="yourID"` to the link, with your unique ID on the target section. Rinse, repeat as many times as necessary. Snazz it up with an Easing lib if you that's your thing.

Your structure will look a little something like this

```html
/*---------------------------  
--Link: Add 'data-scroll' to link with unique name
----------------------------- */
<a data-scroll="sect-one" href="#"></a>

/*---------------------------  
--Target: Apply that unique name as an id
-----------------------------  */
<section id="sect-one"></section>`
```


```javascript
 $('html').weBeScrollin({
  offset: '40',
  addActive: 'true',
  scrollSpeed: 500,
  scrollEase: 'easeOutBounce',
  
  complete : function() {
      $( '.mobile-nav' ).removeClass('js-open');
    },
 });
  
```

## Options / Defualts
A few essential options are available, `offset` to make room for fixed navs, `scrollSpeed` to change to animation's speed, `scrollEase` to enable scroll acceleration/deceleration easings (include an easing lib for more options), `addActive` to add an active class to the clicked nav item (currently, the active class relies on a click event, so use a lib like Waypoints or Inview if true viewport detection is required), and let's not forget a simple after animation callback (useful for closing a mobile nav or triggering 



##Defaults / Options

| Option        			|      Description                  	|   Value 
| :-------------			| :-------------------------------:  | :------------:
| offset     			| Scroll offset from top         	 | 0 
| scrollSpeed   			| Speed of scroll animation    					| 700
| scrollEase    			| add Easing equations  				| swing  
| addActive     	 		| Enable Active link class  			  		|	False
| complete : function() {}   				| Callback function       						| Null


<tr>
<th scope="row">offset</th>
<td>Scroll offset from top</td>
<td>'0'</td>
</tr>

<tr>
<th scope="row">scrollSpeed</th>
<td>Speed of scroll animation</td>
<td>700</td>
</tr>

<tr>
<th scope="row">scrollEase</th>
<td>add Easing equations</td>
<td>Swing</td>
</tr>

<tr>
<th scope="row">addActive</th>
<td>Enable Active link class</td>
<td>False</td>
</tr>

<tr>
<th scope="row">complete : function() {}</th>
<td>Callback function</td>
<td>Null</td>
</tr>


## Check it 
Peep We Be Scrollin in action [Here→](http://webescrollin.stephenscaff.com/), 

