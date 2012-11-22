#hoverIntentMultiple

hoverIntentMultiple is a modification of [hoverIntent](http://cherne.net/brian/resources/jquery.hoverIntent.html
) to allow multiple actions to be bound to the same DOM element, as requested on [StackOverflow](http://stackoverflow.com/questions/13155754/adding-different-timeouts-to-jquery-scripts/13156125#13156125).

hoverIntentMultiple is currently available for use in all personal or commercial 
projects under both MIT and GPL licenses. This means that you can choose 
the license that best suits your project, and use it accordingly.

#Usage

    // basic usage (just like .hover) receives onMouseOver and onMouseOut functions
    $("ul li").hoverIntentMultiple( showNav , hideNav );

    // advanced usage receives configuration object only
    $("ul li").hoverIntentMultiple({
      sensitivity: 7, // number = sensitivity threshold (must be 1 or higher)
      interval: 100,   // number = milliseconds of polling interval
      over: showNav,  // function = onMouseOver callback (required if clear is not set)
      timeout: 0,   // number = milliseconds delay before onMouseOut function call
      out: hideNav    // function = onMouseOut callback (required if clear is not set)
      clear: false    // whether previously bound hoverIntents should be removed
    });

    @param  f  onMouseOver function || An object with configuration options
    @param  g  onMouseOut function  || Nothing (use configuration options object)

* Adding an action will NOT remove actions previously registered
* To remove previously registered actions, set the configuration option clear = true
* If clearing, all other options are optional (i.e. send {clear: true} to wipe out registered actions
      without adding a new one)


&copy; 2012 James Matthews, hereby released under the MIT and GPLv3 licenses.

hoverIntent &copy; [Brian Cherne](http://cherne.net/brian/resources/jquery.hoverIntent.html), used under the MIT license