# The 7-1 Architecture in Sass

In order to organize different sass files in a single project, we can use what's called a __7-1 pattern__. Which consists of 7 different folders and a single file at the root level (`main.scss`) which imports all the files to be compiled into a single stylesheet..

## The 7 Folders

The 7 different folders used in the 7-1 pattern are the following:

- `base`
- `components`
- `layout`
- `pages`
- `themes`
- `abstracts`
- `vendors`

### base
  This folder will contain the standard styling for the whole website.
  Styling would include some typographic rules, and CSS resetting styles.
  - `_base.scss`
  - `_typography.scss`
  - `_reset.scss`

### components
  Use this folder to contain all the reusable components.
  - `_button.scss`

### layout
  This folder will contain styles for the main parts of the sites. 
  - `_header.scss`
  - `_footer.scss`
  - `_sidebar.scss`
  - `_navigation.scss`

### pages
  This folder will contain styles for different pages on your website
  - `_home.scss`

### themes
  If your website contains different themes, use this folder for styling different themes
### abstracts
  This folder will contain different tools and helpers that are used across the project. 
  - `mixin.scss`
  - `variables.scss`
  - `abstract.scss`

### vendors
  If you're going to use external libraries or frameworks such as `Bootstrap` or `Faoundation`
  - `bootstrap.scss`
  - `foundation.scss`
  
## Reference
-[Sass guidelines](https://sass-guidelin.es/#the-7-1-pattern)