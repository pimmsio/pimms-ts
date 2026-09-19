# GroupBy

The parameter to group the analytics data points by. Defaults to `count` if undefined.

## Example Usage

```typescript
import { GroupBy } from "pimms/models/operations";

let value: GroupBy = "channels";
```

## Values

```typescript
"count" | "timeseries" | "link_timeseries" | "continents" | "regions" | "countries" | "cities" | "devices" | "browsers" | "os" | "trigger" | "triggers" | "referers" | "referer_urls" | "channels" | "top_links" | "top_urls" | "utm_combinations" | "utm_sources" | "utm_mediums" | "utm_campaigns" | "utm_terms" | "utm_contents"
```