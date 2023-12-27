# Example Esy Empty Project

Setting up bare bones Esy project.

## Installations

Install Esy package manager.  Esy is a package manager originally maintained by Facebook and was built on top of Opam. It is designed to behave like npm/yarn in the JavaScript ecosystem. Without Esy, some packages are not available such as those provided by Reason-Native.
More information can be found [on their website](https://esy.sh/).
```
npm install -g esy
```

Next, create an `esy.json` file for specifying dependencies and version numbers.
```
echo "{}" > esy.json
```

Then add ocaml and dune as dependencies.  This will ensure your project dependencies will work your current version of ocaml and dune. You can discover the latest version by visiting [OCaml's release page](https://ocaml.org/releases)
```js
esy add ocaml @opam/dune
```

After installing your first dependencies you should see new files and directories used for maintaining the dependency tree. JavaScript developers will be familiar with this. At the time of writing this, the command generated `_esy/` and `esy.lock` directories.
```
_esy/
esy.lock/
.gitignore
esy.json
README.md
```
