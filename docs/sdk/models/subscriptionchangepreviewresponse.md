# SubscriptionChangePreviewResponse

Response showing the financial impact of a subscription plan change

## Example Usage

```typescript
import { SubscriptionChangePreviewResponse } from "@tirdad-ai/sdk/sdk/models";

let value: SubscriptionChangePreviewResponse = {};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `changeType`                                                                                  | [models.SubscriptionChangeType](../../sdk/models/subscriptionchangetype.md)                   | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `currentPlan`                                                                                 | [models.PlanSummary](../../sdk/models/plansummary.md)                                         | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `effectiveDate`                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | effective_date is when the change would take effect                                           |
| `metadata`                                                                                    | Record<string, *string*>                                                                      | :heavy_minus_sign:                                                                            | metadata from the request                                                                     |
| `newBillingCycle`                                                                             | [models.BillingCycleInfo](../../sdk/models/billingcycleinfo.md)                               | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `nextInvoicePreview`                                                                          | [models.InvoicePreview](../../sdk/models/invoicepreview.md)                                   | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `prorationDetails`                                                                            | [models.ProrationDetails](../../sdk/models/prorationdetails.md)                               | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `subscriptionId`                                                                              | *string*                                                                                      | :heavy_minus_sign:                                                                            | subscription_id is the ID of the subscription being changed                                   |
| `targetPlan`                                                                                  | [models.PlanSummary](../../sdk/models/plansummary.md)                                         | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `warnings`                                                                                    | *string*[]                                                                                    | :heavy_minus_sign:                                                                            | warnings contains any warnings about the change                                               |