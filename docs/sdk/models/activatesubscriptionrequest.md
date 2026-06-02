# ActivateSubscriptionRequest

## Example Usage

```typescript
import { ActivateSubscriptionRequest } from "@tirdad-ai/sdk/sdk/models";

let value: ActivateSubscriptionRequest = {
  id: "<id>",
  body: {
    startDate: new Date("2026-06-29T06:09:29.151Z"),
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `id`                                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | Subscription ID                                                                                 |
| `body`                                                                                          | [models.ActivateDraftSubscriptionRequest](../../sdk/models/activatedraftsubscriptionrequest.md) | :heavy_check_mark:                                                                              | Activate Draft Subscription Request                                                             |