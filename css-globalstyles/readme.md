# CSS Default Starter / Global Styles

- Save time on project setup.
- Less lines of CSS.

## Normalize

Small CSS file that provides cross-browser consistency in the default styling of HTML elements.

Alternative/Fancier way of doing this

```css
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}
```

- Go to [Docs ](https://necolas.github.io/normalize.css/)
- Select the latest version
- Create normalize.css
- Setup the link in the html

```html
<link rel="stylesheet" href="./normalize.css" />
```

## Fonts

#### Select Fonts

- [Google Fonts](https://fonts.google.com/)
- [fontpair](https://www.fontpair.co/)
- [pagecloud](https://www.pagecloud.com/blog/best-google-fonts-pairings)

#### Grab the CSS

- [typescale](https://type-scale.com/)

## Colors

```css
:root {
	/* primary */
	/* grey */
	--black: #222;
	--white: #fff;
	--red-light: #f8d7da;
	--red-dark: #842029;
	--green-light: #d1e7dd;
	--green-dark: #0f5132;
}
```

resource: [John Smilga/ default-starter](https://github.com/john-smilga/default-starter)
