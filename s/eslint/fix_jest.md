---
layout: post
title: Fix Jest tests errors
date: 2019-08-22
---

Ah those ESLint errors again... At least they are easy to fix.

Just install `eslint-plugin-jest` as dev dependency.

```bash
yarn add -D eslint-plugin-jest
```

And add following properties to your `.eslintrc`.

```json
{
  ...
  "extends": [..., "plugin:jest/recommended", ...]
  "plugins": ["jest"]
  "env": {
      "jest/globals": true
  }
  ...
}
```

Enjoy your error-free Jest tests!