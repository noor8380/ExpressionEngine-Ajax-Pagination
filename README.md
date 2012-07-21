# ExpressionEngine Ajax Pagination

## Description
This is a jQuery plugin to make Ajax pagination in ExpressionEngine a little easier (and nicer looking!)

## How to use

### Example ExpressionEngine markup:
```html
<section id="articles">
	{exp:channel:entries channel="news" limit="10" paginate="bottom" dynamic="no"}
		<article>
			<h2>{title}</h2>
			{content}
		</article>
		{pagination}
	{/exp:channel:entries}
</section>
```

### Add Pager Javascript (don't forget jQuery!) to document
```html
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
<script src="pager/pager.min.js"></script>
<script src="pager/index.js"></script>
```

### Add Pager CSS for the kewl loading animation (all CSS-based, thanks to [Dan Eden](http://dribbble.com/shots/631496-Spinspinspin-CSS))
```html
<link href="pager.css" rel="stylesheet">
```

### Celebrate!

## Options
The plugin comes with a nice set of options you can dabble with.

```js
link:			'.pagination a',		// The anchor to your pagination links
pull:			'#articles > *',		// When your Ajax request occurs, the plugin pulls this DOM element out into the article wrapper
loaderID:		'loader',				// The ID of the loader element displayed when the Ajax request is initiated
scrollTo:		'body',					// Where the window scrolls after the next page successfully loads
fadeSpeed:		100,					// The fade speed on the loader animation and opacity changes for the article wrapper
fadeOpacity:	.5						// The opacity level on the article wrapper when the Ajax request is initiated
```

## Notes
This has only really been tested with _our_ standard ExpressionEngine pagination methods. Meaning, this may or may not work when using this with Wordpress or content management systems. Fork it and make it better! My jQuery skills are pretty n00bish.