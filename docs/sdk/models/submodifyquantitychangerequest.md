# SubModifyQuantityChangeRequest

## Example Usage

```typescript
import { SubModifyQuantityChangeRequest } from "@tirdad-ai/sdk/sdk/models";

let value: SubModifyQuantityChangeRequest = {
  lineItems: [
    {
      id: "<id>",
      quantity: "<value>",
    },
  ],
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `lineItems`                                                                   | [models.LineItemQuantityChange](../../sdk/models/lineitemquantitychange.md)[] | :heavy_check_mark:                                                            | N/A                                                                           |