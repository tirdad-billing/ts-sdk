# TopUpWalletResponse

## Example Usage

```typescript
import { TopUpWalletResponse } from "@tirdad-ai/sdk/sdk/models";

let value: TopUpWalletResponse = {};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `invoiceId`                                                                       | *string*                                                                          | :heavy_minus_sign:                                                                | Invoice ID if an invoice was created (only for PURCHASED_CREDIT_INVOICED)         |
| `wallet`                                                                          | [models.WalletResponse](../../sdk/models/walletresponse.md)                       | :heavy_minus_sign:                                                                | N/A                                                                               |
| `walletTransaction`                                                               | [models.WalletTransactionResponse](../../sdk/models/wallettransactionresponse.md) | :heavy_minus_sign:                                                                | N/A                                                                               |