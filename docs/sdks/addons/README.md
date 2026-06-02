# Addons

## Overview

### Available Operations

* [createAddon](#createaddon) - Create addon
* [deleteAddon](#deleteaddon) - Delete addon
* [getAddon](#getaddon) - Get addon
* [getAddonByLookupKey](#getaddonbylookupkey) - Get addon by lookup key
* [queryAddon](#queryaddon) - Query addons
* [updateAddon](#updateaddon) - Update addon

## createAddon

Use when defining an optional purchasable item (e.g. extra storage or support tier). Ideal for add-ons that customers can attach to a subscription.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createAddon" method="post" path="/addons" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.addons.createAddon({
    lookupKey: "<value>",
    name: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { addonsCreateAddon } from "@tirdad-ai/sdk/funcs/addonsCreateAddon.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await addonsCreateAddon(tirdad, {
    lookupKey: "<value>",
    name: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("addonsCreateAddon failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateAddonRequest](../../sdk/models/createaddonrequest.md)                                                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreateAddonResponse](../../sdk/models/createaddonresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## deleteAddon

Use when retiring an addon (e.g. end-of-life). Returns 200 with success message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="deleteAddon" method="delete" path="/addons/{id}" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.addons.deleteAddon("<id>");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { addonsDeleteAddon } from "@tirdad-ai/sdk/funcs/addonsDeleteAddon.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await addonsDeleteAddon(tirdad, "<id>");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("addonsDeleteAddon failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Addon ID                                                                                                                                                                       |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SuccessResponse](../../sdk/models/successresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## getAddon

Use when you need to load a single addon (e.g. for display or to attach to a subscription).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getAddon" method="get" path="/addons/{id}" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.addons.getAddon("<id>");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { addonsGetAddon } from "@tirdad-ai/sdk/funcs/addonsGetAddon.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await addonsGetAddon(tirdad, "<id>");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("addonsGetAddon failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Addon ID                                                                                                                                                                       |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.AddonResponse](../../sdk/models/addonresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## getAddonByLookupKey

Use when resolving an addon by external id (e.g. from your product catalog). Ideal for integrations.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getAddonByLookupKey" method="get" path="/addons/lookup/{lookup_key}" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.addons.getAddonByLookupKey("<value>");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { addonsGetAddonByLookupKey } from "@tirdad-ai/sdk/funcs/addonsGetAddonByLookupKey.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await addonsGetAddonByLookupKey(tirdad, "<value>");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("addonsGetAddonByLookupKey failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `lookupKey`                                                                                                                                                                    | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Addon Lookup Key                                                                                                                                                               |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.AddonResponse](../../sdk/models/addonresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## queryAddon

Use when listing or searching addons (e.g. catalog or subscription builder). Returns a paginated list; supports filtering and sorting.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="queryAddon" method="post" path="/addons/search" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.addons.queryAddon({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { addonsQueryAddon } from "@tirdad-ai/sdk/funcs/addonsQueryAddon.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await addonsQueryAddon(tirdad, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("addonsQueryAddon failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.AddonFilter](../../sdk/models/addonfilter.md)                                                                                                                          | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.ListAddonsResponse](../../sdk/models/listaddonsresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## updateAddon

Use when changing addon details (e.g. name, pricing, or metadata).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateAddon" method="put" path="/addons/{id}" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.addons.updateAddon("<id>", {});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { addonsUpdateAddon } from "@tirdad-ai/sdk/funcs/addonsUpdateAddon.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await addonsUpdateAddon(tirdad, "<id>", {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("addonsUpdateAddon failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Addon ID                                                                                                                                                                       |
| `body`                                                                                                                                                                         | [models.UpdateAddonRequest](../../sdk/models/updateaddonrequest.md)                                                                                                            | :heavy_check_mark:                                                                                                                                                             | Update Addon Request                                                                                                                                                           |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.AddonResponse](../../sdk/models/addonresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |