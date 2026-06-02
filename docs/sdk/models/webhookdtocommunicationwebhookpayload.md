# WebhookDtoCommunicationWebhookPayload

## Example Usage

```typescript
import { WebhookDtoCommunicationWebhookPayload } from "@tirdad-ai/sdk/sdk/models";

let value: WebhookDtoCommunicationWebhookPayload = {
  invoice: {
    subscription: {
      latestInvoice: {
        subscription: {
          plan: {},
        },
      },
      plan: {},
    },
  },
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `eventType`                                                     | [models.WebhookEventName](../../sdk/models/webhookeventname.md) | :heavy_minus_sign:                                              | N/A                                                             |
| `invoice`                                                       | [models.InvoiceResponse](../../sdk/models/invoiceresponse.md)   | :heavy_minus_sign:                                              | N/A                                                             |