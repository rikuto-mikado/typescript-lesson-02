# typescript-lesson-02

## What I Learned

### Type Annotations

```typescript
let userName: string;
userName = "Rikuto";  // OK
userName = 123;       // Error: Type 'number' is not assignable to type 'string'
```

JS allows any value. TS catches type mismatches at compile time.

### Primitive Types: Lowercase

| Use | Don't use |
|-----|-----------|
| `string` | `String` |
| `number` | `Number` |
| `boolean` | `Boolean` |

Uppercase versions are wrapper objects, not primitives.

### Types: JS vs TS

**JS & TS (共通)**
| Type | Meaning |
|------|---------|
| `string` | text |
| `number` | integer or float |
| `boolean` | true / false |
| `null` | intentional empty |
| `undefined` | not assigned |
| `object` | non-primitive |
| `symbol` | unique identifier |
| `bigint` | large integers |

**TS only**
| Type | Meaning |
|------|---------|
| `any` | no type checking (avoid) |
| `unknown` | safe `any`, must check before use |
| `never` | never returns (error, infinite loop) |
| `void` | function returns nothing |
| `tuple` | fixed-length array with types |
| `enum` | named constants |
| `interface` | object shape definition |
| `type` | type alias |

## Memo: Node.js Package Management

Same concept as Python virtual environments:

| Python | Node.js |
|--------|---------|
| `venv/` | `node_modules/` |
| `pip install` | `npm install` |
| `requirements.txt` | `package.json` |
| `python script.py` | `npx <command>` |

- `npm install -D typescript` → Installs to project's `node_modules/`
- `npx tsc` → Runs TypeScript from that project
- `npx tsc basics.ts` → Compiles a specific file
- No global impact, isolated per project
