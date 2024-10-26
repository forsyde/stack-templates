# stack-templates
The repository shall provide stack templates that allow a quick start with ForSyDe.


## new-shallow
The stack template `new-shallow` gives a starting point for ForSyDe-Shallow models.

After creating a project with `stack new myproject forsyde/new-shallow`, a few additonal steps have to be taken to have a fully working ForSyDe-Shallow project.

In `package.yaml`:

- Remove the comment before `forsyde-shallow >= 3.5.0.0`

In `stack.yaml`:

1. Add the extra dependency to ForSyDe-Shallow

```
extra-deps:
- forsyde-shallow-3.5.0.0
```

2. If you encounter problems with the Haskell Language Server, add the line

```
system-ghc = true
```
