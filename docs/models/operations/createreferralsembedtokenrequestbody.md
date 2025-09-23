# CreateReferralsEmbedTokenRequestBody

## Example Usage

```typescript
import { CreateReferralsEmbedTokenRequestBody } from "pimms/models/operations";

let value: CreateReferralsEmbedTokenRequestBody = {
  programId: "<id>",
  partner: {
    name: "<value>",
    email: "Soledad90@yahoo.com",
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
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `programId`                                              | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `partnerId`                                              | *string*                                                 | :heavy_minus_sign:                                       | N/A                                                      |
| `tenantId`                                               | *string*                                                 | :heavy_minus_sign:                                       | N/A                                                      |
| `partner`                                                | [operations.Partner](../../models/operations/partner.md) | :heavy_minus_sign:                                       | N/A                                                      |