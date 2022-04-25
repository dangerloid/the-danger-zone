---
aliases: ‹main›
tags: study
---
[[HTML]]
# HTML Main Tag

## definition and usage

`<main>` specifies the main content of a document.

The content inside should be unique to the document.
No content shall be repeated.
Only one `<main>` tag per document.
Not a descendant to any other tag.

## attributes

- [[HTML Event Attributes]]
- [[HTML Global Attributes]]

## examples

the `<main>` tag in action

``` html
<main>
	<h1>Most Popular Browsers</h1>
	<p>Chrome, Firefox and Edge are the most used browsers today.</p>
	
	<article>
		<h2>Google Chrome<h2>
		<p>Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!</p>
	</article>

	<article>
		<h2>Mozilla Firefox</h2>
		<p>Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.</p>
	</article>

	<article>
		<h2>Microsoft Edge</h2>
		<p>Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.</p>
	</article>
</main>
```

styling the `<main>` element with [[CSS]]

```html
<html>
	<head>
		<style>
		main {
			margin: 0;
			padding: 5px;
			background-color: lightgray;
		}
		main > h1, p, .browser {
			margin: 10px;
			padding: 5px;
		}
		.browser {
			background: white;
		}
		.browser > h2, p {
			margin: 4px;
			font-size: 90%;
		}
		</style>
	</head>
	<body>
		<main>
			<h1>Most Popular Browsers</h1>
			<p>Chrome, Firefox and Edge are the most used browsers today.</p>
	
			<article class="browser">
				<h2>Google Chrome<h2>
				<p>Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!</p>
			</article>

			<article class="browser">
				<h2>Mozilla Firefox</h2>
				<p>Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.</p>
			</article>

			<article class="browser">
				<h2>Microsoft Edge</h2>
				<p>Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.</p>
			</article>
		</main>
	</body>
</html>
```

### references

[Main Tag from W3Schools](https://www.w3schools.com/tags/tag_main.asp)