## Usage

This ColdBox Elixir extension allows you to compile Stylus.

## Installation

First, pull in the extension through NPM.

```
npm install --save-dev coldbox-elixir-stylus
```

That's it! You're all set to go!

## Usage

Assuming you write...

```js
elixir( function( mix ) {
   mix.stylus( "app.styl" );
} );
```

...this will compile your `resources/assets/stylus/app.styl` file to `./includes/css/app.css`.

If you'd like to set a different output directory, you may pass a second argument to the `stylus()` method, like so:

```js
mix.stylus( "app.styl", "./public/scripts/styles.css" );
```

Finally, if you want to override the Stylus plugin options, you may pass an object as the third argument.

```js
mix.stylus( "app.styl", null, {} );

// See options at: https://www.npmjs.com/package/gulp-stylus#options
```

## PostCSS

This extension includes a PostCSS adapter out of the box, as well as support for the incredibly impressive [Lost](https://github.com/peterramsing/lost) grid system. Check out the documentation in that link, and immediately start using it in your projects with this extension. Zero setup. :)

If there are other PostCSS plugins you want to pull in, you may use the third argument to `mix.stylus()`

```js
var postStylus = require( "poststylus" ); // npm install poststylus --save-dev

mix.stylus( "app.styl", null, {
   use: [ postStylus( [ "lost", "postcss-position" ] ) ]
} );
```

## Contributions and Bugs

Project tracking for this project can be found at the [Ortus Solutions Jira](https://ortussolutions.atlassian.net/projects/ELIXIR/summary).  Please log all bugs, improvements, and features there.

Pull requests are welcome and encouraged.  Please [check on the Jira page](https://ortussolutions.atlassian.net/projects/ELIXIR/issues/?filter=allissues) before starting any large amount of work so your time isn't wasted.

Brad Wood (@bdw429s) has a [great guide on submitting pull requests.](https://www.ortussolutions.com/blog/submit-your-first-pull-request-to-an-open-source-project)  If you are unsure where to go, in need of help, or have a question, come ask in the #box-products channel on the [CFML Slack](http://cfml-slack.herokuapp.com/).
