# UpdateTaskStatusRequestRequest

## Example Usage

```typescript
import { UpdateTaskStatusRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: UpdateTaskStatusRequestRequest = {
  id: "<id>",
  body: {
    taskStatus: "PROCESSING",
  },
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `id`                                                                          | *string*                                                                      | :heavy_check_mark:                                                            | Task ID                                                                       |
| `body`                                                                        | [models.UpdateTaskStatusRequest](../../sdk/models/updatetaskstatusrequest.md) | :heavy_check_mark:                                                            | Status update                                                                 |