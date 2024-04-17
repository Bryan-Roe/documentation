
# FlattenedImageAnalysis


## Properties

Name | Type
------------ | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema)
**id** | **string**
**ocr** | [**FlattenedOCRAnalysis**](FlattenedOCRAnalysis)
**analysis** | **string**

## Example

```typescript
import { FlattenedImageAnalysis } from '@pieces.app/pieces-os-client'

// TODO: Update the object below with actual values
const example: FlattenedImageAnalysis = {
    "schema": null,
    "id": null,
    "ocr": null,
    "analysis": null,
}

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as FlattenedImageAnalysis
console.log(exampleParsed)
```


