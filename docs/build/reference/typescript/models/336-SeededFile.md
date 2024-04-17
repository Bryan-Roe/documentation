
# SeededFile

This is a base model for a File(Seeded).  We will Throw an Error, if the text and the bytes properties are both null && if both the text and bytes properties are both defined. Ensure that you pass either a text or bytes property.  bytes and string are both optionl but, if both are null or both are defined we will throw an error. So You will be required to pass one or the other, NOT both.

## Properties

Name | Type
------------ | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema)
**bytes** | [**TransferableBytes**](TransferableBytes)
**string** | [**TransferableString**](TransferableString)
**metadata** | [**FileMetadata**](FileMetadata)

## Example

```typescript
import { SeededFile } from '@pieces.app/pieces-os-client'

// TODO: Update the object below with actual values
const example: SeededFile = {
    "schema": null,
    "bytes": null,
    "string": null,
    "metadata": null,
}

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as SeededFile
console.log(exampleParsed)
```


