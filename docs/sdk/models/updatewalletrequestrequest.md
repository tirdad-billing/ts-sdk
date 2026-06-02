# UpdateWalletRequestRequest

## Example Usage

```typescript
import { UpdateWalletRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: UpdateWalletRequestRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `id`                                                                  | *string*                                                              | :heavy_check_mark:                                                    | Wallet ID                                                             |
| `body`                                                                | [models.UpdateWalletRequest](../../sdk/models/updatewalletrequest.md) | :heavy_check_mark:                                                    | Update wallet request                                                 |