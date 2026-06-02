# PaymentStatus

## Example Usage

```typescript
import { PaymentStatus } from "@tirdad-ai/sdk/sdk/models";

let value: PaymentStatus = "OVERPAID";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"INITIATED" | "PENDING" | "PROCESSING" | "SUCCEEDED" | "OVERPAID" | "FAILED" | "REFUNDED" | "PARTIALLY_REFUNDED" | Unrecognized<string>
```