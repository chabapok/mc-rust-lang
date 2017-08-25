# mc-rust-lang
Midinight Commander syntax highlighting for RUST

For Ubuntu:

1. Put `rs.syntax` file to `/usr/share/mc/syntax`
2. Add to `/usr/share/mc/syntax/Syntax` BEFORE `unknown` definitoins:

```
file ..\*\\.rs$ RUST\sProgram
include rs.syntax
```

