# CancelSubscriptionRequestRequest

## Example Usage

```typescript
import { CancelSubscriptionRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: CancelSubscriptionRequestRequest = {
  id: "<id>",
  body: {
    cancellationType: "scheduled_date",
  },
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `id`                                                                              | *string*                                                                          | :heavy_check_mark:                                                                | Subscription ID                                                                   |
| `body`                                                                            | [models.CancelSubscriptionRequest](../../sdk/models/cancelsubscriptionrequest.md) | :heavy_check_mark:                                                                | Cancel Subscription Request                                                       |