# PreviewSubscriptionModifyRequest

## Example Usage

```typescript
import { PreviewSubscriptionModifyRequest } from "@tirdad-ai/sdk/sdk/models";

let value: PreviewSubscriptionModifyRequest = {
  id: "<id>",
  body: {
    type: "grouped_invoicing",
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `id`                                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | Subscription ID                                                                                 |
| `body`                                                                                          | [models.ExecuteSubscriptionModifyRequest](../../sdk/models/executesubscriptionmodifyrequest.md) | :heavy_check_mark:                                                                              | Modification preview request                                                                    |