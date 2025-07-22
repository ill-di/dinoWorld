# Test Failures Documentation

## Summary

This document lists the current test failures in the `client/`, `server/`, and `shared/` directories as of July 22, 2025.

---

### client/

- 1 test suite failed, 5 passed, 6 total
- Notable failures:
  - `__tests__/themeGeneration.integration.test.ts`:
    - Test suite failed to run: Your test suite must contain at least one test.
- Coverage thresholds not met for statements, branches, lines, and functions (see Jest output for details).
- Many files and components have 0% coverage.

---

### server/

- 1 test suite failed, 7 passed, 8 total
- Notable failures:
  - `__tests__/projectManagement.test.ts`:
    - Console errors: `NotFoundError: Calendar project non-existent-id not found`
    - Expected property `error` with value `Missing required fields`, but received a different structure.
  - Various `CalendarError` and validation errors in `calendar.test.ts` and related files (invalid months, missing required fields, invalid event date format, etc.)

---

### shared/

- 1 test suite failed, 1 total
- Notable failures:
  - `__tests__/pdfExport.test.ts`:
    - TypeScript errors: Duplicate identifier 'PDFDocument', 'PageSizes', and 'mockPngBuffer'.
    - Syntax errors: Unexpected keyword or identifier, declaration or statement expected.
    - Cannot redeclare block-scoped variable 'mockPngBuffer'.
    - Only refers to a type, but is being used as a value.

---

## Next Steps

- Review and fix the test configuration in `client/`.
- Address TypeScript and logic errors in `shared/__tests__/pdfExport.test.ts`.
- Investigate and resolve API and validation errors in `server/` test suites.
