# UpdatePriceRequestRequest

## Example Usage

```typescript
import { UpdatePriceRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: UpdatePriceRequestRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `id`                                                                | *string*                                                            | :heavy_check_mark:                                                  | Price ID                                                            |
| `body`                                                              | [models.UpdatePriceRequest](../../sdk/models/updatepricerequest.md) | :heavy_check_mark:                                                  | Price configuration                                                 |