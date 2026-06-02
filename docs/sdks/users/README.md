# Users

## Overview

### Available Operations

* [createUser](#createuser) - Create user or service account
* [getUserInfo](#getuserinfo) - Get current user
* [queryUser](#queryuser) - Query users
* [updateUser](#updateuser) - Update current user

## createUser

Create a user account (type=user, email required; returns user + password for login) or a service account (type=service_account, roles required) for API/automation access.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createUser" method="post" path="/users" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.users.createUser({
    type: "user",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { usersCreateUser } from "@tirdad-ai/sdk/funcs/usersCreateUser.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await usersCreateUser(tirdad, {
    type: "user",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("usersCreateUser failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateUserRequest](../../sdk/models/createuserrequest.md)                                                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreateUserResponse](../../sdk/models/createuserresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## getUserInfo

Use to show the logged-in user's profile in the UI or to check permissions and roles for the current session.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getUserInfo" method="get" path="/users/me" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.users.getUserInfo();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { usersGetUserInfo } from "@tirdad-ai/sdk/funcs/usersGetUserInfo.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await usersGetUserInfo(tirdad);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("usersGetUserInfo failed:", res.error);
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

**Promise\<[models.UserResponse](../../sdk/models/userresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 401                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## queryUser

Use when listing or searching service accounts in an admin UI, or when auditing who has API access and which roles they have.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="queryUser" method="post" path="/users/search" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.users.queryUser({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { usersQueryUser } from "@tirdad-ai/sdk/funcs/usersQueryUser.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await usersQueryUser(tirdad, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("usersQueryUser failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.UserFilter](../../sdk/models/userfilter.md)                                                                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.ListUsersResponse](../../sdk/models/listusersresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## updateUser

Update the current authenticated user. Only metadata updates are supported.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateUser" method="put" path="/users/me" -->
```typescript
import { Tirdad } from "@tirdad-ai/sdk";

const tirdad = new Tirdad({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await tirdad.users.updateUser({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { TirdadCore } from "@tirdad-ai/sdk/core.js";
import { usersUpdateUser } from "@tirdad-ai/sdk/funcs/usersUpdateUser.js";

// Use `TirdadCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const tirdad = new TirdadCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await usersUpdateUser(tirdad, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("usersUpdateUser failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.UpdateUserRequest](../../sdk/models/updateuserrequest.md)                                                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.UpdateUserResponse](../../sdk/models/updateuserresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.ErrorsErrorResponse | 400                        | application/json           |
| models.ErrorsErrorResponse | 500                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |