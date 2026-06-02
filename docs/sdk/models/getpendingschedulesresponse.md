# GetPendingSchedulesResponse

List of pending schedules for a subscription

## Example Usage

```typescript
import { GetPendingSchedulesResponse } from "@tirdad-ai/sdk/sdk/models";

let value: GetPendingSchedulesResponse = {};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `count`                                                                                   | *number*                                                                                  | :heavy_minus_sign:                                                                        | count is the number of pending schedules                                                  |
| `schedules`                                                                               | [models.SubscriptionScheduleResponse](../../sdk/models/subscriptionscheduleresponse.md)[] | :heavy_minus_sign:                                                                        | schedules is the list of pending schedules                                                |