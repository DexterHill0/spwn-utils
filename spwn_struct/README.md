# spwn-struct
C-like structs in SPWN (ish)

## How to use
Import the library like shown:
```spwn
extract import "spwn_struct"
```

The module exposes the `@struct` type.

<br>

## Usage:

### Creating the struct
```rs
let my_struct = @struct::{
	member1: @string,
	member2: @number,
}
```

### Populating the struct
```rs
let populated_struct = @struct::new({
	my_struct,

	member1: "fdf",
	member2: 10,
})
```
* The empy struct must always be provided in the call to `new`. 
* All fields must be populated, with values of the same type as defined in the struct.