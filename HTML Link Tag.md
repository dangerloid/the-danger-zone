---
aliases: ‹link›
tags: study
---
[[HTML]]
# HTML Link Tag

## definition and usage

The `<link>` tag defines the relationship between the current document and an external resource.

Common usage include
- linking to external [[CSS|style sheets]]
- adding a favicon

It's empty and self-closing and contains attributes only.

## attributes

attribute | value | description
-------- | ----  | ------------
crossorigin | anonymous use-credentials | specifies how the element handles cross-origin requests
href | URL | specifies the location of the linked document
hreflang | language_code | specifies the language of the text in the linked document
media | media_query | specifies on what device the linked document will be displayed
referrerpolicy | no-referrer no-referrer-when-downgrade origin origin-when-cross-origin unsafe-url | specifies which referrer to use when fetching the resource
rel | alternate author dns-prefetch help icon license next pingback preconnect prefetch preload prerender prev search stylesheet | required. specifies the relationship between the current document and the linked document
sizes | HeightxWidth any | specifies the size of the linked resource. only for rel="icon"
title| | defines a preferred or an alternate stylesheet
type | media_type | specifies the media type of the linked document

Support for [[HTML Event Attributes]] and [[HTML Global Attributes]] is available.

## examples 

```html
<head>
	<link rel="stylesheet" type="text/css" href="styles.css" />
</head>
```

[[CSS]] defaults

```css
link {
	display: none;
}
```

### references

[Link Tag from W3Schools](https://www.w3schools.com/tags/tag_link.asp)