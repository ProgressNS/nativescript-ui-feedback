# Releases


## 5.1.0 (2019, August, 20)
### Feature:
- [CSS Support](https://github.com/NativeScript/nsplugins-internal/issues/193)

## 5.0.0 (2019, July, 17)
### Features:
- Support for AndroidX
- Support for NS 6.0

## 4.1.1 (2019, June 26)

### Fixes:
 - [VUE: "token" property missing in autocomplete events)](https://github.com/NativeScript/nativescript-ui-feedback/issues/1153)

## 4.1.0 (2019, June 5)

### Features:
 - [Allow passing customized Token Model](https://github.com/NativeScript/nativescript-ui-feedback/issues/65)

### Fixes:
 - [Calling js method onCreateViewHolder failed (Error: Expecting a valid View instance)](https://github.com/NativeScript/nativescript-ui-feedback/issues/855)
 - [Demo for autocomplete crash when suggest view doesn't close on navigate back](https://github.com/NativeScript/nativescript-ui-feedback/issues/1037)

## 4.0.0 (2019, March, 11)

### Breaking changes:
 - Add enumerations for string properties
 
 ## What is the current behavior?
Enum-looking properties are difficult to use, since they are hard to guess. Example:
```
this.autocomplete.displayMode = "Tokens";
```

## What is the new behavior?
These properties are of enum types, so they are easier to use. Example:
```
this.autocomplete.displayMode = AutoCompleteDisplayMode.Tokens;
```

<!-- If this PR contains a breaking change, please describe the impact and migration path for existing applications below. -->

## &#x1F534; BREAKING CHANGES &#x1F534;

The following properties of RadAutoCompleteTextView were of type string, while now they have their own enumeration and there's also a change in the casing of one of the methods so it is consistent with every other usage of `AutoComplete`:
```
    public displayMode: AutoCompleteDisplayMode;
    public completionMode: AutoCompleteCompletionMode;
    public layoutMode: AutoCompleteLayoutMode;
    public suggestMode: AutoCompleteSuggestMode;
    public resetAutoComplete: void;
```

Migration steps:
- replace every usage of the `resetAutocomplete` method with `resetAutoComplete`
- replace every setting of one of the `displayMode`, `completionMode`, `layoutMode` and `suggestMode` properties in typescript from string to a value from the respective enumerations.





## 3.11.0 (2018, December, 13)

### Features:
 - Support for NS 5.1
 - Support for markingMode: none

## 3.10.2 (2018, November, 20)

### Features:
 - Vue improvements
 
 ### Fixes:
 - [autoCompleteDisplayMode is ignored if set in the propertyAnnotations data](https://github.com/NativeScript/nativescript-ui-feedback/issues/921)

## 3.9.0 (2018, august, 17)

### Features:
 - Support for NS 4.2

### Fixes:
 - [AutoCompleteTextView SuggestionView not visible in iOS modal](https://github.com/NativeScript/nativescript-ui-feedback/issues/379)
 - [Can't populate the RadAutoCompleteTextView with a value programmatically](https://github.com/NativeScript/nativescript-ui-feedback/issues/385)

## 3.8.0 (2018, august, 8)

### Features:
 - [Enable property filteredItems on Android](https://github.com/NativeScript/nativescript-ui-feedback/issues/445)
 - [Autocomplete - Need to change the text "No Results Found"](https://github.com/NativeScript/nativescript-ui-feedback/issues/658)

### Fixes:
 - [Append mode is completing the string instead of showing hint](https://github.com/NativeScript/nativescript-ui-feedback/issues/746)
 - [AutoCompleteTextView duplicates token when navigating back to view (Android)](https://github.com/NativeScript/nativescript-ui-feedback/issues/443)
 - [Autocomplete preselected items duplicated when go in background](https://github.com/NativeScript/nativescript-ui-feedback/issues/631)
 - [Autocomplete does not work with minimumCharactersToSearch property](https://github.com/NativeScript/nativescript-ui-feedback/issues/393)
 - [Fix error when in tab view](https://github.com/NativeScript/nativescript-ui-feedback/issues/636)


## 3.7.0 (2018, april, 27)

### Features:
 - Add vue support

### Fixes:
 - [Crash on App resume w/ Error](https://github.com/NativeScript/nativescript-ui-feedback/issues/540)


## v3.6.0

### Features:
  - [AutoComplete - Implement text property and textChanged event](https://github.com/NativeScript/nativescript-ui-feedback/issues/320)

### Fixes:
  - [App crashes when typing](https://github.com/NativeScript/nativescript-ui-feedback/issues/298)
  - [AutoComplete Plain view doesn't remove tokens](https://github.com/NativeScript/nativescript-ui-feedback/issues/537)


## v3.5.0

Initial Release. Matches the state from NativeScript Pro UI v3.4.0.
