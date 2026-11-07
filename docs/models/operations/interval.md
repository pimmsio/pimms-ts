# Interval

The interval to retrieve analytics for. If undefined, defaults to 24h.

## Example Usage

```typescript
import { Interval } from "pimms/models/operations";

let value: Interval = "all";
```

## Values

```typescript
"24h" | "7d" | "30d" | "90d" | "6m" | "1y" | "mtd" | "qtd" | "ytd" | "all"
```