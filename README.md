# elscreen-fr
This code is an extension of the `elscreen` mode that uses your window
title (Emacs frame name) to show the tabs/screens of `elscreen`.

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

1. `(global-set-key [(control prior)] 'elscreen-previous)`
2. `(global-set-key [(control next)] 'elscreen-next)`

The customization group lets you tweak few parameters.

## Example

### Init
This is the first screen after Emacs startup.
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/0-init.png)

### Open several *tabs*

![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/1-one-tab.png)
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/2-two-tabs.png)
![screenshot](https://raw.githubusercontent.com/rocher/elscreen-fr/master/img/3-three-tabs.png)


## Finally
Tested only under Linux / Gnome.  Feedback welcome!
