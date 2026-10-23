# UpdateAlertSettingsRequestRequest

## Example Usage

```typescript
import { UpdateAlertSettingsRequestRequest } from "@tirdad/sdk/sdk/models";

let value: UpdateAlertSettingsRequestRequest = {
  id: "<id>",
  body: {
    config: {},
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `id`                                                                                   | *string*                                                                               | :heavy_check_mark:                                                                     | Alert Settings ID                                                                      |
| `body`                                                                                 | [models.UpdateAlertSettingsRequest](../../sdk/models/update-alert-settings-request.md) | :heavy_check_mark:                                                                     | Alert settings                                                                         |