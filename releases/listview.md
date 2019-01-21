# Releases


## v5.1.1 - January, 21, 2019


### Fixes:
- [RadListView scrolling and swiping at the same time breaks the tap event](https://github.com/telerik/nativescript-ui-feedback/issues/991)

## v5.1.0

### Feature:
- [The tap event will be fired while swipeActions is true](https://github.com/telerik/nativescript-ui-feedback/issues/351)
### Fixes:
- Issue with template building

## v5.0.0 (2018, November 27)

### Braking changes
- `indicatorColor` - its type is changed from `string` to `Color`
- `indicatorBackgroundColor` - its type is changed from `string` to `Color`
- `indicatorBackgroundColor` - now applies to the entire background behind the activity indicator
Migration steps:
When setting the `indicatorColor` and `indicatorBackgroundColor` properties of the `indicatorBackgroundColor` from the code you should use the `Color` class from `tns-core-modules/color`

```
let style = new PullToRefreshStyle();
style.indicatorColor = new Color("white");
style.indicatorBackgroundColor = new Color("blue");
this.listView.pullToRefreshStyle = style;
```

### Features
- [Add support for safe areas (immersive scrolling)](https://github.com/telerik/nativescript-ui-feedback/issues/922)


### Fixes:
- [ [iOS] Assertion failure using pullToRefresh when filteringFunction is applied in iOS](https://github.com/telerik/nativescript-ui-feedback/issues/718)
- [ [iOS] App crashes when grouping is set and data is loaded async](https://github.com/telerik/nativescript-ui-feedback/issues/696)
- [ [iOS] RadListView Angular - loadMoreDataRequested crashes the app when is used with itemSelected](https://github.com/telerik/nativescript-ui-feedback/issues/429)
- [RadListView notifyPullToRefreshFinished not works](https://github.com/telerik/nativescript-ui-feedback/issues/64)
- [Using splice to remove an item while using "swipe actions" and "data operations" causes exception](https://github.com/telerik/nativescript-ui-feedback/issues/805)
- [v3.5.11 RadListView with Staggered Layout have offset applied to each item](https://github.com/telerik/nativescript-ui-feedback/issues/788)
- [ListView load-on-demand auto scroll to top](https://github.com/telerik/nativescript-ui-feedback/issues/706)
- [Vue Item Loading example sets wrong colors on items when scrolled](https://github.com/telerik/nativescript-ui-feedback/issues/905)
- [ListView: Occasional null pointer exceptions](https://github.com/telerik/nativescript-ui-feedback/issues/947)


## v4.0.0 (2018, November 20)

### Features and braking changes:
- Updated plugin dependencies
  - tns-core-modules: 5.0.0
  - angular: 7.0.0
- Vue applications running 4.2.0 requires CLI 4.2

### Fixes:
- [The header of the RadListView with async data source doesn't trigger angular event in android](https://github.com/telerik/nativescript-ui-feedback/issues/913)
- [Calling "refresh" on RadListView while using "ListViewStaggeredLayout" causes the list to go blank/apply strange offset at the begining](https://github.com/telerik/nativescript-ui-feedback/issues/853)
- [Selecting an item on Android resets scroll position to the first item](https://github.com/telerik/nativescript-ui-feedback/issues/906)
- Several vue.js fixes


## v3.8.0

### Fixes:
- [Memory leak in Angular application](https://github.com/telerik/nativescript-ui-feedback/issues/825)
- [itemDeselected: args.view is undefined (iOS only)
](https://github.com/telerik/nativescript-ui-feedback/issues/411)
- [itemTap & ItemDeselected events order inconsistency on iOS and Android](https://github.com/telerik/nativescript-ui-feedback/issues/416)
- [possible fix for Null pointer exception](https://github.com/telerik/nativescript-ui-feedback/issues/911)
- [possible fix for Null pointer exception](https://github.com/telerik/nativescript-ui-feedback/issues/863)
- [itemDeselected not called on Android](https://github.com/telerik/nativescript-ui-feedback/issues/813)

## v3.7.3

### Fixes:
- Virtualization
- [NullPointerException fix](https://github.com/telerik/nativescript-ui-feedback/issues/863)
- [ListView itemDeselected not called on Android](https://github.com/telerik/nativescript-ui-feedback/issues/813)

## v3.7.1

### Features:
- Vue watcher to refresh the list if the items change
- [Resolve an issue with disable of "load on demand" during UICollectionView creation](https://github.com/telerik/nativescript-ui-feedback/issues/674)

## v3.7.0

### Features:
- Vue support
- Provide a way to use "pull to refresh" + "load on demand" together

## v3.6.1

### Fixes:
  - [The 'index' from 'ListViewEventData' of the swipe action events is not correct while using 'groupingFunction'](https://github.com/telerik/nativescript-ui-feedback/issues/789)
  - ["bindingContext" of "swipe" View is not correct when grouping, filtering and/or sorting is enabled](https://github.com/telerik/nativescript-ui-feedback/issues/803)
  - [The "index" of elements in all events is incorrect if grouping, filtering and/or sorting is enabled](https://github.com/telerik/nativescript-ui-feedback/issues/804)

## v3.6.0

### Features:
- Support for NativeScript 4.2

### Fixes
- [RadListView on iOS to does not respect loadMoreDataRequested returnValue](https://github.com/telerik/nativescript-ui-feedback/issues/595)
- [iOS RadListView: header sizing issue when using visibility binding and an async datasource](https://github.com/telerik/nativescript-ui-feedback/issues/762)
- [Memory Consumption is high when use pullToRefresh](https://github.com/telerik/nativescript-ui-feedback/issues/717)
- [Memory leak in RadListView](https://github.com/telerik/nativescript-ui-feedback/issues/748)
- [Android: RadListView changing height of footer affects height of header](https://github.com/telerik/nativescript-ui-feedback/issues/751)
- [Busy indicator is not hidden when using 'Manual' loadOnDemandMode and there are fewer items than the screen size](https://github.com/telerik/nativescript-ui-feedback/issues/793)
  

## v3.5.11

### Fixes:
  - [Implement support for 'horizontal dynamic size' in TKListViewLayoutChangeManager](https://github.com/telerik/nativescript-ui-feedback/issues/783)
  - [Fix angular demo issue](https://github.com/telerik/nativescript-ui-feedback/issues/745)

## v3.5.10

### Fixes:
  - [Angular RadListView iOS: itemLoading and loaded event of template components triggered multiple times](https://github.com/telerik/nativescript-ui-feedback/issues/523)
  - [iOS RadListView: weird itemLoading behaviour since latest nativescript-pro-ui@3.3.0 ](https://github.com/telerik/nativescript-ui-feedback/issues/496)
  - [RadListView is slow displaying 500+ items](https://github.com/telerik/nativescript-ui-feedback/issues/641)
  - [Tapping the default group header throws exception](https://github.com/telerik/nativescript-ui-feedback/issues/712)

## v3.5.9

### Fixes:
  - Various fixes and refactoring in the native part

## v3.5.8

### Fixes:
  - [Error while using groupingFunction with Angular and webpack without 'tkGroupTemplate'](https://github.com/telerik/nativescript-ui-feedback/issues/689)
  - [RadListView : Even though selectionBehavior is 'None', item gets selected on swipe action in ios](https://github.com/telerik/nativescript-ui-feedback/issues/326)
  - [Error when trying to bind data on my radlistview](https://github.com/telerik/nativescript-ui-feedback/issues/270)
  - [ListView Header is missing on iOS](https://github.com/telerik/nativescript-ui-feedback/issues/632)
  - Update dependencies for NativeScript 4.1

## v3.5.7

### Fixes:
  - [ListView crushing on android after using onItemSelected](https://github.com/telerik/nativescript-ui-feedback/issues/530)
  - [Issue when selecting RadListView item from an angular ModalDialogService](https://github.com/telerik/nativescript-ui-feedback/issues/538)

## v3.5.5

### Fixes:
  - [Error when deleting items on multi teplates mode with header](https://github.com/telerik/nativescript-ui-feedback/issues/506)

## v3.5.3

### Fixes:
  - https://github.com/telerik/nativescript-ui-feedback/issues/581
  - https://github.com/telerik/nativescript-ui-feedback/issues/585

### New:
  - https://github.com/telerik/nativescript-ui-feedback/issues/531

## v3.5.2

### Fixes:
- iOS crash with grouping https://github.com/telerik/nativescript-ui-feedback/issues/579


## v3.5.1

### Fixes:
  - [RadListView items with async pipe can cause crash](https://github.com/telerik/nativescript-ui-feedback/issues/410)
  - [Calling `listView.getSelectedItems()` when filtering is enabled and active will not return the actual selected items](https://github.com/telerik/nativescript-ui-feedback/issues/558)


## v3.5.0

Initial Release. Matches the state from NativeScript Pro UI [v3.4.0](http://docs.telerik.com/devtools/nativescript-ui/release-notes#release-notes-340).
