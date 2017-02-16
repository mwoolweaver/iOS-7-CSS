# Basic iOS 7 CSS
Basic, simple, semantic, and less than 2.2kb (minified and gzipped).

Integrate it with your project easily with [Bower](https://bower.io/): `bower install iOS-7-CSS`

Live example: [cydia.hbang.ws](https://cydia.hbang.ws/depiction/ws.hbang.typestatus/)

Licensed under [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0.html). UI design is copyright of Apple Inc.

## Screenshots
![Screenshot 1](https://i.imgur.com/XOKfDs3.png) &nbsp; ![Screenshot 2](https://i.imgur.com/5qAYSyl.png)

## Example Usage
```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8">
	<title>Hello World</title>

	<meta name="viewport" content="initial-scale=1, maximum-scale=1, user-scalable=0">

	<link rel="stylesheet" href="ios7.min.css">
	<script src="ios7.min.js"></script>
</head>
<body>
	<header>
		<h1>Page header.</h1>
	</header>

	<main id="content">
		<h2 role="header">Section header.</h2>
		
		<ul>
			<li>
				<p>Text element.</p>
			</li>

			<li>
				<a href="https://hbang.ws/" target="_blank" role="button">Link.</a>
			</li>

			<li>
				<button type="submit">Button.</button>
			</li>

			<li>
				<p>It’s ok to have more than one element at a time.</p>
				<p>Like so…</p>
				<a href="https://www.google.com/" target="_blank" role="button">But you should probably only use that with multiple paragraphs.</a>
			</li>
		</ul>

		<p role="footer">Section footer.</p>
	</main>
</body>
</html>
```

Note that this has changed since version 1.x. Buttons must now be specified with `role="button"`; footers must be specified with `role="footer"`. Headers *should* use `role="header"`, but the styling is still applied to `<h2>`.

## Building from SASS

Building from SASS is easy once you get off your feet by setting them up. All command below should be run in the project directory.

### If you don't have Bower and Gulp set up

You will need to have [Node.js](https://nodejs.org) and `npm` installed on your machine.

To set up Bower and Gulp for the project, run the following commands:

```
npm install -g bower gulp # Install globally so you can use the commands
npm install # Install project dependencies
```

### Getting project dependencies

Now that you have Bower working, you can use it to fetch dependencies by running:

```
bower install
```

### Building to CSS

Once you've retrieved the required project dependencies using Bower, you can finally build it using Gulp. You can do this by running:

```
gulp
```

This will create the stylesheet as a minified CSS file at "ios7.min.css". It will also include a .map file for helpful debugging.
