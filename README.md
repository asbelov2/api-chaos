# API Chaos

**Test how your app behaves when the API doesn't.**

A lightweight, framework-agnostic TypeScript library for simulating HTTP errors, network failures, and slow responses during development.

### Why API Chaos?

Testing the happy path is easy. Testing a failed backend, delayed response, or unstable connection shouldn't require modifying server code.

### Proposed API

```ts
const chaosFetch = createChaosFetch(fetch, {
  enabled: true,
  rules: [{
    match: '/api/users',
    probability: 1,
    action: {
      type: 'http-error',
      status: 503
    }
  }]
});
```

### MVP

- HTTP error injection
- Artificial response delays
- Network error simulation
- URL and method matching
- Probability-based failure injection
- Native Fetch API compatibility

**Status:** Planning. API subject to change.

**License:** MIT (planned).
