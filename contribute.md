# Contribute

## Getting Started

We utilize a few Javascript libraries and VS Code Extensions that make development of Architecture Diagrams easy, and fun.  Once you clone the repo:

    git clone https://github.com/architectonics/sysopssquad

You'll want to run the command to install the NPM dependencies:

    npm install

Give it a few minutes to download a few dependencies, then run:

    npm start

in order to build and start the documentation in the dev webserver, which should now be running at:  http://localhost:3000

## VS Code Extensions
There are a number of VS Code Extensions recommended in the [extensions.json](.vscode/extensions.json) file.  Feel free to install them yourself, or re-launch VS Code in this folder, and you should get prompted to install these extensions.  

## Contributions

Please create a github fork of the repository, and submit any pull requests.  Because the images are just text files, using traditional git workflows works great for both major refactoring and minor enhancements to the images.

## Steps before submitting your pull request

The /docs folder is what is served on our [Github Pages](https://architectonics.github.io/sysopssquad/).  Please execute the following commands before submitting your PR:

```shell
npm run buildStatic 
git add docs/
git commit -m "<your commit message>"
```

Ideally, we'd configure a [C4 Builder Action](https://github.com/marketplace/actions/c4builder) to do all of this, and if you'd like to submit a PR to improve the build process, we'd welcome that!