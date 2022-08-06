# Demo starter template (with Sass)

If you want to use Sass with Node just install:

```bash
npm i -D sass // or globaly
npm install -g sass
```

Here I use the extension of VsCode: Live Sass Compiler from Glenn Marks

## Architecture: The 7-1 Pattern

I use to go [the 7-1 pattern](https://sass-guidelin.es/#architecture): 7 folders, 1 file. Basically, you have all your partials stuffed into 7 different folders, and a single file at the root level (usually named main.scss) which imports them all to be compiled into a CSS stylesheet.

- base/
- abstracts/
- components/
- layout/
- pages/
- themes/
- vendors/

And of course:

- main.scss

---

## Main file

The main file (usually labelled `main.scss`) should be the only Sass file from the whole code base not to begin with an underscore. This file should not contain anything but `@forward` and comments.

### Reference: [Sass Guidelines](https://sass-guidelin.es/) > [Architecture](https://sass-guidelin.es/#architecture) > [Main file](https://sass-guidelin.es/#main-file)

---

## BASE FOLDER

The base/ folder holds what we might call the boilerplate code for the project. In there, you might find the reset file, some typographic rules, and probably a stylesheet defining some standard styles for commonly used HTML elements (that I like to call \_base.scss).

- `_base.scss`
- `_reset.scss`
- `_typography.scss`

---

## LAYOUT FOLDER

The layout/ folder contains everything that takes part in laying out the site or application. This folder could have stylesheets for the main parts of the site (header, footer, navigation, sidebar…), the grid system or even CSS styles for all the forms.

- `_grid.scss`
- `_header.scss`
- `_footer.scss`
- `_sidebar.scss`
- `_forms.scss`
- `_navigation.scss`

---

## COMPONENTS FOLDER

For smaller components, there is the components/ folder. While layout/ is macro (defining the global wireframe), components/ is more focused on widgets. It contains all kind of specific modules like a slider, a loader, a widget, and basically anything along those lines. There are usually a lot of files in components/ since the whole site/application should be mostly composed of tiny modules.

- `_button.scss`
- `_media.scss`
- `_carousel.scss`

The components/ folder might also be called modules/, depending on what you prefer.

---

## PAGES FOLDER

If you have page-specific styles, it is better to put them in a pages/ folder, in a file named after the page. For instance, it’s not uncommon to have very specific styles for the home page hence the need for a \_home.scss file in pages/.

- `home_.scss`
- `_contact.scss`

---

## THEMES FOLDER

On large sites and applications, it is not unusual to have different themes. There are certainly different ways of dealing with themes but I personally like having them all in a themes/ folder.

- `_theme_.scss`
- `_admin.scss`

_This is very project-specific and is likely to be non-existent on many projects._

---

## ABSTRACTS or UTILITIES FOLDER

The abstracts/ folder gathers all Sass tools and helpers used across the project. Every global variable, function, mixin and placeholder should be put in here.

The rule of thumb for this folder is that it should not output a single line of CSS when compiled on its own. These are nothing but Sass helpers.

- `_variables.scss`
- `_mixins.scss`
- `_functions.scss`
- `_placeholders.scss`

When working on a very large project with a lot of abstract utilities, it might be interesting to group them by topic rather than type, for instance typography (\_typography.scss), theming (\_theming.scss), etc. Each file contains all the related helpers: variables, functions, mixins and placeholders. Doing so can make the code easier to browse and maintain, especially when files are getting very long.

_The `abstracts/` folder might also be called `utilities/` or helpers/, depending on what you prefer._

---

## VENDORS FOLDER

And last but not least, most projects will have a vendors/ folder containing all the CSS files from external libraries and frameworks – Normalize, Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, and so on. Putting those aside in the same folder is a good way to say “Hey, this is not from me, not my code, not my responsibility”.

- `_normalize.scss`
- `_bootstrap.scss`
- `_jquery-ui.scss`
- `_select2.scss`

If you have to override a section of any vendor, I recommend you have an 8th folder called `vendors-extensions/` in which you may have files named exactly after the vendors they overwrite.

For instance, `vendors-extensions/_bootstrap.scss` is a file containing all CSS rules intended to re-declare some of Bootstrap’s default CSS. This is to avoid editing the vendor files themselves, which is generally not a good idea.
