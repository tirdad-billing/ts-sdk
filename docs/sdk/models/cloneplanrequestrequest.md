# ClonePlanRequestRequest

## Example Usage

```typescript
import { ClonePlanRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: ClonePlanRequestRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `id`                                                            | *string*                                                        | :heavy_check_mark:                                              | Source Plan ID                                                  |
| `body`                                                          | [models.ClonePlanRequest](../../sdk/models/cloneplanrequest.md) | :heavy_check_mark:                                              | Clone configuration                                             |