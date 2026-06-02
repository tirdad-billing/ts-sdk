# CloneFeatureRequestRequest

## Example Usage

```typescript
import { CloneFeatureRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: CloneFeatureRequestRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `id`                                                                  | *string*                                                              | :heavy_check_mark:                                                    | Source Feature ID                                                     |
| `body`                                                                | [models.CloneFeatureRequest](../../sdk/models/clonefeaturerequest.md) | :heavy_check_mark:                                                    | Clone configuration                                                   |