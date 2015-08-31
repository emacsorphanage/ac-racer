# ac-racer.el

ac-racer.el is an auto-complete source of [racer](https://github.com/phildawes/racer) for rust language.


## Screenshot

![ac-racer](image/ac-racer.png)


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
