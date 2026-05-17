```markdown
# Full-bord-agent Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns used in the `Full-bord-agent` TypeScript codebase. You'll learn the project's coding conventions, commit message style, file organization, and how to write and run tests. The repository does not use a framework, focusing on clean, modular TypeScript code.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example:  
    ```
    user-service.ts
    data-model.test.ts
    ```

### Import Style
- Use **relative imports** for referencing other files.
  - Example:
    ```typescript
    import { fetchData } from './utils/fetch-data';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In user-service.ts
    export function getUser(id: string) { ... }

    // In another file
    import { getUser } from './user-service';
    ```

### Commit Messages
- Follow **Conventional Commits** with the `feat` prefix for new features.
  - Example:
    ```
    feat: add user authentication middleware
    ```

## Workflows

### Creating a New Feature
**Trigger:** When adding new functionality  
**Command:** `/create-feature`

1. Create a new TypeScript file using kebab-case (e.g., `new-feature.ts`).
2. Use named exports for all functions or constants.
3. Import dependencies using relative paths.
4. Write a conventional commit message prefixed with `feat`.
5. (Optional) Add a corresponding test file named `new-feature.test.ts`.

### Writing a Test
**Trigger:** When testing a module or function  
**Command:** `/write-test`

1. Create a test file with the same name as the module, adding `.test` before the extension (e.g., `user-service.test.ts`).
2. Write tests using the project's preferred (unknown) testing framework.
3. Use relative imports to bring in the module under test.
4. Use named exports for any test utilities.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern.
  - Example: `api-handler.test.ts`
- The testing framework is not specified; check existing tests for patterns.
- Tests import modules using relative paths and named exports.

  ```typescript
  import { getUser } from './user-service';

  describe('getUser', () => {
    it('returns user data for a valid id', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command          | Purpose                                  |
|------------------|------------------------------------------|
| /create-feature  | Scaffold a new feature module            |
| /write-test      | Create a new test file for a module      |
```
