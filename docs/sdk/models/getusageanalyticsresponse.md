# GetUsageAnalyticsResponse

## Example Usage

```typescript
import { GetUsageAnalyticsResponse } from "@tirdad-ai/sdk/sdk/models";

let value: GetUsageAnalyticsResponse = {
  items: [
    {
      price: {
        addon: {
          prices: [
            {
              addon: {},
              meter: {
                createdAt: new Date("2024-03-20T15:04:05Z"),
                eventName: "api_request",
                id: "550e8400-e29b-41d4-a716-446655440000",
                name: "API Usage Meter",
                status: "published",
                tenantId: "tenant123",
                updatedAt: new Date("2024-03-20T15:04:05Z"),
              },
              plan: {},
            },
          ],
        },
        meter: {
          createdAt: new Date("2024-03-20T15:04:05Z"),
          eventName: "api_request",
          id: "550e8400-e29b-41d4-a716-446655440000",
          name: "API Usage Meter",
          status: "published",
          tenantId: "tenant123",
          updatedAt: new Date("2024-03-20T15:04:05Z"),
        },
        plan: {},
      },
    },
  ],
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `currency`                                                            | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `customAnalytics`                                                     | [models.CustomAnalyticItem](../../sdk/models/customanalyticitem.md)[] | :heavy_minus_sign:                                                    | N/A                                                                   |
| `items`                                                               | [models.UsageAnalyticItem](../../sdk/models/usageanalyticitem.md)[]   | :heavy_minus_sign:                                                    | N/A                                                                   |
| `totalCost`                                                           | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |