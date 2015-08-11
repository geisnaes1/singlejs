# SingleJS

SingleJS was made to help creating "slideable" single-page websites, with mobile integration.

## How to install

`bower install singlejs --save`

or

`npm install singlejs --save`

## How to use it

```html
<div class="single">

	<div id="home">

	</div>

	<div id="skills">
		<a href="#contact">Go To Contact</a>
	</div>

	<div id="portfolio">
		<img src="img/assassin.jpg" alt="Assassins Creed" class="single-responsive" />
	</div>

	<div id="contact">

	</div>

</div>
```

And you can call the plugin like that:

```javascript
$(".single").single();
```

## Scroll effect on links

Using the `href` attribute specifying the ID of the element you want to go `CSS Style`, you can easily get a scroll effect to the targeted section of your website, see the example bellow:

```html
<a href="#contact">Go To Contact</a>
```

The link is pointing at the contact section:

```html
<div id="contact"></div>
```

## Auto-resizing images

Using the `single-responsive` class on every image the plugin will automatically add a sufix to the name of the image as the window changes it's size. You only need to have 4 different sizes of the same image available.

Let's say you have these four images: `assassin.jpg`, `assassin-md.jpg`, `assassin-sm.jpg` and `assassin-xs.jpg`. They're all optimized for smartphones, tablets and desktops. You could do this:

```html
<img src="img/assassin.jpg" class="single-responsive" />
```

And the plugin will recognize your image source and add the suffix for you.

## Plugin Defaults

```javascript
$("#single").single({
	speed: 2000,
	animation: "easeOutExpo",
	sufixes: {
		smallest: "-xs",
		small   : "-sm",
		medium  : "-md"
	}
});
```

## Inspiration

- SuperheroJS: [http://superherojs.com/](http://superherojs.com/)