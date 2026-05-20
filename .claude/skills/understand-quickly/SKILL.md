```markdown
# understand-quickly Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `understand-quickly` TypeScript repository. You'll learn about file naming, import/export styles, commit conventions, and how to write and run tests. This guide is ideal for contributors who want to quickly align with the project's established practices.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myUtility.ts`, `parseData.test.ts`

### Import Style
- Use **relative imports** for referencing local modules.
  - Example:
    ```typescript
    import { parseData } from './parseData';
    ```

### Export Style
- Use **named exports** instead of default exports.
  - Example:
    ```typescript
    // In parseData.ts
    export function parseData(input: string): ParsedResult { ... }
    ```

### Commit Message Patterns
- Mixed commit types, commonly using the `fix` prefix.
- Average commit message length: ~59 characters.
  - Example: `fix: correct parsing logic for edge cases`

## Workflows

### Code Contribution
**Trigger:** When adding or updating features or fixing bugs  
**Command:** `/contribute`

1. Create or update files using camelCase naming.
2. Use relative imports and named exports in your TypeScript files.
3. Write or update corresponding test files using the `*.test.*` pattern.
4. Commit changes with a descriptive message, prefixed with the type (e.g., `fix:`).
5. Open a pull request for review.

### Writing Tests
**Trigger:** When adding new code or refactoring existing code  
**Command:** `/write-test`

1. Create a test file named `yourModule.test.ts` alongside the module.
2. Write tests using your preferred testing framework (framework is currently unknown).
3. Ensure tests cover all new or changed functionality.
4. Run tests locally to verify correctness.

### Reviewing Code
**Trigger:** When reviewing a pull request  
**Command:** `/review`

1. Check that file naming, import, and export conventions are followed.
2. Verify that commit messages use the correct prefix and are descriptive.
3. Ensure all new code is covered by tests in `*.test.*` files.
4. Run the test suite to confirm all tests pass.

## Testing Patterns

- Test files follow the `*.test.*` naming convention (e.g., `parseData.test.ts`).
- The specific testing framework is not detected; use the project's existing test patterns as reference.
- Place test files alongside the modules they test.
- Tests should comprehensively cover the logic and edge cases of the module.

  Example:
  ```typescript
  // parseData.test.ts
  import { parseData } from './parseData';

  describe('parseData', () => {
    it('should parse valid input', () => {
      const result = parseData('input');
      expect(result).toEqual({ /* expected output */ });
    });
  });
  ```

## Commands
| Command        | Purpose                                            |
|----------------|----------------------------------------------------|
| /contribute    | Start the code contribution workflow               |
| /write-test    | Begin writing or updating tests for your code      |
| /review        | Review code for conventions and test coverage      |
```