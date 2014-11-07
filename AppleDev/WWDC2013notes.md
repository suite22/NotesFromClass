# WWDC 2013
## Interface Builder

The initial layout is fixed by default for fast experimentation 

Intrinsic content size
- for buttons it's the text label inside

Orange border in IB means not enough constraints set

Avoid attaching constraints to the superview.
- instead try to connect to related items
-- siblings

Intermediate states
- Ambigious frames
- Conflict
- Misplaced

-- dashes show where object will be at runtime
-- update frame = change object to match constraints
--- cmd + opt + =  == keyboard shortcut