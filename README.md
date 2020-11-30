This is a [Hugo Components](https://gohugo.io/hugo-modules/) that packages the [Bootstrap v5](https://v5.getbootstrap.com/docs/5.0/getting-started/introduction/) SCSS source ready to be used in Hugo.

You need the Hugo extended version and Go to use this component.

Please note that Bootstrap v5 is currently in Alpha.

## Use

Add the component to your Hugo site's config:

```toml
[module]
[[module.imports]]
path = "github.com/denolteholding/hugo-mod-bootstrap-scss-v5"
```

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


## Versions

This repository is a personal fork of https://github.com/gohugoio/hugo-mod-bootstrap-scss-v4 to explore Bootstrap v5 while in Alpha.
Please refer to the original repository for proper update cycles and maintenance.
