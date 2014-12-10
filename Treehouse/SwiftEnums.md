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

var today = Day.Monday
today = Day.Sunday
println(today)

weekdayOrWeekendEnum(Day.Sunday)


// CODE FOR CHALLENGE
enum Speed {
    case Slow,
        Medium,
        Fast
}
```

# Enum Members and Raw Values
enums create new data types

```
var today = Day.Monday
today = .Sunday
// Already knows that today is of type Day, so you can short hand the reassignment
```

Assigning raw values to enum cases

```
// Enum Members and Raw Values

enum DayRaw: Int {
    // system with automatically assign sequencial values to each member
    case Monday = 1, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday
}

func daysTillWeekend(day: DayRaw) -> Int {
    return DayRaw.Saturday.rawValue - day.rawValue
}

daysTillWeekend(DayRaw.Monday)

if let firstDayOfWeek = DayRaw(rawValue: 2) {
    daysTillWeekend(firstDayOfWeek)
}
```

start enum with Captial letter
same with each Case.

# Associated Values

# Methods or Member Functions
methods are just functions associated to a type. 
- i.e. array.removeLast() is a function that's designed to help manupulate the array, but referred to as a method.

# Initializers

# Struct Methods


