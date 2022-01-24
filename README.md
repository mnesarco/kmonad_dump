# KMonad Dump

Compile KMnad configuration file into keyboard layout code to visualize at http://www.keyboard-layout-editor.com/

## From this:

```
...

(deflayer colemakdhmo
  XX        f1   f2   f3   f4   f5           ssrq     f6   f7   f8   f9   f10
  XX   XX   w    f    p    b    XX           f11      f12   j    l    u    -    grv
  @_nav  q    r    s    t    g               bspc      m    n    e    i    @~n
  bspc     a    c    d    v    z             caps    @_mac    k    h    y   o
             x        @calt  @tctl @_num      @ssp @_pun                   met   ent
                                                    ralt
)

...

```

## To this:

![Layout Visualization](https://github.com/mnesarco/kmonad_dump/raw/main/example.jpg)

## Just adding a block comment in your KMonad file:

```

#|
<hardware-layout>

!!! Keycap layout and colors
----------------------------

(keycap 
    _ _ _
    _ _ _
    _ _ _
    _ _ _
)

(colors
    _ _ _
    _ _ _
    _ _ _
    _ _ _
)

!!! Custom options per key (Optional)
!!! Options are based on `defsrc` (a.k.a. Layer 0) keys
-------------------------------------------------------

(options key custom_layout)
.
.
.

!!! Override or assign labels (Optional)
----------------------------------------

(label alias label)
.
.
.

!!! Add some notes (Optional)
-----------------------------

(description
    Free Text
)

</hardware-layout>
|#
```

See example: https://github.com/mnesarco/kmonad_dump/raw/main/example.kbd

## Usage:

```
python3 kmonad_dump.py example.kbd

```

# Requirements:

- Python3.6+

# References:

- KMonad: https://github.com/kmonad/kmonad
<br />Amazing keyboard customization tool.

- Keyboard Layout Editor: http://www.keyboard-layout-editor.com/
<br />Online Keyboard Layout visualization and editing tool.
