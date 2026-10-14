<!-- Start SDK Example Usage [usage] -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.activity.listActivity({});

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->