# mc-rust-lang
Midinight Commander syntax highlighting for RUST

For Ubuntu:

1. Put `rs.syntax` file to `/usr/share/mc/syntax`
2. Add to `/usr/share/mc/syntax/Syntax` BEFORE `unknown` definitoins:

```
file ..\*\\.rs$ RUST\sProgram
include rs.syntax
```


# If you want to help this project

* Right now we don't have full syntax support. I would be glad to get your PR with extended syntax support.

# At that moment we do not support:

```
// This is syntax madness. In general, we could highlight it,
// but i didn't find such syntax in the reference, that why it looks like quotes.
let x = r###"abcdefg"###;

// content inside the brackets doesn't parse in any special way or parse badly
// 
impl<....>

// it would be nice to colorize fields and their types in structures
struct Foo {
 v: MyType
}

```


# If doesn't work

* Make sure, that you use `mcedit` and not `mcview`. Right now `mcview` doesn't have syntax highlight. 
* Try ctrl+s. In mc this key combination -- syntax, and not save
* Make sure, that pattern is written till unknown in the Syntax file. (it possible to write in begin of file)
* Make sure, that file `~/.config/mc/mcedit/Syntax` doesn't exist. If file exists you need to write configuration inside
* Perhaps, your mc could use other paths to configs. Read `man mcedit` about it

If after this steps it still doesn't work you could try to find solution and create PR with problem description  and solution.
