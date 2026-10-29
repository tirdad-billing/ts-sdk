# Commitments

## Overview

### Available Operations

* [createCommitment](#createcommitment) - Create commitment
* [previewCommitment](#previewcommitment) - Preview commitment
* [queryCommitment](#querycommitment) - Query commitments
* [getCommitment](#getcommitment) - Get commitment
* [updateCommitment](#updatecommitment) - Update commitment
* [terminateCommitment](#terminatecommitment) - Terminate commitment

## createCommitment

Creates a commitment on a subscription: a minimum spend or quantity over a term, with optional committed and overage rates.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createCommitment" method="post" path="/commitments" -->
```typescript
import { Tirdad } from "@tirdad/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.commitments.createCommitment({
    endDate: new Date("2024-12-01T13:56:43.281Z"),
    measurement: "billing_period",
    name: "<value>",
    scope: {
      entityType: "group",
    },
    startDate: new Date("2026-08-30T15:34:29.816Z"),
    type: "amount",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad/sdk/core.js";
import { commitmentsCreateCommitment } from "@tirdad/sdk/funcs/commitments-create-commitment.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await commitmentsCreateCommitment(tirdad, {
    endDate: new Date("2024-12-01T13:56:43.281Z"),
    measurement: "billing_period",
    name: "<value>",
    scope: {
      entityType: "group",
    },
    startDate: new Date("2026-08-30T15:34:29.816Z"),
    type: "amount",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("commitmentsCreateCommitment failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateCommitmentRequest](../../sdk/models/create-commitment-request.md)                                                                                                | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CommitmentResponse](../../sdk/models/commitment-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400, 404                   | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## previewCommitment

Validates a commitment and returns its computed value without creating it.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="previewCommitment" method="post" path="/commitments/preview" -->
```typescript
import { Tirdad } from "@tirdad/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.commitments.previewCommitment({
    endDate: new Date("2025-03-29T18:57:47.888Z"),
    measurement: "window",
    name: "<value>",
    scope: {
      entityType: "group",
    },
    startDate: new Date("2024-09-25T08:18:25.213Z"),
    type: "amount",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad/sdk/core.js";
import { commitmentsPreviewCommitment } from "@tirdad/sdk/funcs/commitments-preview-commitment.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await commitmentsPreviewCommitment(tirdad, {
    endDate: new Date("2025-03-29T18:57:47.888Z"),
    measurement: "window",
    name: "<value>",
    scope: {
      entityType: "group",
    },
    startDate: new Date("2024-09-25T08:18:25.213Z"),
    type: "amount",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("commitmentsPreviewCommitment failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateCommitmentRequest](../../sdk/models/create-commitment-request.md)                                                                                                | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CommitmentResponse](../../sdk/models/commitment-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## queryCommitment

Lists commitments with filtering and sorting. Returns a paginated list.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="queryCommitment" method="post" path="/commitments/search" -->
```typescript
import { Tirdad } from "@tirdad/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.commitments.queryCommitment({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad/sdk/core.js";
import { commitmentsQueryCommitment } from "@tirdad/sdk/funcs/commitments-query-commitment.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await commitmentsQueryCommitment(tirdad, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("commitmentsQueryCommitment failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CommitmentFilter](../../sdk/models/commitment-filter.md)                                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.ListCommitmentsResponse](../../sdk/models/list-commitments-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## getCommitment

Loads a single commitment by ID.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getCommitment" method="get" path="/commitments/{id}" -->
```typescript
import { Tirdad } from "@tirdad/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.commitments.getCommitment("<id>");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad/sdk/core.js";
import { commitmentsGetCommitment } from "@tirdad/sdk/funcs/commitments-get-commitment.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await commitmentsGetCommitment(tirdad, "<id>");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("commitmentsGetCommitment failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Commitment ID                                                                                                                                                                  |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CommitmentResponse](../../sdk/models/commitment-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400, 404                   | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## updateCommitment

Updates the descriptive fields of a commitment. Economic terms are immutable.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateCommitment" method="put" path="/commitments/{id}" -->
```typescript
import { Tirdad } from "@tirdad/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.commitments.updateCommitment("<id>", {});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad/sdk/core.js";
import { commitmentsUpdateCommitment } from "@tirdad/sdk/funcs/commitments-update-commitment.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await commitmentsUpdateCommitment(tirdad, "<id>", {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("commitmentsUpdateCommitment failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Commitment ID                                                                                                                                                                  |
| `body`                                                                                                                                                                         | [models.UpdateCommitmentRequest](../../sdk/models/update-commitment-request.md)                                                                                                | :heavy_check_mark:                                                                                                                                                             | Commitment update                                                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CommitmentResponse](../../sdk/models/commitment-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400, 404                   | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## terminateCommitment

Ends a commitment early, effective at the given time or now.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="terminateCommitment" method="post" path="/commitments/{id}/terminate" -->
```typescript
import { Tirdad } from "@tirdad/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.commitments.terminateCommitment("<id>");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad/sdk/core.js";
import { commitmentsTerminateCommitment } from "@tirdad/sdk/funcs/commitments-terminate-commitment.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await commitmentsTerminateCommitment(tirdad, "<id>");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("commitmentsTerminateCommitment failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Commitment ID                                                                                                                                                                  |
| `body`                                                                                                                                                                         | [models.TerminateCommitmentRequest](../../sdk/models/terminate-commitment-request.md)                                                                                          | :heavy_minus_sign:                                                                                                                                                             | Termination request                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CommitmentResponse](../../sdk/models/commitment-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400, 404                   | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |