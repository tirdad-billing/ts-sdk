# WebhookDtoWalletWebhookPayload

## Example Usage

```typescript
import { WebhookDtoWalletWebhookPayload } from "@tirdad-ai/sdk/sdk/models";

let value: WebhookDtoWalletWebhookPayload = {};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `alert`                                                                           | [models.WebhookDtoWalletAlertInfo](../../sdk/models/webhookdtowalletalertinfo.md) | :heavy_minus_sign:                                                                | N/A                                                                               |
| `customer`                                                                        | [models.CustomerResponse](../../sdk/models/customerresponse.md)                   | :heavy_minus_sign:                                                                | Customer response object containing all customer information                      |
| `eventType`                                                                       | [models.WebhookEventName](../../sdk/models/webhookeventname.md)                   | :heavy_minus_sign:                                                                | N/A                                                                               |
| `wallet`                                                                          | [models.WalletResponse](../../sdk/models/walletresponse.md)                       | :heavy_minus_sign:                                                                | N/A                                                                               |