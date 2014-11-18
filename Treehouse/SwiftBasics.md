let = constant instead of a mutable variable

\ = backslash allows inline variables with strings
- string interpolation
- var example = "\(varInline) this is an inline example."

unary operator = var++
- post-fix = var++
- pre-fix = ++var
- !var = negates value of a bool

* option + click in Xcode for inline documentation 

dictionaries are unordered

while loop
- increment index after main body of loop

do {
	// runs at least once	
} while condition

# Functions
to include the type required for an argument use:
- func calcArea(height: Int, width: Int) { }

# Named Parameters
include the label name for the parameter when setting up the arguments for the function.
func calculateArea(#height: Int, #width: Int) -> Int {
	return height * width
}

# Tuples
n-tuple

func searchNames (#name: String) -> Bool {
	let names = ["Amit"]

	var found = (false, "\(name) is not a treehouse teacher")

	for n in names {
		if n == name {
			found = (true, "\(name) is a Treehouse teacher")
		}
	}

	return found
}

searchNames(name: "John")		-> false
searchNames(name: "Amit")		-> (.0 true, .1 "Amit is a Treehouse teacher")

result.0 				-> false

## Decomposing a Tuple

let (found, description) = searchNames(name: "Jon")

or use an understore to ignore a tuple value

found 			-> false

func searchNames (#name: String) -> (found: Bool, description: String)

name the returns from the func and give them labels just like arguments into the func

let result = searchNames(name: "Amit")
result.found 			-> true
result.description 		-> as as previous

# Optionals
can have value or nil

if let statement to safely unwrap.

## Optional Chaining
if let culprit = findApt("101")?.toInt() {
	sendNoticeTo(aptNumber: culprit)
}

the ?.toInt() removes the need for another layer of if let statements that would safely unwrap the optional.

## Exercise: isDivisible function