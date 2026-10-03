<!-- Start SDK Example Usage [usage] -->
```typescript
import { Pimms } from "pimms";

const pimms = new Pimms({
  token: "PIMMS_API_KEY",
});

async function run() {
  const result = await pimms.links.create({
    url: "https://pimms.io",
    externalId: "123456",
    tagIds: [
      "clux0rgak00011...",
    ],
  });

  console.log(result);
}

run();

```

```typescript
import { Pimms } from "pimms";

const pimms = new Pimms({
  token: "PIMMS_API_KEY",
});

async function run() {
  const result = await pimms.links.upsert({
    url: "https://pimms.io",
    externalId: "123456",
    tagIds: [
      "clux0rgak00011...",
    ],
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->