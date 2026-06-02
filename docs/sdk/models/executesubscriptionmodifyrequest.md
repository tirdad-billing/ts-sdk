# ExecuteSubscriptionModifyRequest

## Example Usage

```typescript
import { ExecuteSubscriptionModifyRequest } from "@tirdad-ai/sdk/sdk/models";

let value: ExecuteSubscriptionModifyRequest = {
  type: "grouped_invoicing",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `groupedInvoicingParams`                                                                      | [models.SubModifyGroupedInvoicingParams](../../sdk/models/submodifygroupedinvoicingparams.md) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `inheritanceParams`                                                                           | [models.SubModifyInheritanceRequest](../../sdk/models/submodifyinheritancerequest.md)         | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `quantityChangeParams`                                                                        | [models.SubModifyQuantityChangeRequest](../../sdk/models/submodifyquantitychangerequest.md)   | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `trialEndParams`                                                                              | [models.SubModifyTrialEndRequest](../../sdk/models/submodifytrialendrequest.md)               | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `type`                                                                                        | [models.SubscriptionModifyType](../../sdk/models/subscriptionmodifytype.md)                   | :heavy_check_mark:                                                                            | N/A                                                                                           |