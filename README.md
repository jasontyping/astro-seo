![Astro SEO Logo](https://user-images.githubusercontent.com/5182256/131216951-8f74f425-f775-463d-a11b-0e01ad9fce8d.png)

# 🚀 Astro SEO

This [Astro](https://astro.build/) component makes it easy to add tags that are
relevant for seach engine optimization (SEO) to your pages.

Currently it's __very__ early in development. The ultimate goal is to make this
the one-stop shop for most of your SEO needs when developing Astro sites.

Pull requests and/or feature requests are very welcome!

## How To Use

In any of your Astro pages, import Astro SEO and then use the component inside
the `<head>` section of your HTML:

```jsx
---
import { SEO } from 'astro-seo'
---

<html lang="en">
	<head>
		<SEO 
			title="A Very Descriptive Title"
			description="A heavily optimized description full of well-researched keywords."
		/>
	</head>
	// ... rest of <head>

	<body>
		// ... body
	</body>
</html>
```

## Supported Props

Propname | Type | Description
------------ | ------------- | -------------
title | string | The title of the page.
description | string | Text that gives a concise description of what your page is about.
canoncial | string | Prevent duplicate content issues by specifying the "canonical" or "preferred" url of a web page.

## Goals

Our first goal for this project is to support the most-used tags that are
relevant for SEO. That includes the most-used open graph tags.

After that comes feature-parity with Next SEO. After _that_ ... we'll see.

## What does this component do, exactly?

There's certainly no magic to what Astro SEO does. Basically, it bundles the
creation of regular SEO-relevant HTML tags inside one component that you can
then use inside your page's `<head>` tag.

The translation between props and tags is pretty direct and almost 1:1. After 
building, there probably won't be anything you wouldn't have written yourself.
The idea is to surface the options that exist in a central place and adhere to 
best practices where it's theoretically possible not to. __If you want to see 
how the sausage gets made, there's only one place you will have to check__: 
`/src/SEO.astro`

If you want, you can view Astro SEO as a checklist, so you don't forget a tag.
Or maybe also as an educational tool, to see which options exist in the first 
place.

## Acknowledgements

Astro SEO is _heavily_ inspired by [Next SEO](https://github.com/garmeeh/next-seo)
and all the amazing work Gary is doing developing it. Thanks Gary! ❤️