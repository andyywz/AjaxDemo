* linking to stylesheet
* * <link rel="stylesheet" href="directory">
* grabbing document with jQuery
* * use `document` not `html`
* head
* * doesn't show up on th epage typically.
* * define stylesheets, and can put javascript stuff (will block rest of document until it loads) but should not
* * async tag can get around this behaviour
* * instead, put scripts at the end of the page most of the time (can't look for tags with jquery that are before the script is loaded)
* unobtrusive javascript
* * functionality without any javascript
-------
* every browser (user-agent as it calls itself) has a default stylesheet
* * default styles with some html tags (browser specific)
* * * solution: reset stylesheet (gets rid of existsing styles), normalize stylesheet (Eric Meyer)
* * * or add them to your own stylesheet on the go
Prescedence
----
* all tags inherit from body
* #id (trump card), .class , tag
* most specific wins
* figure img {}
* * means img inside a figure tag, regardless of how deeply its nested
* * direct descendants should be done with a > symbol
* <input type="submit">
* * targetted with input[type="submit"]
* * attributes go into brackets
* asterix is for everything
Toggling
------
* <div class="lamp-on">
  * state that is on

  .lamp-on {
    display:none;
  }
  .lamp-off {
    display:block;
  }
  .is-on > .lamp-on {
    display:block;
  }
  .is-on > .lamp-off {
    display:none;
  }

  * switch parameter in the toggleClass method
  * don't bind a form submission on a click use: on("submit", function..)
  * find more jquery events (DOM events), like
Random
--------
* padding