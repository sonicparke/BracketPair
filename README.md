# Bracket Pair Colorizer

This extension allows matching brackets to be identified with colours. The user can define which characters to match, and which colours to use.

Screenshot:  
![Screenshot](images/example.png "Bracket Pair Colorizer")

-----------------------------------------------------------------------------------------------------------

## Features

### User defined matching characters
> By default (), [], and {} are matched, however custom bracket characters can also be configured.

> A list of colors can be configured, as well as a specific color for orphaned brackets.

### Fast

> Bracket Pair Colorizer will only update during configurable idle time.

> Bracket Pair Colorizer will only update iterative changes to the document, caching already parsed lines.

-----------------------------------------------------------------------------------------------------------

## Settings

> `"bracketPairColorizer.timeOut"`  
Configure how long the editor should be idle for before updating the document.  
Set to 0 to disable.

> `"bracketPairColorizer.forceUniqueOpeningColor"`  
![Disabled](images/forceUniqueOpeningColorDisabled.png "forceUniqueOpeningColor Disabled")
![Enabled](images/forceUniqueOpeningColorEnabled.png "forceUniqueOpeningColor Enabled")

> `"bracketPairColorizer.forceIterationColorCycle"`  
![Enabled](images/forceIterationColorCycleEnabled.png "forceIterationColorCycle Enabled")


>`"bracketPairColorizer.colorMode"`  
Consecutive brackets share a color pool for all bracket types  
Independent brackets allow each bracket type to use its own color pool  
![Consecutive](images/consecutiveExample.png "Consecutive Example")
![Independent](images/independentExample.png "Independent Example")

> `"bracketPairColorizer.consecutivePairColors"`   
> A new bracket pair can be configured by adding it to the array.  
> Example for matching '<>'
>````
>[
>    "()",
>    "[]",
>    "{}",
>    "<>",                  // New bracket
>    [                      // CSS Color cycle
>        "Gold",
>        "Orchid",
>        "LightSkyBlue"
>    ],
>    "Red"                  // Orphaned bracket color
>]
>````

> `"bracketPairColorizer.independentPairColors"`   
> A new bracket pair can be configured by adding it to the array.  
> Example for matching '<>'
>````
>[
>    "<>",                   // New bracket
>    [                       // CSS Color cycle
>        "Gold",
>        "Orchid",
>        "LightSkyBlue"
>    ],
>    "Red"                   // Orphaned bracket color
>]
>````

-----------------------------------------------------------------------------------------------------------


## Release Notes

### 0.2.1
forceUniqueOpeningColor now works with independent color pools  
forceIterationColorCycle now works with independent color pools  

### 0.2.0
Added forceUniqueOpeningColor  
Added forceIterationColorCycle

### 0.1.1
Prevent opening brackets having same color as previous closing bracket in consecutive mode

### 0.1.0
Added consecutive bracket coloring

### 0.0.4

Fixed race condition causing a textEditor to be disposed while updating decoration.

### 0.0.3

Updated ReadMe  
Improved icon

### 0.0.2

Fixed an issue where timeout wasn't being disabled when set to 0

### 0.0.1

Initial release

-----------------------------------------------------------------------------------------------------------


