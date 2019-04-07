### cl-python
---
https://github.com/metawilm/cl-python

```lisp
// lib/sys.lisp

(in-package :clpython.module.sys)
(in-syntax *user-readtable*)

(defmacro def-habitat-attribute (name accessor-func doc)
  `(progn (defparameter ,name
    (clpython::make-writable-attribute
      (lambda () (,accessor-func clpython:*habitat*))
      (lambda (val) (setf (,accessor-func clpython:*habitat*) val)))
    ,doc)
  (set-impl-status ',name t)))

```

```
```

```
```


