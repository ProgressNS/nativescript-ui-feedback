# Releases

### 6.1.0 (2020, March, 18)

### Features:
- add two new style properties for month view in iOS only - disabledCellStyle and anotherMonthCellStyle

### 6.0.1 (2020, March, 16)

### Fixes:
- issue with Android dark mode support
- issue with iOS build - missing TNSCore.TKTheme import

### Features:
- updated plugin typings

### 6.0.0 (2019, October, 31)

### Features:
- Support dark mode for iOS and Android

### Breaking changes:

#### iOS:
- The background color of the list in which the "inline events" are rendered is changed to from `black` to `white` (in "Light mode")
- Some colors are now lighter when running in "Light mode"

## 5.0.0 (2019, July, 17)
### Features:
- Support for AndroidX
- Support for NS 6.0


## 4.1.0 (2019, June, 26)

### Features:

- [Allow custom events](https://github.com/NativeScript/nativescript-ui-feedback/issues/418)

### Fixes:

- [Cannot select multiple dates on iOS](https://github.com/NativeScript/nativescript-ui-feedback/issues/728)
- [Broken selection and alignment](https://github.com/NativeScript/nativescript-ui-feedback/issues/1065)

## 4.0.0 (2019, March, 11)

### Breaking changes:
- Add enumerations for string properties

## What is the current behavior?
1. Enum-looking properties are difficult to use, because their type is string and they are hard to guess. Example:
```
monthViewStyle.selectionShape = "Round";
```
2. Color related properties are not using the Color type, instead they are of type string. Example:
```
monthViewStyle.selectionShapeColor = "Red";
```
3. Date related properties are not using the Date type, instead they are of type string. Example:
```
calendar.minDate = "2018/02/28";
```

## What is the new behavior?
1. The enum-looking properties have their enums, so they are easier to use. Example:
```
monthViewStyle.selectionShape = CalendarSelectionShape.Round;
```
2. The Color related properties are using the type especially created for handling colors - Color:
```
monthViewStyle.selectionShapeColor = new Color("Red");
```
3. The Date related properties are using the type especially created for handling dates - Date:
```
calendar.minDate = new Date(2018, 2, 28);
```

<!-- If this PR contains a breaking change, please describe the impact and migration path for existing applications below. -->

## &#x1F534; BREAKING CHANGES &#x1F534;

1. The following enumerations are created: `CalendarFontStyle`, `CalendarViewMode`, `CalendarSelectionShape`, `CalendarSelectionMode`, `CalendarTransitionMode`, `CalendarEventsViewMode`, `CalendarCellAlignment`. They are used where appropriate. 
2. Every property that contains "color" in its name (for example: `selectionShapeColor`, `backgroundColor`, etc.) is now of type `Color` (was `string`).
3. Every property that contains "date" in its name (for example: `minDate`, `maxDate`, etc.) is now of type `Date` (was `string`).

Migration steps:
- replace every "magic string" usage with a value from the relevant enum
- replace every "Color string" usage with values of type `Color`
- replace every "Date string" usage with values of type `Date`


## 3.9.0 (2018, Oct, 2)

### Features:

- Vue extended support

## 3.8.1 (2018, Aug, 28)

### Features:

- [Calendar(iOS): Events longer than 1 day are drawn like they are one day event](https://github.com/NativeScript/nativescript-ui-feedback/issues/373)
- [Date spanning multiple days is only displayed on start date](https://github.com/NativeScript/nativescript-ui-feedback/issues/694)
- [RadCalendar extends over the elements above it](https://github.com/NativeScript/nativescript-ui-feedback/issues/606)

## 3.8.0 (2018, Aug, 16)

### Features:

- Support for NativeScript 4.2.0
- Support for java 10


## 3.7.0 (2018, july, 10)

### Features:

- [DayView - Add a property to control whether the week is visible](https://github.com/NativeScript/nativescript-ui-feedback/issues/509)

### Fixes:

- [Unable to select particular day in Calendar Day view](https://github.com/NativeScript/nativescript-ui-feedback/issues/546)

## 3.6.1

### Fixes:

- Update d.ts


## 3.6.0 (2018, april, 27)

### Features:

- Add vue support
### Fixes:

- [Day view calendar - events at the same time overlap each other](https://github.com/NativeScript/nativescript-ui-feedback/issues/414)

## v3.5.2

### Fixes
 - [Calendar: Missing hours slots for appointment in calendar dayView](https://github.com/NativeScript/nativescript-ui-feedback/issues/590)
 - [Calendar: The property displayedDate is not correctly updated](https://github.com/NativeScript/nativescript-ui-feedback/issues/589)

## v3.5.1

### Fixes:
 - [RadCalendar: Error thrown once I click on a date using viewMode="Year" and selectionMode="Range"](https://github.com/NativeScript/nativescript-ui-feedback/issues/494)


## v3.5.0

Initial Release. Matches the state from NativeScript Pro UI v3.4.0.
