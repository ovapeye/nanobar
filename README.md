nanobar
=======

Very very lighweight progress bars

## Installation

Download and extract the last release from [here](https://github.com/jacoborus/nanobar/archive/master.zip) or install with Bower
```
$ bower install nanobar
```

## Usage

Link `nanobar.js` from your html file

```
<script src="path/to/nanobar.js"></script>
```

or require it with [Browserify](http://browserify.org/):

```js
var Nanobar = require('path/to/nanobar.js')
```

### Generate progressbar

```js
var nanobar = new Nanobar( options );
```

**options**

- `bg` `<String>`: background css property, '#000' by default
- `id` `<String>`: id for **nanobar** div
- `target` `<DOM Element>`: (optional) Where to put the progress bar, **nanobar** will be fixed to top of document if `target` is `null`


### Move bar

Resize the bar with `nanobar.go(percentage)`

**arguments**

- `percentage` `<Number>` : percentage width of nanobar


## Example

Create bar

```js
var options = {
	background: '#acf',
	// left target blank for global nanobar
	target: document.getElementById('myDivId'),
	// id for new nanobar
	id: 'mynano'
};

var nanobar = new Nanobar( options );

//move bar
nanobar.go( 30 ); // size bar 30%

// Finish progress bar
nanobar.go(100);
```

<br><br>

---

© 2014 [jacoborus](https://github.com/jacoborus)

Released under [MIT License](https://raw.github.com/jacoborus/nanobar/master/LICENSE)