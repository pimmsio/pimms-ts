# EmbedTokens
(*embedTokens*)

## Overview

### Available Operations

* [referrals](#referrals) - Create a new referrals embed token

## referrals

Create a new referrals embed token for the given partner/tenant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createReferralsEmbedToken" method="post" path="/tokens/embed/referrals" -->
```typescript
import { Pimms } from "pimms";

const pimms = new Pimms({
  token: "PIMMS_API_KEY",
});

async function run() {
  const result = await pimms.embedTokens.referrals({
    programId: "<id>",
    partner: {
      name: "<value>",
      email: "Letha_Wuckert2@yahoo.com",
      linkProps: {
        externalId: "123456",
        tagIds: [
          "clux0rgak00011...",
        ],
        testVariants: [
          {
            url: "https://example.com/variant-1",
            percentage: 50,
          },
          {
            url: "https://example.com/variant-2",
            percentage: 50,
          },
        ],
      },
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PimmsCore } from "pimms/core.js";
import { embedTokensReferrals } from "pimms/funcs/embedTokensReferrals.js";

// Use `PimmsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const pimms = new PimmsCore({
  token: "PIMMS_API_KEY",
});

async function run() {
  const res = await embedTokensReferrals(pimms, {
    programId: "<id>",
    partner: {
      name: "<value>",
      email: "Letha_Wuckert2@yahoo.com",
      linkProps: {
        externalId: "123456",
        tagIds: [
          "clux0rgak00011...",
        ],
        testVariants: [
          {
            url: "https://example.com/variant-1",
            percentage: 50,
          },
          {
            url: "https://example.com/variant-2",
            percentage: 50,
          },
        ],
      },
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("embedTokensReferrals failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateReferralsEmbedTokenRequestBody](../../models/operations/createreferralsembedtokenrequestbody.md)                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CreateReferralsEmbedTokenResponseBody](../../models/operations/createreferralsembedtokenresponsebody.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.BadRequest          | 400                        | application/json           |
| errors.Unauthorized        | 401                        | application/json           |
| errors.Forbidden           | 403                        | application/json           |
| errors.NotFound            | 404                        | application/json           |
| errors.Conflict            | 409                        | application/json           |
| errors.InviteExpired       | 410                        | application/json           |
| errors.UnprocessableEntity | 422                        | application/json           |
| errors.RateLimitExceeded   | 429                        | application/json           |
| errors.InternalServerError | 500                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |