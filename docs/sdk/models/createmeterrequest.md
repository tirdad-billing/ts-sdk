# CreateMeterRequest

## Example Usage

```typescript
import { CreateMeterRequest } from "@tirdad-ai/sdk/sdk/models";

let value: CreateMeterRequest = {
  aggregation: {},
  eventName: "api_request",
  name: "API Usage Meter",
  resetUsage: "BILLING_PERIOD",
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     | Example                                                         |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `aggregation`                                                   | [models.MeterAggregation](../../sdk/models/meteraggregation.md) | :heavy_check_mark:                                              | N/A                                                             |                                                                 |
| `eventName`                                                     | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             | api_request                                                     |
| `filters`                                                       | [models.MeterFilter](../../sdk/models/meterfilter.md)[]         | :heavy_minus_sign:                                              | N/A                                                             |                                                                 |
| `name`                                                          | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             | API Usage Meter                                                 |
| `resetUsage`                                                    | [models.ResetUsage](../../sdk/models/resetusage.md)             | :heavy_check_mark:                                              | N/A                                                             |                                                                 |