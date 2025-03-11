## Development

- Put `.env.example` in project root and keep it updated.
- Install `biome` in your code editor and use this [configuration file](./files/biome.json).
- If you are working on `typescript` project use this [tsconfig.json](./files/tsconfig).
- If you starting a new project install [husky](https://typicode.github.io/husky).

## Naming convention

### Types, interfaces and classes - Pascal case

```ts
interface User {}

type Session = {}

class User {
  constructor() {}
}
```

> [!NOTE]
> Prefer interfaces over types.

### Files - Kebab case

```sh
user.ts
user-auth.ts
```

### Constants - ALL CAPS

```ts
const SESSION_TIMEOUT = 50;
```

### Enums - Pascal case and members all caps

```ts
enum UserRoles {
  ADMIN = 'admin',
  USER = 'user',
}
```

### Constant values - lower case

```ts
const USER_ROLE = 'admin';
```

### Variables and functions - Camel case

```ts
function getUser() {}
const userData = {};
```

### Use absolute path imports

```ts
// Good:
import config from '@/config/common';
import config from '@/config';

// Bad:
import config from '../../../config';
```
