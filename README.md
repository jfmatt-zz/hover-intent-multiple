hoverIntentMultiple is a rewrite of hoverIntent to allow multiple actions to be bound to the same DOM element.

hoverIntentMultiple // 2012.10.31
<https://github.com/jfmatt/hover-intent-multiple>

hoverIntentMultiple is currently available for use in all personal or commercial 
projects under both MIT and GPL licenses. This means that you can choose 
the license that best suits your project, and use it accordingly.

Usage is the same as below, with the following changes:
**Adding an action will NOT remove actions previously registered
**To remove previously registered actions, set the configuration option clear = true
**If clearing, other options are optional (i.e. send {clear: true} to wipe out registered actions
      without adding a new one)

@param  f  onMouseOver function || An object with configuration options
@param  g  onMouseOut function  || Nothing (use configuration options object)
@author    James Matthews github.com/jfmatt

ORIGINAL HOVERINTENT HEADER TEXT:
hoverIntent is similar to jQuery's built-in "hover" function except that
instead of firing the onMouseOver event immediately, hoverIntent checks
to see if the user's mouse has slowed down (beneath the sensitivity
threshold) before firing the onMouseOver event.

hoverIntent r6 // 2011.02.26 // jQuery 1.5.1+
<http://cherne.net/brian/resources/jquery.hoverIntent.html>

hoverIntent is currently available for use in all personal or commercial 
projects under both MIT and GPL licenses. This means that you can choose 
the license that best suits your project, and use it accordingly.

// basic usage (just like .hover) receives onMouseOver and onMouseOut functions
$("ul li").hoverIntent( showNav , hideNav );

// advanced usage receives configuration object only
$("ul li").hoverIntent({
  sensitivity: 7, // number = sensitivity threshold (must be 1 or higher)
  interval: 100,   // number = milliseconds of polling interval
  over: showNav,  // function = onMouseOver callback (required)
  timeout: 0,   // number = milliseconds delay before onMouseOut function call
  out: hideNav    // function = onMouseOut callback (required)
});

@param  f  onMouseOver function || An object with configuration options
@param  g  onMouseOut function  || Nothing (use configuration options object)
@author    Brian Cherne brian(at)cherne(dot)net
