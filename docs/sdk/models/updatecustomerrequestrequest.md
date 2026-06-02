# UpdateCustomerRequestRequest

## Example Usage

```typescript
import { UpdateCustomerRequestRequest } from "@tirdad-ai/sdk/sdk/models";

let value: UpdateCustomerRequestRequest = {
  body: {},
};
```

## Fields

| Field                                                                     | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `id`                                                                      | *string*                                                                  | :heavy_minus_sign:                                                        | Customer ID                                                               |
| `externalCustomerId`                                                      | *string*                                                                  | :heavy_minus_sign:                                                        | Customer External ID                                                      |
| `body`                                                                    | [models.UpdateCustomerRequest](../../sdk/models/updatecustomerrequest.md) | :heavy_check_mark:                                                        | Customer                                                                  |