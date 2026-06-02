# AlertLogResponse

## Example Usage

```typescript
import { AlertLogResponse } from "@tirdad-ai/sdk/sdk/models";

let value: AlertLogResponse = {
  feature: {
    meter: {
      createdAt: new Date("2024-03-20T15:04:05Z"),
      eventName: "api_request",
      id: "550e8400-e29b-41d4-a716-446655440000",
      name: "API Usage Meter",
      status: "published",
      tenantId: "tenant123",
      updatedAt: new Date("2024-03-20T15:04:05Z"),
    },
  },
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `alertInfo`                                                                                   | [models.AlertInfo](../../sdk/models/alertinfo.md)                                             | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `alertStatus`                                                                                 | [models.AlertState](../../sdk/models/alertstate.md)                                           | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `alertType`                                                                                   | [models.AlertType](../../sdk/models/alerttype.md)                                             | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `createdBy`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `customer`                                                                                    | [models.CustomerResponse](../../sdk/models/customerresponse.md)                               | :heavy_minus_sign:                                                                            | Customer response object containing all customer information                                  |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `entityId`                                                                                    | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `entityType`                                                                                  | [models.AlertEntityType](../../sdk/models/alertentitytype.md)                                 | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `environmentId`                                                                               | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `feature`                                                                                     | [models.FeatureResponse](../../sdk/models/featureresponse.md)                                 | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `parentEntityId`                                                                              | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `parentEntityType`                                                                            | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `status`                                                                                      | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `tenantId`                                                                                    | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `updatedBy`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `wallet`                                                                                      | [models.WalletResponse](../../sdk/models/walletresponse.md)                                   | :heavy_minus_sign:                                                                            | N/A                                                                                           |