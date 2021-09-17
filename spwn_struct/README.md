# spwn-struct
C-like structs in SPWN (ish)

## How to use
Import the library like shown:
```spwn
extract import "spwn_struct"
```

The module exposes the `@struct` type.

<br>

## Macros:

## **n**:

> **Printed:** 
>```spwn
>(args) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _The function that creates the base struct._
>### Example: 
>```spwn
> let struct = @struct::n([
>	{ member1: @string },
>	{ member2: @number },
>])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`args`** |any | |An array of objects, where each object has a member name and type for a member in the struct. |
>

## **c**:

> **Printed:** 
>```spwn
>(struct, vals) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Populates a given struct with values that match the types of the members of that struct._
>### Example: 
>```spwn
> let struct_populated = @struct::c(x, ["member1_value", 3])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`struct`** |any | |The struct to populate. |
>| 2 | **`vals`** |any | |The values to populate the struct with. The order of the values should match the order the members were given in `struct::n`. |
>
