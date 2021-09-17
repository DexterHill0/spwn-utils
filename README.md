# spwn-pprint
Allows pretty-printing of objects within SPWN!

## How to use
Import the library like shown:
```spwn
extract import "spwn_pprint"
```

The module exposes 1 public function:
```
@pprint::print
```

>### Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`object`** | `@dictionary|@array|@macro` | |The object to pretty-print. Can be of type `@dictionary`, `@array` or `@macro` |
>| 2 | `spaces` | `@number` | `4` |The number of padding spaces to print each element with. Default is `4` |
>| 3 | `recurse_objects` | `@bool` | `true` |Will recursively loop over any nested objects and pretty print those too. Default is `true` |
>| 4 | `key_sort` | `@ASCENDING|@DESCENDING` | `@ASCENDING` |The order in which the keys of a dictionary will be sorted. Default is `@ASCENDING`. |


## Example
```
extract import "spwn_pprint"

//very gross nested object
let object = {
	key1: "string",
	key2: [1, 2, 3, {key3: @pprint::pprint}],
	key4: {key4: ["test", "test"]}
}

@pprint::print(object)
// {
//     key1: string,
//     key2:
//     [
//         1,
//         2,
//         3,
//         {
//             key3:
//             (
//                 object
//                 spaces: @number = 4
//                 recurse_objects: @bool = true
//                 key_sort = @ASCENDING
//             ),
//         },
//     ],
//     key4:
//     {
//         key4:
//         [
//             test,
//             test,
//         ],
//     },
// }
```