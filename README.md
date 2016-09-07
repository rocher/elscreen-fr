# elscreen-fr
This code is an extension of
the [`elscreen`](https://github.com/knu/elscreen) mode that uses your
window title (Emacs frame name) to show the tabs/screens of
`elscreen`.

## Usage
Mostly the same as `elscreen`:

```{lisp}
    (require 'elscreen-fr)     ;; was (require 'elscreen)
    (elscreen-fr-start)        ;; was (elscreen-start)
```

You can Keep the same `elscreen` customization variables, but some of
them will no take effect. These variables are:

1. `elscreen-display-screen-number`
2. `elscreen-display-tab`
3. `elscreen-tab-display-control`
4. `elscreen-tab-display-kill-screen`

All are set to nil when `elscreen-fr` is started.

## Customization
Useful keys to change from tab to tab, as in most user interfaces
using tabs:

```{lisp}
    (global-set-key [(control prior)] 'elscreen-previous)
    (global-set-key [(control next)] 'elscreen-next)
```

The customization group lets you tweak few parameters.

## Example

### Init
This is the first screen after Emacs startup.
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/0-init.png)

### Open several *tabs*
Once `elscreen-fr` has been started, use it as you would use
`elscreen`. See how opening new *screens* with different buffers on
them change the window title.

The current screen is shown between square brackets:

![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/1-one-tab.png)
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/2-two-tabs.png)
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/3-three-tabs.png)

Now select the first one again,
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/4-three-tabs-select-first.png)

and open `customomize-group`
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/5-three-tabs-first-is-custom.png)


### Customization

You can use numbers or nicknames instead of the default name:
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/6-using-numbers.png)
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/7-using-numbers-and-nicknames.png)


And also a custom *window title prefix* instead of the default frame name:
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/8-with-custom-prefix.png)


## Finally
Tested only under Linux / Gnome.  Feedback welcome!
