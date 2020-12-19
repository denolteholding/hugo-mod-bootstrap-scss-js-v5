This is a [Hugo Component](https://gohugo.io/hugo-modules/) that packages the [Bootstrap v5](https://v5.getbootstrap.com/docs/5.0/getting-started/introduction/) SCSS source and JS bundles ready to be used in Hugo.

You need the Hugo extended version and Go to use this component.

Please note that Bootstrap v5 is currently in Beta.

## Use

### Include module

Add the component to your Hugo site's config:

```toml
[module]
[[module.imports]]
path = "github.com/denolteholding/hugo-mod-bootstrap-scss-js-v5"
```

### SCSS source files

The Bootstrap SCSS will be mounted in `assets/scss/bootstrap`, so you can then import either all:

```scss
@import "bootstrap/bootstrap";
```

Or only what you need:


```scss
@import "functions";
@import "variables";
@import "mixins";
@import "utilities";
@import "root";
@import "reboot";
@import "type";
@import "images";
@import "containers";
@import "grid";
@import "tables";
@import "forms";
@import "buttons";
@import "transitions";
@import "dropdown";
@import "button-group";
@import "nav";
@import "navbar";
@import "card";
@import "accordion";
@import "breadcrumb";
@import "pagination";
@import "badge";
@import "alert";
@import "progress";
@import "list-group";
@import "close";
@import "toasts";
@import "modal";
@import "tooltip";
@import "popover";
@import "carousel";
@import "spinners";
@import "helpers";
@import "utilities/api";
```

### JS Bundles

The Bootstrap JS bundles will be mounted in `assets/js/bootstrap`. Within Hugo pages
you can import it as follows to deliver one combined JS file for your site.
```html
{{ $bootstrap := resources.Get "js/bootstrap/bootstrap.bundle.js" }}
{{ $your_js := resources.Get "js/your_js/main.js" }}
{{ $defaultJS := slice $bootstrap $your_js | resources.Concat "js/global.js" }}
{{ $globalJS := $defaultJS | resources.Minify | resources.Fingerprint }}

<script src="{{ $globalJS.Permalink }}" integrity="{{ $globalJS.Data.Integrity }}"></script>
```

## Versions

This repository is a personal fork of https://github.com/gohugoio/hugo-mod-bootstrap-scss-v4 to explore Bootstrap v5 while in Alpha.
Please refer to the original repository for proper update cycles and maintenance.
