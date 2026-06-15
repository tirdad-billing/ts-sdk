# Integrations

## Overview

### Available Operations

* [getIntegrationConfig](#getintegrationconfig) - Get integration configurations
* [linkIntegrationMapping](#linkintegrationmapping) - Link integration mapping
* [delinkIntegrationMapping](#delinkintegrationmapping) - Delink integration mapping
* [getEntityIntegrationMappings](#getentityintegrationmappings) - Get entity integration mappings

## getIntegrationConfig

Returns the base capabilities and current sync configuration for all connected providers.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getIntegrationConfig" method="get" path="/integrations/config" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.integrations.getIntegrationConfig();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { integrationsGetIntegrationConfig } from "@tirdad-ai/sdk/funcs/integrations-get-integration-config.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await integrationsGetIntegrationConfig(tirdad);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("integrationsGetIntegrationConfig failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.IntegrationConfigResponse](../../sdk/models/integration-config-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## linkIntegrationMapping

Link a Tirdad entity to provider entity with provider-specific side effects.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="linkIntegrationMapping" method="post" path="/integrations/link" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.integrations.linkIntegrationMapping({
    entityId: "<id>",
    entityType: "item_price",
    providerEntityId: "<id>",
    providerType: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { integrationsLinkIntegrationMapping } from "@tirdad-ai/sdk/funcs/integrations-link-integration-mapping.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await integrationsLinkIntegrationMapping(tirdad, {
    entityId: "<id>",
    entityType: "item_price",
    providerEntityId: "<id>",
    providerType: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("integrationsLinkIntegrationMapping failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.LinkIntegrationMappingRequest](../../sdk/models/link-integration-mapping-request.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.LinkIntegrationMappingResponse](../../sdk/models/link-integration-mapping-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## delinkIntegrationMapping

Soft-delete (archive) the mapping between a Tirdad entity and a provider entity.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="delinkIntegrationMapping" method="delete" path="/integrations/link" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.integrations.delinkIntegrationMapping({
    entityId: "<id>",
    entityType: "item_price",
    providerType: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { integrationsDelinkIntegrationMapping } from "@tirdad-ai/sdk/funcs/integrations-delink-integration-mapping.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await integrationsDelinkIntegrationMapping(tirdad, {
    entityId: "<id>",
    entityType: "item_price",
    providerType: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("integrationsDelinkIntegrationMapping failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.DelinkIntegrationMappingRequest](../../sdk/models/delink-integration-mapping-request.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SuccessResponse](../../sdk/models/success-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400, 404                   | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## getEntityIntegrationMappings

Get integration mappings for a specific entity by entity type and entity ID.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getEntityIntegrationMappings" method="get" path="/integrations/mappings" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.integrations.getEntityIntegrationMappings("<value>", "<id>");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { integrationsGetEntityIntegrationMappings } from "@tirdad-ai/sdk/funcs/integrations-get-entity-integration-mappings.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await integrationsGetEntityIntegrationMappings(tirdad, "<value>", "<id>");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("integrationsGetEntityIntegrationMappings failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `entityType`                                                                                                                                                                   | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Entity type (customer, plan, invoice, subscription, payment, credit_note, addon, item, item_price, price)                                                                      |
| `entityId`                                                                                                                                                                     | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | Entity ID                                                                                                                                                                      |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.ListEntityIntegrationMappingsResponse](../../sdk/models/list-entity-integration-mappings-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |