## Completing the Compiler: Proposed Implementation

### Compilation Engine

- Gets its input from a JackTokenizer and writes its output using the VMWriter
- Organized as a series of compilexxx routines, xxx being a syntactic element in the Jack language
- Contract:
  - Each compilexxx routine should read xxx from the input, advance() the input exactly beyond xxx, and emit to the output VM code effecting the semantics of xxx
  - Thus compilexxx should be called only if xxx is the current syntactic element
  - If xxx is part of an expression and thus has a value, the emitted VM code should compute this value and leave it at the top of VM stack

