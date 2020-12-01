# Extended keys for [Alacritty]

[Alacritty]: https://github.com/alacritty/alacritty

Enable CSI u mode.

The specification can be found at [Fix keyboard input on terminals].

[Fix keyboard input on terminals]: http://www.leonerd.org.uk/hacks/fixterms/

## Installation

Copy [`keys.yml`] to your config file.

[`keys.yml`]: keys.yml

## Configuration

### Add more keys

Read the [specification].

The syntax is:

```
CSI <code-point> ; <modifier> u
```

In Alacritty-speak, it is:

``` yaml
key_bindings:
  - { key: <key>, mods: <modifiers>, chars: "\x1b[<code-point>;<modifier>u" }
```

Get Alacritty key names for the `key` section:

``` sh
alacritty --print-events
```

Get the code points for the `chars` section:

``` sh
showkey --ascii
```

## References

- [Specification]

[Specification]: http://www.leonerd.org.uk/hacks/fixterms/
