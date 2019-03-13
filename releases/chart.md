# Releases

## v4.0.0 (2019, March, 13)

### Breaking changes: 
 - [Add enumerations for string properties](https://github.com/NativeScript/nsplugins-internal/issues/169)

## What is the current behavior?
1. Enum-looking properties are difficult to use, because their type is string and they are hard to guess. Example:
```
this._linearAxisZoom.horizontalLocation = "Left";
```
2. Color related properties are not using the Color type, instead they are of type string. Example:
```
annotation.strokeColor = "Red";
```

## What is the new behavior?
1. The enum-looking properties have their enums, so they are easier to use. Example:
```
this._linearAxisZoom.horizontalLocation = ChartAxisHorizontalLocation.Left;
```
2. The Color related properties are using the type especially created for handling colors - Color:
```
annotation.strokeColor = new Color("Red");
```

Related to [this issue](https://github.com/NativeScript/nsplugins-internal/issues/169).

<!-- If this PR contains a breaking change, please describe the impact and migration path for existing applications below. -->

## &#x1F534; BREAKING CHANGES &#x1F534;

1. The following enumerations are created: `ChartSeriesStackMode`, `ChartFontStyle`, `ChartSeriesSelectionMode`, `ChartSelectionMode`, `ChartTrackballSnapMode`, `ChartLegendPosition`, `ChartLegendOffsetOrigin`, `ChartPaletteSeriesState`, `ChartSeriesPaletteMode`, `ChartAxisLabelFitMode`, `ChartAxisLabelLayoutMode`, `ChartAxisHorizontalLocation`, `ChartAxisVerticalLocation`, `ChartAxisPlotMode`, `ChartAxisLabelVisibility`, `ChartAxisDateTimeComponent`, `ChartAnnotationZPosition`. They are used where appropriate. 
2. Every property that contains "color" in its name (for example: `strokeColor`, `fillColor`, etc.) is now of type `Color` (was `string`).

Migration steps:
- replace every "magic string" usage with a value from the relevant enum
- replace every "Color string" usage with values of type `Color`


## v3.11.1 (2018, December, 11)

### Fixes: 
 - Panbehavior listener disposed in wrong chart class

## v3.11.0 (2018, December, 7)

### Features:
 - [Option to change the fillColor for each Bar in the series](https://github.com/telerik/nativescript-ui-feedback/issues/679)
 - Support for markingMode: none

### Fixes: 
 - [Typo in the readme file](https://github.com/telerik/nativescript-ui-feedback/issues/912)


## v3.10.0 (2018, November 20)

### Features:
 - Improve Vue.js Support
 - [Add 'allowAnimations' as a chart property](https://github.com/telerik/nativescript-ui-feedback/issues/908)        

### Fixes:
 - [Missing legend info](https://github.com/telerik/nativescript-ui-feedback/issues/901)


## v3.9.1

### Fixes:
 - [RadPieChart visual discrepancy between Android and iOS](https://github.com/telerik/nativescript-ui-feedback/issues/879).
 - [Chart Legend example displays wrong Area series](https://github.com/telerik/nativescript-ui-feedback/issues/832).
 - [Chart - omitting a data point in a LineSeries crashes the app on iOS](https://github.com/telerik/nativescript-ui-feedback/issues/188).
 - [Prevent exceptions when passing null values to chart](https://github.com/telerik/nativescript-ui-feedback/issues/876).

## v3.9.0

### Fixes:
 - [iOS: labelMargin Bug on tkCartesianVerticalAxis](https://github.com/telerik/nativescript-ui-feedback/issues/505).
 - [Trackball selects more than one point incorrectly](https://github.com/telerik/nativescript-ui-feedback/issues/470).
 - [snapMode property does nothing](https://github.com/telerik/nativescript-ui-feedback/issues/818).
 - [Legend is not updated with colors from palettes](https://github.com/telerik/nativescript-ui-feedback/issues/819).

### Features:
 - [Add the ability to customize the color of the major ticks](https://github.com/telerik/nativescript-ui-feedback/issues/252)

## v3.6.1

### Fixes:
 - [DateTimeContiniousAxis with majorStep Hour and large items source freezes the app](https://github.com/telerik/nativescript-ui-feedback/issues/321).

## v3.6.0

### Fixes:
 - [Annotation no longer visible if showing/hiding chart using *ngIf on Android](https://github.com/telerik/nativescript-ui-feedback/issues/296).
 - Crash in iOS when showin/hiding a chart using visibility Angular Property.

### Features:
 - Vue support

## v3.5.0

Initial Release. Matches the state from NativeScript Pro UI [v3.4.0](http://docs.telerik.com/devtools/nativescript-ui/release-notes#release-notes-340).
