# UpdatePaymentRequestRequest

## Example Usage

```typescript
import { UpdatePaymentRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: UpdatePaymentRequestRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `id`                                                                    | *string*                                                                | :heavy_check_mark:                                                      | Payment ID                                                              |
| `body`                                                                  | [models.UpdatePaymentRequest](../../sdk/models/updatepaymentrequest.md) | :heavy_check_mark:                                                      | Payment configuration                                                   |