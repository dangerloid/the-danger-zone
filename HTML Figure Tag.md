---
aliases: ‹figure›
tags: study
---
[[HTML]]
# HTML Figure Tag

## definition and usage

The `<figure>` tag specifies self-contained content, like illustrations, diagrams, photos, code listing etc.

It shouldn't affect the flow of the document if removed.

## attributes

- [[HTML Global Attributes]]
- [[HTML Event Attributes]]

## examples

```html
<figure>
	<img src="pic_trulli.jpg" alt="Trulli" style="width=100%">
	<figcaption>Fig 1. - Trulli, Puglia, Italy</figcaption>
</figure>
```

using [[CSS]] to style `<figure>` and `<figcaption>`.

```html
<html>
	<head>
		<style>
			figure {
				border: 1px #cccccc solid;
				padding: 4px;
				margin: auto;
			}
			figcaption {
				background-color: black;
				color: white;
				font-style: italic;
				padding: 2px;
				text-align: center;
			}
		</style>
	</head>
	<body>
		<figure>
			<img src="pic_trulli.jpg" alt="Trulli" style="width=100%">
			<figcaption>Fig 1. - Trulli, Puglia, Italy</figcaption>
		</figure>
	</body>
</html>
```

[[CSS]] defaults

```css
figure {
	display: block;
	margin-top: 1em;
	margin-bottom: 1em;
	margin-left: 40px;
	margin-right: 40px;
}
```

### references

[Figure Tag from W3Schools](https://www.w3schools.com/tags/tag_figure.asp)