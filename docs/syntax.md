# Syntax

## Basic

### Symbol

```lisp
(eq 'fooo 'FoOo) ; T
```

### Number

```lisp
(+ 1 1.0) ; 2.0
(expt 53 53) ; 24356848165022712132477606520104725518533453128685640844505130879576720609150223301256150373
(/ 4 6) ; 2/3
(/ 4.0 6) ; 0.6666667
```

### String

```lisp
(princ "Tutti Frutti")
; Tutti Frutti ; by princ
; "Tutti Frutti"  ; REPL
```

escape:

```lisp
(princ "He said \"Hello, there.\"")
```

## Code / Data Mode

```lisp
(+ 3 4)  ; 7
'(+ 3 4) ; (+ 3 4)
```

## List

```lisp
(cons 'chicken 'cat) ; (CHICKEN . CAT)
(cons 'chicken 'nil) ; (CHICKEN)
(cons 'chicken ())   ; (CHICKEN)

(cons 'pork '(beef chicken)) ; (PORK BEEF CHICKEN)
(cons 'beef (cons 'chicken ())) ; (BEEF CHICKEN)
(cons 'pork (cons 'beef (cons 'chicken ()))) ; (PORK BEEF CHICKEN)
```

```lisp
(car '(pork beef chicken)) ; PORK
(cdr '(pork beef chicken)) ; (BEEF CHICKEN)
```

```lisp
(list 'pork 'beef 'chicken) ; (PORK BEEF CHICKEN)
```

```lisp
'(cat (duck bat) ant) ; (CAT (DUCK BAT) ANT)
```
