# Changelog

## Version 2.0.0 (2025-04-03)

### Features


- new `buildCssVars` mixin, which allows generating css variables from map
- new `is-map` function, which tests whether provided variable is of type `map`
- new `buildMarginCss` mixin, which allows generating css variables for margin and css classes for margins of various sizes according provided map
- new `buildPaddingCss` mixin, which allows generating css variables for padding and css classes for paddings of various sizes according provided map
- new `buildBorderRadiusCss` mixin, which allows generating css variables for border radius and css classes for border radiuses of various sizes according provided map
- new `buildGapsCss` mixin, which allows generating css variables for gaps and css classes for gaps of various sizes according provided map
- new `buildSizes` mixin, which allows generating css variables with sizes using provided map
- new `buildFontSizeCss` mixin, which allows generating css variables for font size and css classes for font sizes of various sizes according provided map
- new `fontSizes` map scss variable, with default values for fong sizes
- updated `misc-css` mixin, now generates also `--color-transparent` css variable
- updated `getSize` function, now takes optional third parameter `fixed`, which allows function to get size in `rem` units, relative to root
- **misc**
    - new `%align-items-start` placeholder for `align-items: start;` css properties
    - new `.align-items-start` css class for `align-items: start;` css properties
    - new `%align-items-end` placeholder for `align-items: end;` css properties
    - new `.align-items-end` css class for `align-items: end;` css properties

### BREAKING CHANGES

- removed `.file-upload.input-group` css class
- updated `buildSizes` mixin
    - removed `--responsive-threshold-md` variable
    - removed `--border-radius-small`, `--border-radius-medium`, `--border-radius`, use new mixin `buildBorderRadiusCss`
    - removed `--color-transparent`, use `misc-css`
- renamed `buildSizes` mixin into `buildFixedSizes` and it take only `fontSize` as parameter
- removed `negXsWidth`, `negSmWidth`, `negMdWidth`, `negLgWidth`, `rootMinFontSize`, `rootMaxFontSize`, `rootMinFontSizeWidth`, `rootMaxFontSizeWidth`, `responsiveThresholdMd`, `borderRadiusSmall`, `borderRadius`, `borderRadiusMedium`, `dimensions`,  scss variables

## Version 1.6.0 (2024-07-29)

### Features

- **misc**
    - new `%grid-subgrid` placeholder for `display: grid; grid-template-columns: subgrid; grid-template-rows: subgrid;` css properties
    - new `.grid-subgrid` css class for `display: grid; grid-template-columns: subgrid; grid-template-rows: subgrid;` css properties
    - new `%overflow-horizontal-auto` placeholder for `overflow-x: auto;` css properties
    - new `.overflow-horizontal-auto` css class for `overflow-x: auto;` css properties
    - new `%overflow-horizontal-scroll` placeholder for `overflow-x: scroll;` css properties
    - new `.overflow-horizontal-scroll` css class for `overflow-x: scroll;` css properties

## Version 1.5.0 (2024-06-06)

### Features

- **misc**
    - new `%flex-025` placeholder for `flex: .25;`, `min-width: 0;`, `min-height: 0;` css properties
    - new `.flex-025` css class for `flex: .25;`, `min-width: 0;`, `min-height: 0;` css properties
    - new `%flex-05` placeholder for `flex: .5;`, `min-width: 0;`, `min-height: 0;` css properties
    - new `.flex-05` css class for `flex: .5;`, `min-width: 0;`, `min-height: 0;` css properties
    - new `%flex-075` placeholder for `flex: .75;`, `min-width: 0;`, `min-height: 0;` css properties
    - new `.flex-075` css class for `flex: .75;`, `min-width: 0;`, `min-height: 0;` css properties
    - new `%align-self-start` placeholder for `align-self: start;` css property
    - new `.align-self-start` css class for `align-self: start;` css property
    - new `%align-self-end` placeholder for `align-self: end;` css property
    - new `.align-self-end` css class for `align-self: end;` css property
    - new `%justify-self-stretch` placeholder for `justify-self: stretch;` css property
    - new `.justify-self-stretch` css class for `justify-self: stretch;` css property
    - new `%justify-content-stretch` placeholder for `justify-content: stretch;` css property
    - new `.justify-content-stretch` css class for `justify-content: stretch;` css property

## Version 1.4.0 (2024-06-05)

### Features

- **mixins**
    - updated `fluid-type` mixin
        - now also generates nested `.initial-zoom` css class with same calculated font size

## Version 1.3.0 (2024-06-04)

### Features

- **misc**
    - new `%root-scale` placeholder for `font-size: 1rem;` css property
    - new `.root-scale` css class for `font-size: 1rem;` css property
    - new `.reset-scale` alias css class for `.root-scale`
    - new `.reset-zoom` alias css class for `.root-scale`
- **mixins**
    - updated `buildSizes` mixin
        - now has second optional parameter which allows customization of *dimensions*
- **vars**
    - new `dimensions` map variable
        - holds all default dimensions in form of map

## Version 1.2.0 (2024-06-04)

### Bug Fixes

- fixed `%thin-scrollbar` placeholder, now using only native css not *webkit* specials
- fixed `thin-scrollbar-color` mixin, now using only native css not *webkit* specials

### Features

- **misc**
    - new `%grid-subgrid-rows` placeholder for `display: grid;`, `grid-template-rows: subgrid;` css properties
    - new `%justify-self-start` placeholder for `justify-self: start;` css property
    - new `%justify-self-end` placeholder for `justify-self: end;` css property
    - new `%justify-content-start` placeholder for `justify-content: start;` css property
    - new `%justify-content-center` placeholder for `justify-content: center;` css property
    - new `.grid-subgrid-rows` css class for `display: grid;`, `grid-template-rows: subgrid;` css properties
    - new `.justify-self-start` css class for `justify-self: start;` css property
    - new `.justify-self-end` css class for `justify-self: end;` css property
    - new `.justify-content-start` css class for `justify-content: start;` css property
    - new `.justify-content-center` css class for `justify-content: center;` css property
- **mixins**
    - updated `thin-scrollbar-color` mixin
        - new second parameter with default value (transparent) for changing scrollbar background (track)
    - updated `buildSizes` mixin
        - now also defines `--color-transparent` css variable
        - now also defines `--border-radius-small` css variable
        - now also defines `--border-radius-medium` css variable
    - new `css-reset` mixin
        - allows reseting default browser styles
- **vars**
    - new `$borderRadiusSmall` variable with `2` as value
    - new `$borderRadiusMedium` variable with `8` as value

## Version 1.1.0 (2024-05-13)

### Features

- **misc**
    - new `%white-space-normal` alias placeholder for `%content-wrap`
    - new `%white-space-nowrap` alias placeholder for `%content-nowrap`
    - new `.white-space-normal` alias css class for `.content-wrap`
    - new `.white-space-nowrap` alias css class for `.content-nowrap`
    - new `%white-space-pre` placeholder for `white-space: pre;` css property
    - new `%white-space-pre-wrap` placeholder for `white-space: pre-wrap;` css property
    - new `.white-space-pre` css class for `white-space: pre;` css property
    - new `.white-space-pre-wrap` css class for `white-space: pre-wrap;` css property


## Version 1.0.0 (2024-02-06)

### Features

- new base sets of *misc* placeholder selectors
- new `misc-css` *mixin* for generating misc styles
- new `thin-scrollbar-color` *mixin* for generating thin scrollbar css with colour vars
- new `strip-unit` *mixin* which removes unit from unitfull value
- new `getSize` *mixin* which gets relative size to font
- new `fluid-type` *mixin* which generates fluid font size
- new `buildSizes` *mixin* which generates variables for various sizes
- new *vars* for sizes and colours
