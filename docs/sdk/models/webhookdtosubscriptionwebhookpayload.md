# WebhookDtoSubscriptionWebhookPayload

## Example Usage

```typescript
import { WebhookDtoSubscriptionWebhookPayload } from "@tirdad-ai/sdk/sdk/models";

let value: WebhookDtoSubscriptionWebhookPayload = {
  subscription: {
    latestInvoice: {
      subscription: {
        plan: {},
      },
    },
    plan: {},
  },
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `eventType`                                                             | [models.WebhookEventName](../../sdk/models/webhookeventname.md)         | :heavy_minus_sign:                                                      | N/A                                                                     |
| `subscription`                                                          | [models.SubscriptionResponse](../../sdk/models/subscriptionresponse.md) | :heavy_minus_sign:                                                      | N/A                                                                     |