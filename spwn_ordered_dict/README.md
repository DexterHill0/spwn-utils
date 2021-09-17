# spwn-ordered-dict
A dictionary that keeps the order of the keys within.

## How to use
Import the library like shown:
```spwn
extract import "spwn_ordered_dict"
```

The module exposes the `@ordereddict` type. Create a new, empty ordered dictionary:
```
let od = @ordereddict::new()
```

<br>

## Macros:

## **clone**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Creates an identical clone of the ordered dictionary._
>

## **clone\_without**:

> **Printed:** 
>```spwn
>(self, keys: @number | @string | [@number | @string]) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Create a clone of the ordered dictionary, with the provided keys removed._
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`keys`** | @number or @string or [@number or @string] | |A single key or array of keys that will be ignored when cloning the dictionary. |
>

## **combine**:

> **Printed:** 
>```spwn
>(self, extra: @ordereddict | @dictionary) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Combines another dictionary (ordered or unordered) with the current ordered dictionary._
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`extra`** | @ordereddict or @dictionary | |Combines another object with the current object. Will keep the order of the keys if an `@ordereddict` is given. |
>

## **del**:

> **Printed:** 
>```spwn
>(self, key: @number | @string) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Deletes a key from the ordered dictionary._
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`key`** | @number or @string | |The key of the element. |
>

## **del\_end**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Deletes the key at the end of the ordered dictionary._
>

## **del\_start**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Deletes the key at the start of the ordered dictionary._
>

## **get**:

> **Printed:** 
>```spwn
>(self, key: @number | @string) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Gets a key from the ordered dictionary._
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`key`** | @number or @string | |The key of the element. |
>

## **is\_empty**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns whether the ordered dictionary is empty._
>

## **items**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns the key + value pairs of the ordered dictionary._
>

## **keys**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns the keys of the ordered dictionary._
>

## **length**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns the length of the ordered dictionary._
>

## **map**:

> **Printed:** 
>```spwn
>(self, macro: @macro) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Maps key + values of the ordered dictionary._
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`macro`** | @macro | |The macro to be called. An array in the format `[key, value]` is passed as an argument. |
>

## **set**:

> **Printed:** 
>```spwn
>(self, key: @number | @string, value) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Sets a key to a value, in the ordered dictionary._
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`key`** | @number or @string | |The key of the element. |
>| 2 | **`value`** |any | |The value of the element. |
>

## **to\_kv\_array**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Equivalent to `.items()`_
>

## **to\_unordered\_dict**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Converts the ordered dictionary to a standard dictionary._
>

## **unshift**:

> **Printed:** 
>```spwn
>(self, key: @number | @string, value) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Inserts and returns a key and value to the begging of the ordered dictionary._
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`key`** | @number or @string | |The key of the element. |
>| 2 | **`value`** |any | |The value of the element. |
>

## **values**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns the values of the ordered dictionary._
>

<br>
<br>

## Operator Implementations:

## **\_as\_**:

> **Printed:** 
>```spwn
>(self, type_indicator) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`type_indicator`** |any | | |
>

## **\_display\_**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>

## **\_equal\_**:

> **Printed:** 
>```spwn
>(self, other: @ordereddict) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`other`** | @ordereddict | | |
>

## **\_has\_**:

> **Printed:** 
>```spwn
>(self, key: @number | @string) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`key`** | @number or @string | | |
>