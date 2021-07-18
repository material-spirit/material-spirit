# material-spirit/breakpoints

## Usage

``` scss

@use 'material-spirit/breakpoints' as bp;

@include bp.media-query(tablet) {
  .my-class {
    color: red;
  }
}
```

Available [breakpoints](https://material.angular.io/cdk/layout/overview):
* handset
* tablet
* web
* --
* tablet-down
* tablet-up
* --
* handset-portrait
* handset-landscape
* tablet-portrait
* tablet-landscape
* web-portrait
* web-landscape
* --
* xs
* sm
* md
* lg
* xl


All these breakpoints are available via mixin `bp.media-query()`. Breakpoint-specific styles are compiled only for subset of breakpoints. The subset is defined by `bp.$compile-breakpoints` variable. By default the subset is:

* handset
* tablet
* web


## Customization

Customize breakpoints like this:

``` scss
@use 'material-spirit/breakpoints' as bp with (
    $breakpoints: (
        phone: '<media query>',
        tablet: '<media query>',
        desktop: '<media query>'
    )
);
```

Or use predefined breakpoint sets from `material-spirit/bp-presets`;