# UpdateFeatureRequestRequest

## Example Usage

```typescript
import { UpdateFeatureRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: UpdateFeatureRequestRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `id`                                                                    | *string*                                                                | :heavy_check_mark:                                                      | Feature ID                                                              |
| `body`                                                                  | [models.UpdateFeatureRequest](../../sdk/models/updatefeaturerequest.md) | :heavy_check_mark:                                                      | Feature update data                                                     |