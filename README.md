# stack-templates
The repository shall provide stack templates that allow a quick start with ForSyDe.

It assumes that you have already an installed Haskell environment. Otherwise, follow the instructions on the [Haskell webpage](https://www.haskell.org/) to install it.


## new-shallow
The stack template `new-shallow` gives a starting point for ForSyDe-Shallow models. The following text assumes that you create a new ForSyDe-Shallow project with the name `my-shallow-project`.

### Creating the project
Create the project structure using the stack template `forsyde/new-shallow`. 
```
stack new my-shallow-project forsyde/new-shallow
```
After creating the project structure, a few additonal steps have to be taken to have a fully working ForSyDe-Shallow project.

Enter the project directory `my-shallow-project` and change the following in the files `package.yaml` and `stack.yaml`.

In `package.yaml`:

- Remove the comment character (`#`) before `- forsyde-shallow >= 3.5.0.0`

In `stack.yaml`:

1. Add the extra dependency to ForSyDe-Shallow

```
extra-deps:
- forsyde-shallow-3.5.0.0
```

You can add it at the end of the file.

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
stack exec my-shallow-project-exe
```
Now, you should receive the following output:
```
{2,3,4,5,6,7,8,9,10,11}
```

## new-atom
The stack template `new-atom` gives a starting point for ForSyDe-Atom models. The following text assumes that you create a new ForSyDe-Atom project with the name `my-atom-project`.

### Creating the project
Create the project structure using the stack template `forsyde/new-atom`.
```
stack new my-atom-project forsyde/new-atom
```
After creating the project structure, a few additonal steps have to be taken to have a fully working ForSyDe-Shallow project.

Enter the project directory `my-atom-project` and change the following in the files `package.yaml` and `stack.yaml`.

In `package.yaml`:

- Remove the comment character (`#`) before `- forsyde-atom >=0.3.2 && <0.3.3`

In `stack.yaml`:

1. Add the extra dependency to ForSyDe-Atom. Here we use a so far inofficial version that has been developed for newer GHC-version (9.6.6). You can add it at the end of the file.

```
extra-deps:
- git: git@github.com:forsyde/forsyde-atom.git
  commit: dc70e7f764f149bbe5ddb8a97f000aad34a09f91
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
stack exec my-atom-project-exe
```
Now, you should receive the following output:
```
{2,3,4,5,6,7,8,9,10,11}
```
