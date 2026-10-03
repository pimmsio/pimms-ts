# SortMetric

Optional secondary sort metric for list endpoints (used for deterministic ordering and top-N selection).

## Example Usage

```typescript
import { SortMetric } from "pimms/models/operations";

let value: SortMetric = "clicks";
```

## Values

```typescript
"clicks" | "leads" | "sales" | "saleAmount"
```