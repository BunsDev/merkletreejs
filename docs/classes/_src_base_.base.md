[merkletreejs](../README.md) › [Globals](../globals.md) › ["src/Base"](../modules/_src_base_.md) › [Base](_src_base_.base.md)

# Class: Base

## Hierarchy

* **Base**

  ↳ [IncrementalMerkleTree](_src_incrementalmerkletree_.incrementalmerkletree.md)

  ↳ [MerkleMountainRange](_src_merklemountainrange_.merklemountainrange.md)

  ↳ [MerkleRadixTree](_src_merkleradixtree_.merkleradixtree.md)

  ↳ [MerkleSumTree](_src_merklesumtree_.merklesumtree.md)

  ↳ [MerkleTree](_src_merkletree_.merkletree.md)

## Index

### Methods

* [bigNumberify](_src_base_.base.md#bignumberify)
* [binarySearch](_src_base_.base.md#binarysearch)
* [bufferArrayIncludes](_src_base_.base.md#bufferarrayincludes)
* [bufferIndexOf](_src_base_.base.md#protected-bufferindexof)
* [bufferToHex](_src_base_.base.md#buffertohex)
* [bufferify](_src_base_.base.md#bufferify)
* [bufferifyFn](_src_base_.base.md#bufferifyfn)
* [isHexString](_src_base_.base.md#protected-ishexstring)
* [linearSearch](_src_base_.base.md#linearsearch)
* [log2](_src_base_.base.md#protected-log2)
* [print](_src_base_.base.md#print)
* [zip](_src_base_.base.md#protected-zip)
* [bigNumberify](_src_base_.base.md#static-bignumberify)
* [binarySearch](_src_base_.base.md#static-binarysearch)
* [bufferToHex](_src_base_.base.md#static-buffertohex)
* [bufferify](_src_base_.base.md#static-bufferify)
* [bufferifyFn](_src_base_.base.md#static-bufferifyfn)
* [hexZeroPad](_src_base_.base.md#static-hexzeropad)
* [isHexString](_src_base_.base.md#static-ishexstring)
* [linearSearch](_src_base_.base.md#static-linearsearch)
* [print](_src_base_.base.md#static-print)

## Methods

###  bigNumberify

▸ **bigNumberify**(`value`: any): *BigInt*

**Parameters:**

Name | Type |
------ | ------ |
`value` | any |

**Returns:** *BigInt*

___

###  binarySearch

▸ **binarySearch**(`array`: Buffer[], `element`: Buffer, `compareFunction`: function): *number*

binarySearch

**`desc`** Returns the first index of which given item is found in array using binary search.

**`example`** 
```js
const index = tree.binarySearch(array, element, Buffer.compare)
```

**Parameters:**

▪ **array**: *Buffer[]*

Array of items.

▪ **element**: *Buffer*

Item to find.

▪ **compareFunction**: *function*

▸ (`a`: unknown, `b`: unknown): *number*

**Parameters:**

Name | Type |
------ | ------ |
`a` | unknown |
`b` | unknown |

**Returns:** *number*

- Index number

___

###  bufferArrayIncludes

▸ **bufferArrayIncludes**(`bufferArray`: Buffer[], `targetBuffer`: Buffer): *boolean*

**Parameters:**

Name | Type |
------ | ------ |
`bufferArray` | Buffer[] |
`targetBuffer` | Buffer |

**Returns:** *boolean*

___

### `Protected` bufferIndexOf

▸ **bufferIndexOf**(`array`: Buffer[], `element`: Buffer, `isSorted`: boolean): *number*

bufferIndexOf

**`desc`** Returns the first index of which given buffer is found in array.

**`example`** 
```js
const index = tree.bufferIndexOf(haystack, needle)
```

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`array` | Buffer[] | - |
`element` | Buffer | - |
`isSorted` | boolean | false |

**Returns:** *number*

- Index number

___

###  bufferToHex

▸ **bufferToHex**(`value`: Buffer, `withPrefix`: boolean): *string*

bufferToHex

**`desc`** Returns a hex string with 0x prefix for given buffer.

**`example`** 
```js
const hexStr = tree.bufferToHex(Buffer.from('A'))
```

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`value` | Buffer | - |
`withPrefix` | boolean | true |

**Returns:** *string*

___

###  bufferify

▸ **bufferify**(`value`: any): *Buffer*

bufferify

**`desc`** Returns a buffer type for the given value.

**`example`** 
```js
const buf = tree.bufferify('0x1234')
```

**Parameters:**

Name | Type |
------ | ------ |
`value` | any |

**Returns:** *Buffer*

___

###  bufferifyFn

▸ **bufferifyFn**(`f`: any): *any*

bufferifyFn

**`desc`** Returns a function that will bufferify the return value.

**`example`** 
```js
const fn = tree.bufferifyFn((value) => sha256(value))
```

**Parameters:**

Name | Type |
------ | ------ |
`f` | any |

**Returns:** *any*

___

### `Protected` isHexString

▸ **isHexString**(`value`: string): *boolean*

isHexString

**`desc`** Returns true if value is a hex string.

**`example`** 
```js
console.log(MerkleTree.isHexString('0x1234'))
```

**Parameters:**

Name | Type |
------ | ------ |
`value` | string |

**Returns:** *boolean*

___

###  linearSearch

▸ **linearSearch**(`array`: Buffer[], `element`: Buffer, `eqChecker`: function): *number*

linearSearch

**`desc`** Returns the first index of which given item is found in array using linear search.

**`example`** 
```js
const index = tree.linearSearch(array, element, (a, b) => a === b)
```

**Parameters:**

▪ **array**: *Buffer[]*

Array of items.

▪ **element**: *Buffer*

Item to find.

▪ **eqChecker**: *function*

▸ (`a`: unknown, `b`: unknown): *boolean*

**Parameters:**

Name | Type |
------ | ------ |
`a` | unknown |
`b` | unknown |

**Returns:** *number*

- Index number

___

### `Protected` log2

▸ **log2**(`n`: number): *number*

log2

**`desc`** Returns the log2 of number.

**Parameters:**

Name | Type |
------ | ------ |
`n` | number |

**Returns:** *number*

___

###  print

▸ **print**(): *void*

print

**`desc`** Prints out a visual representation of the merkle tree.

**`example`** 
```js
tree.print()
```

**Returns:** *void*

___

### `Protected` zip

▸ **zip**(`a`: any[], `b`: any[]): *any[][]*

zip

**`desc`** Returns true if value is a hex string.

**`example`** 
```js
const zipped = tree.zip(['a', 'b'],['A', 'B'])
console.log(zipped) // [ [ 'a', 'A' ], [ 'b', 'B' ] ]
```

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`a` | any[] | first array |
`b` | any[] | second array |

**Returns:** *any[][]*

___

### `Static` bigNumberify

▸ **bigNumberify**(`value`: any): *BigInt*

**Parameters:**

Name | Type |
------ | ------ |
`value` | any |

**Returns:** *BigInt*

___

### `Static` binarySearch

▸ **binarySearch**(`array`: Buffer[], `element`: Buffer, `compareFunction`: function): *number*

binarySearch

**`desc`** Returns the first index of which given item is found in array using binary search.

**`example`** 
```js
const index = MerkleTree.binarySearch(array, element, Buffer.compare)
```

**Parameters:**

▪ **array**: *Buffer[]*

Array of items.

▪ **element**: *Buffer*

Item to find.

▪ **compareFunction**: *function*

▸ (`a`: unknown, `b`: unknown): *number*

**Parameters:**

Name | Type |
------ | ------ |
`a` | unknown |
`b` | unknown |

**Returns:** *number*

- Index number

___

### `Static` bufferToHex

▸ **bufferToHex**(`value`: Buffer, `withPrefix`: boolean): *string*

bufferToHex

**`desc`** Returns a hex string with 0x prefix for given buffer.

**`example`** 
```js
const hexStr = MerkleTree.bufferToHex(Buffer.from('A'))
```

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`value` | Buffer | - |
`withPrefix` | boolean | true |

**Returns:** *string*

___

### `Static` bufferify

▸ **bufferify**(`value`: any): *Buffer*

bufferify

**`desc`** Returns a buffer type for the given value.

**`example`** 
```js
const buf = MerkleTree.bufferify('0x1234')
```

**Parameters:**

Name | Type |
------ | ------ |
`value` | any |

**Returns:** *Buffer*

___

### `Static` bufferifyFn

▸ **bufferifyFn**(`f`: any): *any*

bufferifyFn

**`desc`** Returns a function that will bufferify the return value.

**`example`** 
```js
const fn = MerkleTree.bufferifyFn((value) => sha256(value))
```

**Parameters:**

Name | Type |
------ | ------ |
`f` | any |

**Returns:** *any*

___

### `Static` hexZeroPad

▸ **hexZeroPad**(`hexStr`: string, `length`: number): *string*

**Parameters:**

Name | Type |
------ | ------ |
`hexStr` | string |
`length` | number |

**Returns:** *string*

___

### `Static` isHexString

▸ **isHexString**(`v`: string): *boolean*

isHexString

**`desc`** Returns true if value is a hex string.

**`example`** 
```js
console.log(MerkleTree.isHexString('0x1234'))
```

**Parameters:**

Name | Type |
------ | ------ |
`v` | string |

**Returns:** *boolean*

___

### `Static` linearSearch

▸ **linearSearch**(`array`: Buffer[], `element`: Buffer, `eqChecker`: function): *number*

linearSearch

**`desc`** Returns the first index of which given item is found in array using linear search.

**`example`** 
```js
const index = MerkleTree.linearSearch(array, element, (a, b) => a === b)
```

**Parameters:**

▪ **array**: *Buffer[]*

Array of items.

▪ **element**: *Buffer*

Item to find.

▪ **eqChecker**: *function*

▸ (`a`: unknown, `b`: unknown): *boolean*

**Parameters:**

Name | Type |
------ | ------ |
`a` | unknown |
`b` | unknown |

**Returns:** *number*

- Index number

___

### `Static` print

▸ **print**(`tree`: any): *void*

print

**`desc`** Prints out a visual representation of the given merkle tree.

**`example`** 
```js
MerkleTree.print(tree)
```

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`tree` | any | Merkle tree instance. |

**Returns:** *void*
