# My First Assembly Code...
## Build & Run

```bash
# Assemble
as asem.s -o asem.o          # GNU assembler → object file

# Link (static, no C runtime)
gcc -o asem asem.o -nostdlib -static          # produces a fully‑static ELF

# Execute
./asem
````

### What the flags do

| Flag        | Purpose                                                                          |
| ----------- | -------------------------------------------------------------------------------- |
| `-nostdlib` | Don’t link the standard C runtime (we rely only on our own code + the kernel).   |
| `-static`   | Produce a statically linked binary so it runs without external shared libraries. |

Running `./asem` should print:

```
Hello, World!
```
