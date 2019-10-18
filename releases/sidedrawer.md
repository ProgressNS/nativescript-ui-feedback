# Releases

## 7.0.4 (2019, October, 18)
### Fixes:
 - [Css element selectors do not work with uglify](https://github.com/NativeScript/nativescript-ui-feedback/issues/1275)

## 7.0.3 (2019, October, 14)
### Fixes:
 - [iOS: SideDrawer 7.0.2 breaks scrolling/tapping](https://github.com/NativeScript/nativescript-ui-feedback/issues/1262)

## 7.0.2 (2019, September, 19)
### Fixes:
 - [iOS: drawerTransition is ignored](https://github.com/NativeScript/nativescript-ui-feedback/issues/1225)

## 7.0.1 (2019, September, 2)
### Fixes:
 - [iOS: Toggle Status Bar break the page's layout when using the SideDrawer](https://github.com/NativeScript/nativescript-ui-feedback/issues/1189)

## 7.0.0 (2019, July, 17)
### Features:
- Support for AndroidX
- Support for NS 6.0
- [Support safe area in nested mode](https://github.com/NativeScript/nativescript-ui-feedback/issues/1058)
### Fixes:
 - [RadSideDrawer displays margin equal to the ActionBar's height when drawerLocation is set to Bottom in xml](https://github.com/NativeScript/nativescript-ui-feedback/issues/1094)
 - [Nested RadSideDrawer have strange offset on both main content and drawer content](https://github.com/NativeScript/nativescript-ui-feedback/issues/956)
 

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
