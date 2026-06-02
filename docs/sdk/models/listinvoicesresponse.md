# ListInvoicesResponse

## Example Usage

```typescript
import { ListInvoicesResponse } from "@tirdad-ai/sdk/sdk/models";

let value: ListInvoicesResponse = {
  items: [
    {
      subscription: {
        latestInvoice: {
          subscription: {
            plan: {},
          },
        },
        plan: {},
      },
    },
  ],
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `items`                                                             | [models.InvoiceResponse](../../sdk/models/invoiceresponse.md)[]     | :heavy_minus_sign:                                                  | N/A                                                                 |
| `pagination`                                                        | [models.PaginationResponse](../../sdk/models/paginationresponse.md) | :heavy_minus_sign:                                                  | N/A                                                                 |