# Setting up your environment

+ For following along in class, you can use the [this online OCaml interpreter](https://try.ocamlpro.com/), but you will need to eventually install OCaml 
  locally for development for this course: 
+ First, [install OCaml on your system](https://ocaml.org/docs/installing-ocaml).
  Follow all the instructions on this page, including installing platform tools.
+ You should follow the "Check Installation" instructions to ensure you
  have properly installed OCaml.
+ You should configure your preferred development environment (VSCode,
  Vim, Emacs) to have OCaml support following [these instructions](https://ocaml.org/docs/set-up-editor)
+ You should use OCaml version `4.14.0` for this class. You should follow
  the instructions for using `opam switch` [here](https://ocaml.org/docs/opam-switch-introduction). 

```
opam switch create cs4400 4.14.0
opam switch cs4400
```

+ You should install the following packages which we will use in this course:

```
opam install ocaml-lsp-server odoc ocamlformat utop merlin ounit menhir
```

+ It is likely OK to use whichever version of OCaml is installed by default
  on your system. We will not be using features that are backwards incompatible.
  However, our testing environment will use OCaml version `4.14.0`, so if you
  encounter autograder build issues, this may be why.
+ A common issue is that your path may not be up-to-date with the installed
  OCaml tools. If you ever encounter an error relating to this, you may need
  to run the following command which inserts all the OCaml binaries into your path:

```
eval `opam env`
```

# Running this starter project

+ After setting up your environment, you should be able to build this repository.
+ Your code goes inside `main.ml`
+ To build and run the code `Main.ml`, run the following:

```
dune exec ./main.exe
```

+ OCaml will fail to build if you have unused variables when building with `dune`. If you want
  to ignore these warnings, you can use the following dune command instead:

```
dune exec ./main.exe --profile release
```

+ If you set up your environment correctly, you will see the following output:

```
...                              
Ran: 3 tests in: 0.11 seconds.
OK
```
