# UpdatePaymentStatusRequest

## Example Usage

```typescript
import { UpdatePaymentStatusRequest } from "@tirdad-ai/sdk/sdk/models";

let value: UpdatePaymentStatusRequest = {
  paymentStatus: "FAILED",
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `amount`                                                  | *string*                                                  | :heavy_minus_sign:                                        | amount is the optional payment amount to record           |
| `paymentStatus`                                           | [models.PaymentStatus](../../sdk/models/paymentstatus.md) | :heavy_check_mark:                                        | N/A                                                       |