# ac-racer.el [![melpa badge][melpa-badge]][melpa-link] [![melpa stable badge][melpa-stable-badge]][melpa-stable-link]

ac-racer.el is an auto-complete source of [racer](https://github.com/phildawes/racer) for rust language.


## Screenshot

![ac-racer](image/ac-racer.png)


## Installation

`ac-racer` is available on [MELPA](https://melpa.org) and [MELPA-STABLE](https://stable.melpa.org).

You can install `ac-racer` with the following command.

<kbd>M-x package-install [RET] ac-racer [RET]</kbd>


## Configuration

You must set `racer-cmd` and `racer-rust-src-path`. See [racer document](https://github.com/phildawes/racer#emacs-integration) in more detail.

```lisp
(custom-set-variables
 '(racer-cmd (expand-file-name "your racer path"))
 '(racer-rust-src-path (expand-file-name "your rust source code path")))
```


## Sample Configuration

```lisp
(defun my/racer-mode-hook ()
  (ac-racer-setup))
(add-hook 'racer-mode-hook 'my/racer-mode-hook)

(custom-set-variables
 '(racer-cmd (expand-file-name "~/src/racer/target/release/racer"))
 '(racer-rust-src-path (expand-file-name "~/src/rustc/src")))
```

[melpa-link]: http://melpa.org/#/ac-racer
[melpa-stable-link]: http://stable.melpa.org/#/ac-racer
[melpa-badge]: http://melpa.org/packages/ac-racer-badge.svg
[melpa-stable-badge]: http://stable.melpa.org/packages/ac-racer-badge.svg
