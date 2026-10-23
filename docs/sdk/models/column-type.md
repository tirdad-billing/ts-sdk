# ColumnType

## Example Usage

```typescript
import { ColumnType } from "@tirdad/sdk/sdk/models";

let value: ColumnType = "datetime";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"string" | "decimal" | "datetime" | Unrecognized<string>
```