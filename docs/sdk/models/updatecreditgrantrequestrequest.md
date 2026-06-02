# UpdateCreditGrantRequestRequest

## Example Usage

```typescript
import { UpdateCreditGrantRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: UpdateCreditGrantRequestRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `id`                                                                            | *string*                                                                        | :heavy_check_mark:                                                              | Credit Grant ID                                                                 |
| `body`                                                                          | [models.UpdateCreditGrantRequest](../../sdk/models/updatecreditgrantrequest.md) | :heavy_check_mark:                                                              | Credit Grant configuration                                                      |