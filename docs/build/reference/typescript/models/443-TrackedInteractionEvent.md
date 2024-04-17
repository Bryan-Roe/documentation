
# TrackedInteractionEvent

This is a model that will hold relavent information in relation to an interaction(ONLY CLICK/TAP) analytics event(usage). If you want to register an event that relates to an interaction with the key then register a Keyboard Event. 

## Properties

Name | Type
------------ | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema)
**description** | **string**
**element** | **string**

## Example

```typescript
import { TrackedInteractionEvent } from '@pieces.app/pieces-os-client'

// TODO: Update the object below with actual values
const example: TrackedInteractionEvent = {
    "schema": null,
    "description": null,
    "element": null,
}

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TrackedInteractionEvent
console.log(exampleParsed)
```


