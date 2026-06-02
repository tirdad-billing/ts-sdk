# BulkIngestEventRequest

## Example Usage

```typescript
import { BulkIngestEventRequest } from "@tirdad-ai/sdk/sdk/models";

let value: BulkIngestEventRequest = {
  events: [
    {
      customerId: "customer456",
      eventId: "event123",
      eventName: "api_request",
      externalCustomerId: "customer456",
      properties: {
        ""response_status"": "200}",
        "{"request_size"": "100",
      },
      source: "api",
      timestamp: "2024-03-20T15:04:05Z",
    },
  ],
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `events`                                                              | [models.IngestEventRequest](../../sdk/models/ingesteventrequest.md)[] | :heavy_check_mark:                                                    | N/A                                                                   |