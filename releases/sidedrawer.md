# Releases

## 6.0.0 (2019, March, 12)

### Breaking changes
 - Add enumerations for string properties
 
 ## What is the current behavior?
The enum-looking property `drawerLocation` is difficult to use, because its type is string and the available values are hard to guess:
```
this._sideDrawer.drawerLocation = "Left";
```

## What is the new behavior?
The `drawerLocation` property's type is `SideDrawerLocation`, so it is easier to use:
```
this._sideDrawer.drawerLocation = SideDrawerLocation.Left;
```

<!-- If this PR contains a breaking change, please describe the impact and migration path for existing applications below. -->

## &#x1F534; BREAKING CHANGES &#x1F534;

The following enumeration is created: `SideDrawerLocation`. It is used for RadSideDrawer's `drawerLocation` property. 

Migration steps:
Replace every setting of a string value to the `drawerLocation` property value, to setting a value from the `SideDrawerLocation` enumeration.



## 5.1.0 (2018, December, 17)

### Features:
 - Support for NS 5.1
 - Support for markingMode: none

## 5.0.1 (2018, Dec, 06)

### Fixes:
- [Attempt to invoke virtual method 'float android.view.MotionEvent.getX()' on a null object reference](https://github.com/NativeScript/nativescript-ui-feedback/issues/958)

## 4.3.0 (2018, Aug, 16)

### Feature:
- Support for NativeScript 4.2.0 


## v4.1.0
### Features:
- Vue support

## v4.0.0
### Breaking changes
- The `showOverNavigation` property is removed. More details and migration guide can be found in this ["article"](https://docs.nativescript.org/angular/ui/professional-ui-components/ng-SideDrawer/show-over-navi-bar#migrating-from-versions-3xx-to-the-latest-version) article.
### New
- RadSideDrawer can be used as a root element enabling it to be shared in the entire application lifecycle. More details in [this](https://docs.nativescript.org/angular/ui/professional-ui-components/ng-SideDrawer/show-over-navi-bar#share-a-single-radsidedrawer-throughout-the-entire-life-cycle-of-the-application) article.

## v3.5.2
 - [Item in RadSideDrawer does not respond](https://github.com/NativeScript/nativescript-ui-feedback/issues/575)

## v3.5.1

### Fixes:
 - [RadSideDrawer is sluggish when you open/close it slowly](https://github.com/NativeScript/nativescript-ui-feedback/issues/465)


## v3.5.0

Initial Release. Matches the state from NativeScript Pro UI v3.4.0.
