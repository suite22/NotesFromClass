# What is an Enum
enum = enumeration

enums rock! Example use case is for days of the week.

## Playground Example Code

```
// Playground - noun: a place where people can play

import UIKit

let days = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]

func weekdayOrWeekend(dayOfWeek: String) -> String {
    
    switch dayOfWeek {
        case "Monday", "Tuesday", "Wednesday", "Thursday", "Friday":
            return "It's a weekday"
        case "Saturday", "Sunday":
            return "Yay! Party time"
    default:
            return "not a normal day"
    }
}

weekdayOrWeekend(days[0])
weekdayOrWeekend(days[6])

// code is fragile because any mispelling would throw off the whole system.

// enum would prompt for correct types

enum Day {
    // can be written with each as new lines 
    // case Monday
    // case Tuesday
    // or strung together
    // case Monday, Tuesday, etc
    // or broken into new lines for readability
    case Monday,
        Tuesday,
        Wednesday,
        Thursday,
        Friday,
        Saturday,
        Sunday
}

func weekdayOrWeekendEnum(dayOfWeek2: Day) -> String {
    
    switch dayOfWeek2 {
        // because the func knows the input is of type Day, you can use just .case instead of Day.case
    case .Monday, .Tuesday, .Wednesday, .Thursday, .Friday:
        return "Time to work dog"
        // or keep it Day.case to be more verbose
    case Day.Saturday, Day.Sunday:
        return "Go to the lake"
    }
}

weekdayOrWeekendEnum(Day.Sunday)
```