
# ReferencedAsset

A reference to a asset, which at minimum must have the asset\'s id. But in the case of a hydrated client API it may have a populated reference of type Asset.

## Properties

Name | Type
------------ | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema)
**id** | **string**
**reference** | [**FlattenedAsset**](FlattenedAsset)

## Example

```typescript
import { ReferencedAsset } from '@pieces.app/pieces-os-client'

// TODO: Update the object below with actual values
const example: ReferencedAsset = {
    "schema": null,
    "id": 2254f2c8-5797-40e8-ac56-41166dc0e159,
    "reference": null,
}

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ReferencedAsset
console.log(exampleParsed)
```


