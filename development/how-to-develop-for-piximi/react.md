---
description: How we use React in Piximi
---

# React

## Organization

Use the following directory structure for new React components:

```text
Foo/Foo.css.ts
Foo/Foo.stories.tsx
Foo/Foo.test.tsx
Foo/Foo.tsx
Foo/index.ts
```

If your component has one or more child components, use the following directory structure:

```text
Foo/Bar/Bar.css.ts
Foo/Bar/Bar.stories.tsx
Foo/Bar/Bar.test.tsx
Foo/Bar/Bar.tsx
Foo/Bar/index.ts
Foo/Foo/Foo.css.ts
Foo/Foo/Foo.stories.tsx
Foo/Foo/Foo.test.tsx
Foo/Foo/Foo.tsx
Foo/Foo/index.ts
Foo/index.ts
```

A component shouldn’t publicly export any of their child components. In the previous example, `Foo/index.ts` should only export `Foo`:

```typescript
export { Foo } from "./Foo";
```

### Cascading Style Sheets \(CSS\)

```typescript
import {Theme} from "@material-ui/core";
import {createStyles} from "@material-ui/styles";

export const styles = ({ palette, spacing }: Theme) => createStyles({});
```

