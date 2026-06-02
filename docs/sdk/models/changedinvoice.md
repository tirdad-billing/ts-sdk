# ChangedInvoice

## Example Usage

```typescript
import { ChangedInvoice } from "@tirdad-ai/sdk/sdk/models";

let value: ChangedInvoice = {
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

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `action`                                                                                                            | [models.ChangedInvoiceAction](../../sdk/models/changedinvoiceaction.md)                                             | :heavy_minus_sign:                                                                                                  | created (proration invoice) \| wallet_credit (downgrade credit)                                                     |
| `id`                                                                                                                | *string*                                                                                                            | :heavy_minus_sign:                                                                                                  | N/A                                                                                                                 |
| `invoice`                                                                                                           | [models.InvoiceResponse](../../sdk/models/invoiceresponse.md)                                                       | :heavy_minus_sign:                                                                                                  | N/A                                                                                                                 |
| `status`                                                                                                            | [models.ChangedInvoiceStatus](../../sdk/models/changedinvoicestatus.md)                                             | :heavy_minus_sign:                                                                                                  | preview \| issued \| INITIATED \| PENDING \| PROCESSING \| SUCCEEDED \| OVERPAID \| FAILED \| REFUNDED \| PARTIALLY_REFUNDED |
| `walletTransaction`                                                                                                 | [models.WalletTransactionResponse](../../sdk/models/wallettransactionresponse.md)                                   | :heavy_minus_sign:                                                                                                  | N/A                                                                                                                 |