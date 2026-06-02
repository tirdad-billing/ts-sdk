# UpdateTaxAssociationRequest

## Example Usage

```typescript
import { UpdateTaxAssociationRequest } from "@tirdad-ai/sdk/sdk/models";

let value: UpdateTaxAssociationRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `id`                                                                                  | *string*                                                                              | :heavy_check_mark:                                                                    | Tax Config ID                                                                         |
| `body`                                                                                | [models.TaxAssociationUpdateRequest](../../sdk/models/taxassociationupdaterequest.md) | :heavy_check_mark:                                                                    | Tax Config Request                                                                    |