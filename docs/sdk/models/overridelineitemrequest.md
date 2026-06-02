# OverrideLineItemRequest

## Example Usage

```typescript
import { OverrideLineItemRequest } from "@tirdad-ai/sdk/sdk/models";

let value: OverrideLineItemRequest = {
  priceId: "<id>",
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `amount`                                                                                           | *string*                                                                                           | :heavy_minus_sign:                                                                                 | Amount is the new price amount that overrides the original price (optional)                        |
| `billingModel`                                                                                     | [models.BillingModel](../../sdk/models/billingmodel.md)                                            | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `priceId`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | PriceID references the plan price to override                                                      |
| `priceUnitAmount`                                                                                  | *string*                                                                                           | :heavy_minus_sign:                                                                                 | PriceUnitAmount is the amount of the price unit (for CUSTOM type, FLAT_FEE/PACKAGE billing models) |
| `priceUnitTiers`                                                                                   | [models.CreatePriceTier](../../sdk/models/createpricetier.md)[]                                    | :heavy_minus_sign:                                                                                 | PriceUnitTiers are the tiers for the price unit (for CUSTOM type, TIERED billing model)            |
| `quantity`                                                                                         | *string*                                                                                           | :heavy_minus_sign:                                                                                 | Quantity for this line item (optional)                                                             |
| `tierMode`                                                                                         | [models.BillingTier](../../sdk/models/billingtier.md)                                              | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `tiers`                                                                                            | [models.CreatePriceTier](../../sdk/models/createpricetier.md)[]                                    | :heavy_minus_sign:                                                                                 | Tiers determines the pricing tiers for this line item                                              |
| `transformQuantity`                                                                                | [models.PriceTransformQuantity](../../sdk/models/pricetransformquantity.md)                        | :heavy_minus_sign:                                                                                 | N/A                                                                                                |