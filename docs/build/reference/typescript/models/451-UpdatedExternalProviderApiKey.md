
# UpdatedExternalProvider APIKey

This is the update Auth0UserMetadata object, and the specific update output model for \"/external_provider/api_key/update\"

## Properties

Name | Type
------------ | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema)
**metadata** | [**Auth0UserMetadata**](Auth0UserMetadata)

## Example

```typescript
import { UpdatedExternalProviderApiKey } from '@pieces.app/pieces-os-client'

// TODO: Update the object below with actual values
const example: UpdatedExternalProviderApiKey = {
    "schema": null,
    "metadata": null,
}

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UpdatedExternalProviderApiKey
console.log(exampleParsed)
```


