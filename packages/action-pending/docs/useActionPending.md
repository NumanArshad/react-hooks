---
title: useActionPending
nav:
  title: Hooks
  path: /hook
group:
  title: Action Pending
  path: /action-pending
order: 2
---

# useActionPending

By providing an async function, this hook creates a wrapped version with a number indicating how many pending calls are on the fly.

```typescript
type AsyncFunction = (...args: any[]) => Promise<any>;

function useActionPending<A extends AsyncFunction>(action: A): [A, number]
```

The second value of returned tuple is the `pendingCount`, a simple `!!pendingCount` can be used to check whether there is any unfinished calls and motivates to a loading UI.

<code src="./demo/useActionPending.tsx">