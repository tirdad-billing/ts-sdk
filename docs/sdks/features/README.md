# Features

## Overview

### Available Operations

* [cloneFeature](#clonefeature) - Clone a feature
* [createFeature](#createfeature) - Create feature
* [deleteFeature](#deletefeature) - Delete feature
* [queryFeature](#queryfeature) - Query features
* [updateFeature](#updatefeature) - Update feature

## cloneFeature

Clone an existing feature

### Example Usage

<!-- UsageSnippet language="typescript" operationID="cloneFeature" method="post" path="/features/{id}/clone" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.features.cloneFeature("<id>", {});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { featuresCloneFeature } from "@tirdad-ai/sdk/funcs/featuresCloneFeature.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await featuresCloneFeature(tirdad, "<id>", {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("featuresCloneFeature failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Source Feature ID                                                                                                                                                              |
| `body`                                                                                                                                                                         | [models.CloneFeatureRequest](../../sdk/models/clonefeaturerequest.md)                                                                                                          | :heavy_check_mark:                                                                                                                                                             | Clone configuration                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.FeatureResponse](../../sdk/models/featureresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400, 404, 409              | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## createFeature

Use when defining a new feature or capability to gate or meter (e.g. feature flags or usage-based limits). Ideal for boolean or usage features.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createFeature" method="post" path="/features" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.features.createFeature({
    meter: {
      aggregation: {},
      eventName: "api_request",
      name: "API Usage Meter",
      resetUsage: "NEVER",
    },
    name: "<value>",
    type: "metered",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { featuresCreateFeature } from "@tirdad-ai/sdk/funcs/featuresCreateFeature.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await featuresCreateFeature(tirdad, {
    meter: {
      aggregation: {},
      eventName: "api_request",
      name: "API Usage Meter",
      resetUsage: "NEVER",
    },
    name: "<value>",
    type: "metered",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("featuresCreateFeature failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateFeatureRequest](../../sdk/models/createfeaturerequest.md)                                                                                                        | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.FeatureResponse](../../sdk/models/featureresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## deleteFeature

Use when retiring a feature (e.g. deprecated capability). Returns 200 with success message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="deleteFeature" method="delete" path="/features/{id}" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.features.deleteFeature("<id>");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { featuresDeleteFeature } from "@tirdad-ai/sdk/funcs/featuresDeleteFeature.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await featuresDeleteFeature(tirdad, "<id>");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("featuresDeleteFeature failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Feature ID                                                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SuccessResponse](../../sdk/models/successresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400, 404                   | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## queryFeature

Use when listing or searching features (e.g. catalog or entitlement setup). Returns a paginated list; supports filtering and sorting.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="queryFeature" method="post" path="/features/search" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.features.queryFeature({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { featuresQueryFeature } from "@tirdad-ai/sdk/funcs/featuresQueryFeature.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await featuresQueryFeature(tirdad, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("featuresQueryFeature failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.FeatureFilter](../../sdk/models/featurefilter.md)                                                                                                                      | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.ListFeaturesResponse](../../sdk/models/listfeaturesresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## updateFeature

Use when changing feature definition (e.g. name, type, or meter). Request body contains the fields to update.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateFeature" method="put" path="/features/{id}" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.features.updateFeature("<id>", {});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { featuresUpdateFeature } from "@tirdad-ai/sdk/funcs/featuresUpdateFeature.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await featuresUpdateFeature(tirdad, "<id>", {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("featuresUpdateFeature failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Feature ID                                                                                                                                                                     |
| `body`                                                                                                                                                                         | [models.UpdateFeatureRequest](../../sdk/models/updatefeaturerequest.md)                                                                                                        | :heavy_check_mark:                                                                                                                                                             | Feature update data                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.FeatureResponse](../../sdk/models/featureresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400, 404                   | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |