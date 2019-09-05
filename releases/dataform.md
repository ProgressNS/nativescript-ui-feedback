# Releases


## 5.1.0 (2019, September, 5)
### Features:
- [CSS support](https://github.com/NativeScript/nativescript-ui-feedback/issues/1202)


## 5.0.0 (2019, July, 17)
### Features:
- Support for AndroidX
- Support for NS 6.0

### v4.0.1 (2019, May 31)
#### Fixes:
- [Crash in iOS when using groups](https://github.com/NativeScript/nativescript-ui-feedback/issues/1095)

## v4.0.0 (2019, March 18)
### Fixes:
- [RadDataform DatePicker returns a timestamp when started with value](https://github.com/NativeScript/nativescript-ui-feedback/issues/942)
- [Setting a dataform property to hidden crashes android](https://github.com/NativeScript/nativescript-ui-feedback/issues/1011)

## &#x1F534; BREAKING CHANGES &#x1F534;
## What is the current behavior?
1. Enum-looking properties are difficult to use, because their type is string and they are hard to guess. Example:
```
propertyEditor.type = "Slider";
```
2. Color related properties are not using the Color type, instead they are of type string. Example:
```
property.editor.propertyEditorStyle.fillColor = "LightBlue";
```

## What is the new behavior?
1. The enum-looking properties have their enums, so they are easier to use. Example:
```
propertyEditor.type = DataFormEditorType.Slider;
```
2. The Color related properties are using the type especially created for handling colors - Color:
```
property.editor.propertyEditorStyle.fillColor = new Color("LightBlue");
```

### 3.10.0 (2018, December, 19)
#### Features:
- Support for markingMode: none
- Support for NS 5.1

#### Fixes:
- [Dataform iOS groups text gets shrunk when all groups are collapsed](https://github.com/NativeScript/nativescript-ui-feedback/issues/938)
- [RadDataForm TKPropertyEditor type decimal does not accept decimal separator iOS 11.4.1 PT-BR](https://github.com/NativeScript/nativescript-ui-feedback/issues/739)


### 3.9.1 (2018, December, 06)
#### Fixes:
- [Transfer long text on two lines, while using long text for the displayName](https://github.com/NativeScript/nativescript-ui-feedback/issues/299)


### 3.9.0 (2018, November, 20)
#### Features:
- Vue improvements

#### Fixes:
- [autoCompleteDisplayMode is ignored if set in the propertyAnnotations data](https://github.com/NativeScript/nativescript-ui-feedback/issues/921)
- [Issue while setting up groups from the metadata](https://github.com/NativeScript/nativescript-ui-feedback/issues/216)

### 3.8.0 (2018, November, 7)
#### Features:
- [Make it possible to style the RadDataForm and its editors with CSS](https://github.com/NativeScript/nativescript-ui-feedback/issues/841)

#### Fixes:
- [Date picker crash on android](https://github.com/NativeScript/nativescript-ui-feedback/issues/871)
- [Unable to create editor of type DatePicker or TimePicker, while using metadata](https://github.com/NativeScript/nativescript-ui-feedback/issues/218)
- [Time Picker Only Display UTC format](https://github.com/NativeScript/nativescript-ui-feedback/issues/533)
- [Empty array for valuesProvider crashes in iOS](https://github.com/NativeScript/nativescript-ui-feedback/issues/862)
- [iOS displayed wrong values above 100](https://github.com/NativeScript/nativescript-ui-feedback/issues/177)
- [MultilineText not working on Android](https://github.com/NativeScript/nativescript-ui-feedback/issues/877)


### 3.7.3 (2018, September, 20)
#### Fixes:

- [DatePicket source property is changed to an empty object no matter what date is selected.](https://github.com/NativeScript/nativescript-ui-feedback/issues/834)
- [DataForm: validateAll always returns false](https://github.com/NativeScript/nativescript-ui-feedback/issues/843)
- [DataForm boolean field not changing](https://github.com/NativeScript/nativescript-ui-feedback/issues/625)
- [OnValidated validates labels, not keys from valuesProvider](https://github.com/NativeScript/nativescript-ui-feedback/issues/797)


## 3.7.2 (2018, September, 18)
#### Fix

- [Editor "DatePicker" throws error when used from json 'source' and 'metadata](https://github.com/NativeScript/nativescript-ui-feedback/issues/834)

## 3.7.1 (2018, September, 12)
#### Features

- Fix: [Error when source contains nested properties, using 'ignore' in 'metadata' does not help](https://github.com/NativeScript/nativescript-ui-feedback/issues/831)


## 3.6.3 (2018, August, 17)
#### Features

- Support for NativeScript 4.2.0

## 3.6.0 (2018, april, 27)
### Features:
- Add vue support



## v3.5.0

Initial Release. Matches the state from NativeScript Pro UI v3.4.0.
