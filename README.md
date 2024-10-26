# stack-templates
The repository shall provide stack templates that allow a quick start with ForSyDe.


## new-shallow
The stack template `new-shallow` gives a starting point for ForSyDe-Shallow models. The following text assumes that you create a new ForSyDe-Shallow project with the name `shallow-project`.

### Creating the project
Create the project structure using the stack template `forsyde/new-shallow`.
```
stack new shallow-project forsyde/new-shallow
```
After creating the project structure, a few additonal steps have to be taken to have a fully working ForSyDe-Shallow project.

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
system-ghc: true
```
### Build and run the project
1. Enter the project directory and build the project
```
stack build
```
2. Execute the project
```
stack exec shallow-project-exe
```
Now, you should receive the following output:
```
{2,3,4,5,6,7,8,9,10,11}
```
