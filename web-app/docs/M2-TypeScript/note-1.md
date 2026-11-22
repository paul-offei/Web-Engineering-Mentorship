# Environmental Setup 
* We will be making use of our terminal a lot


## Installing Text Editor and Git
* [Installing VS Code](https://code.visualstudio.com/Download)
* [Installing Git](https://git-scm.com/download/win)

 
## Installing the Node Run Time Environment
* [Intalling Node version Manager](https://github.com/coreybutler/nvm-windows/releases)
* Checking NVM Version
```bash
nvm --version
```
* You can Install the latest available version number
```bash
nvm install 26
``` 
* Use the latest version
```bash
nvm use 26
```
* Install the latest LTS version (we will mostly use this forr security reasons)
```bash
nvm install --lts 
```
      
* Use the latest LTS version
```bash
nvm use --lts                        
```
* Check the node version
```bash
node --version                       
```
* Check the version of node default package manager (NPM)
```bash
npm --version                    
```

## Install Yarn package manager
```bash
npm install -g corepack               
```


* [Yarn is a package manager that doubles down as project manager.](https://yarnpkg.com/)


* Initialize a new project
```bash
mkdir test
cd test
yarn init -2                
```


* Check the version
```bash
yarn --version                    
```



* Any time you'll want to update Yarn to the latest version, just run:
```bash
yarn set version stable
yarn install           
```

## Let Setup TypeScript Playground
```bash
mkdir playground
cd playground
yarn init -2
yarn add typescript -D
yarn add immutable
```

* Initializing the Typescript prroject
```bash
cd playground
yarn tsc -init
touch main.ts
```

* Code in the `main.ts` file
```ts
console.log("Welcome to Web-based Application Development")
```

* Turning typescript code into javascript and and run it
```bash
cd playground
yarn tsc
node bin/main..js
```
* Continous compilation: add the watch command 
```bash
cd playground
yarn tsc -w
```