# ChangedResources

## Example Usage

```typescript
import { ChangedResources } from "@tirdad-ai/sdk/sdk/models";

let value: ChangedResources = {
  invoices: [
    {
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
    },
  ],
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `invoices`                                                              | [models.ChangedInvoice](../../sdk/models/changedinvoice.md)[]           | :heavy_minus_sign:                                                      | N/A                                                                     |
| `lineItems`                                                             | [models.ChangedLineItem](../../sdk/models/changedlineitem.md)[]         | :heavy_minus_sign:                                                      | N/A                                                                     |
| `subscriptions`                                                         | [models.ChangedSubscription](../../sdk/models/changedsubscription.md)[] | :heavy_minus_sign:                                                      | N/A                                                                     |