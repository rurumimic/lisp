# Variable

## Top-level definition

```lisp
(defparameter *ten* 10)  ; *TEN*
(defparameter *ten* 100) ; *TEN*
*TEN* ; 100

(defvar *one* 1)  ; *ONE*
(defvar *one* -1) ; *ONE*
*ONE* ; 1
```

### Function

```lisp
(defun guess-my-number ()
  (ash (+ *one* *ten*) -1))
; GUESS-MY-NUMBER

(guess-my-number) ; 50
```

```lisp
(ash 11 1)  ; 22 ; 1011 -> 10110 = 16 + 4 + 2
(ash 11 -1) ; 5  ; 1011 -> 101 = 4 + 1
```

```lisp
(defun return-five ()
  (+ 2 3))

(return-five) ; 5
```

```lisp
(defun smaller ()
  (setf *ten* (1- (guess-my-number)))
  (guess-my-number))
; SMALLER

(defun bigger ()
  (setf *one* (1+ (guess-my-number)))
  (guess-my-number))
; BIGGER
```

```lisp
(bigger)  ; 75
(smaller) ; 62
(smaller) ; 56
```

```lisp
(defun start-over ()
  (defparameter *one* 1)
  (defparameter *ten* 100)
  (guess-my-number))
```

## Local Scope

```lisp
(let ((a 5)
      (b 6))
  (+ a b))
; 11
```

### Local Function

```lisp
(flet ((f (n)
          (+ n 10)))
  (f 5))
; 15

(flet ((f (n)
          (+ n 10))
       (g (n)
          (- n 3)))
  (g (f 5)))
; 12
```

```lisp
(labels ((a (n)
            (+ n 5))
         (b (n)
            (+ (a n) 6)))
  (b 10))
; 21
```
