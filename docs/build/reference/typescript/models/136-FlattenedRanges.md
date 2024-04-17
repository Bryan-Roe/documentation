
# FlattenedRanges

This is a DAG-Safe minimal representation of many Ranges.

## Properties

Name | Type
------------ | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema)
**iterable** | [**Array&lt;ReferencedRange&gt;**](ReferencedRange)
**indices** | **\{ [key: string]: number; \}**
**score** | [**Score**](Score)
**continuous** | **boolean**

## Example

```typescript
import { FlattenedRanges } from '@pieces.app/pieces-os-client'

// TODO: Update the object below with actual values
const example: FlattenedRanges = {
    "schema": null,
    "iterable": null,
    "indices": null,
    "score": null,
    "continuous": null,
}

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as FlattenedRanges
console.log(exampleParsed)
```


