# UpdatePlanRequestRequest

## Example Usage

```typescript
import { UpdatePlanRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: UpdatePlanRequestRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `id`                                                                | *string*                                                            | :heavy_check_mark:                                                  | Plan ID                                                             |
| `body`                                                              | [models.UpdatePlanRequest](../../sdk/models/update-plan-request.md) | :heavy_check_mark:                                                  | Plan update                                                         |