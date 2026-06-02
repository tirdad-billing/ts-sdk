# ListSubscriptionsResponse

## Example Usage

```typescript
import { ListSubscriptionsResponse } from "@tirdad-ai/sdk/sdk/models";

let value: ListSubscriptionsResponse = {
  items: [
    {
      latestInvoice: {
        subscription: {
          plan: {},
        },
      },
      plan: {},
    },
  ],
};
```

## Fields

| Field                                                                     | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `items`                                                                   | [models.SubscriptionResponse](../../sdk/models/subscriptionresponse.md)[] | :heavy_minus_sign:                                                        | N/A                                                                       |
| `pagination`                                                              | [models.PaginationResponse](../../sdk/models/paginationresponse.md)       | :heavy_minus_sign:                                                        | N/A                                                                       |