# Retyped routes (beta)

## About

Retyped routes provides a type-safe way to create API definitions with [retype](https://github.com/withgraphite/retype) in a way that can be read both by the server and client.

## Install

```
yarn add @withgraphite/retyped-routes
```

## Usage

```typescript
import * as t from "@withgraphite/retype";
import { asRouteTree } from "@withgraphite/retyped-routes";

const API_ROUTES = asRouteTree({
  login: {
    method: "POST",
    url: "/auth",
    params: {
      email: t.string,
      password: t.string,
    },
    response: {
      token: t.string,
    },
  },
} as const);

export default API_ROUTES;
```

## License

Copyright 2021, Screenplay Studios Inc.
