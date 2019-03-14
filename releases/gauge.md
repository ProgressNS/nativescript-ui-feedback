# Releases


### 4.0.0 (2019, March 14)

#### Breaking changes:
 - [Add enumerations for string properties](https://github.com/NativeScript/nsplugins-internal/issues/169)



## What is the current behavior?
1. Enum-looking properties are difficult to use, because their type is string and they are hard to guess. Example:
```
scaleStyle.ticksLayoutMode = "Outer";
```
2. Color related properties are not using the Color type, instead they are of type string. Example:
```
scaleStyle.lineColor = "SlateGray";
```

## What is the new behavior?
1. The enum-looking properties have their enums, so they are easier to use. Example:
```
scaleStyle.ticksLayoutMode = GaugeScaleLayoutMode.Outer;
```
2. The Color related properties are using the type especially created for handling colors - Color:
```
scaleStyle.lineColor = new Color("SlateGray");
```

Related to [this issue](https://github.com/NativeScript/nsplugins-internal/issues/169).

<!-- If this PR contains a breaking change, please describe the impact and migration path for existing applications below. -->

## &#x1F534; BREAKING CHANGES &#x1F534;

1. The following enumerations are created: `GaugeScaleLayoutMode`, `GaugeIndicatorCapMode`. They are used where appropriate. 
2. Every property that contains "color" in its name (for example: `majorTicksStrokeColor`, `lineColor`, etc.) is now of type `Color` (was `string`).

Migration steps:
- replace every "magic string" usage with a value from the relevant enum
- replace every "Color string" usage with values of type `Color`


### 3.8.0 (2018, December 20)

#### Features:
 - Support for markingMode: none
 - Support for NS 5.1

#### Fixes:
- [The colorFill parameter in the gauge plugin cannot be set by an observable for color ](https://github.com/telerik/nativescript-ui-feedback/issues/639)
- [Can't change the color of indicator on iOS](https://github.com/telerik/nativescript-ui-feedback/issues/306)


## 3.7.1

#### Fixes
- [Gauge Customization demo displays different values](https://github.com/telerik/nativescript-ui-feedback/issues/795)

## 3.7.0

#### Features
- Support for NativeScript 4.2.0

## v3.6.0

### Features:
 - Vue support.

## v3.5.0

Initial Release. Matches the state from NativeScript Pro UI [v3.4.0](http://docs.telerik.com/devtools/nativescript-ui/release-notes#release-notes-340).
