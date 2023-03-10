# Serverless Node.js Project Skeleton

[![npm](https://img.shields.io/npm/v/@makenew/serverless-nodejs.svg)](https://www.npmjs.com/package/@makenew/serverless-nodejs)
[![GitHub Actions](https://github.com/makenew/serverless-nodejs/workflows/main/badge.svg)](https://github.com/makenew/serverless-nodejs/actions)

Package skeleton for a Node.js Serverless project on AWS Lambda.

## Description

Bootstrap a new Node.js Serverless project in five minutes or less.

### Features

- Deploy to [AWS Lambda] with [Serverless].
- [Node.js]'s [npm] package structure.
- Package management with [npm].
- Examples with configurable options and arguments powered by [examplr].
- Linting with the [JavaScript Standard Style] using [ESLint].
- [Prettier] code.
- Futuristic debuggable unit testing with [AVA].
- Code coverage reporting with [Istanbul] and [c8].
- Continuous deployment, testing, and package publishing with [GitHub Actions].
- [Keep a CHANGELOG].
- Consistent coding with [EditorConfig].
- Badges from [Shields.io].

[AVA]: https://github.com/avajs/ava
[AWS Lambda]: https://aws.amazon.com/lambda/
[ESLint]: https://eslint.org/
[EditorConfig]: https://editorconfig.org/
[GitHub Actions]: https://github.com/features/actions
[Istanbul]: https://istanbul.js.org/
[JavaScript Standard Style]: https://standardjs.com/
[Keep a CHANGELOG]: https://keepachangelog.com/
[Node.js]: https://nodejs.org/
[Prettier]: https://prettier.io/
[Serverless]: https://serverless.com/
[Shields.io]: https://shields.io/
[c8]: https://github.com/bcoe/c8
[examplr]: https://github.com/meltwater/node-examplr
[npm]: https://www.npmjs.com/

### Bootstrapping a new project

1. Create an empty (**non-initialized**) repository on GitHub.
2. Clone the master branch of this repository with
   ```
   $ git clone --single-branch git@github.com:makenew/serverless-nodejs.git <new-node-lib>
   $ cd <new-node-lib>
   ```
   Optionally, reset to the latest version with
   ```
   $ git reset --hard <version-tag>
   ```
3. Run
   ```
   $ ./makenew.sh
   ```
   This will replace the boilerplate, delete itself,
   remove the git remote, remove upstream tags,
   and stage changes for commit.
4. Create the required GitHub repository secrets.
5. Review, commit, and push the changes to GitHub with
   ```
   $ git diff --cached
   $ git commit -m "Replace makenew boilerplate"
   $ git remote add origin git@github.com:<user>/<new-node-lib>.git
   $ git push -u origin master
   ```
6. Ensure the GitHub action passes,
   then release the initial version with
   ```
   $ nvm install
   $ npm install
   $ npm version patch
   ```

### Updating from this skeleton

If you want to pull in future updates from this skeleton,
you can fetch and merge in changes from this repository.

Add this as a new remote with

```
$ git remote add upstream git@github.com:makenew/serverless-nodejs.git
```

You can then fetch and merge changes with

```
$ git fetch --no-tags upstream
$ git merge upstream/master
```

#### Changelog for this skeleton

Note that `CHANGELOG.md` is just a template for this skeleton.
The actual changes for this project are documented in the commit history
and summarized under [Releases].

[Releases]: https://github.com/makenew/serverless-nodejs/releases

## Installation

Add this as a dependency to your project using [npm] with

```
$ npm install @makenew/serverless-nodejs
```

[npm]: https://www.npmjs.com/

## Development and Testing

### Quickstart

```
$ git clone https://github.com/makenew/serverless-nodejs.git
$ cd serverless-nodejs
$ nvm install
$ npm install
```

Run the command below in a separate terminal window:

```
$ npm run test:watch
```

Primary development tasks are defined under `scripts` in `package.json`
and available via `npm run`.
View them with

```
$ npm run
```

### Source code

The [source code] is hosted on GitHub.
Clone the project with

```
$ git clone git@github.com:makenew/serverless-nodejs.git
```

[source code]: https://github.com/makenew/serverless-nodejs

### Requirements

You will need [Node.js] with [npm] and a [Node.js debugging] client.

Be sure that all commands run under the correct Node version, e.g.,
if using [nvm], install the correct version with

```
$ nvm install
```

Set the active version for each shell session with

```
$ nvm use
```

Install the development dependencies with

```
$ npm install
```

[Node.js]: https://nodejs.org/
[Node.js debugging]: https://nodejs.org/en/docs/guides/debugging-getting-started/
[npm]: https://www.npmjs.com/
[nvm]: https://github.com/creationix/nvm

### Publishing

Use the [`npm version`][npm-version] command to release a new version.
This will push a new git tag which will trigger a GitHub action.

Publishing may be triggered using a [version workflow_dispatch on GitHub Actions].

[npm-version]: https://docs.npmjs.com/cli/version
[version workflow_dispatch on GitHub Actions]: https://github.com/makenew/serverless-nodejs/actions?query=workflow%3Aversion

### Deployment

Serverless deployment is triggered by a release repository_dispatch on GitHub Actions.

Deployment may be triggered using a [release workflow_dispatch on GitHub Actions].

[release workflow_dispatch on GitHub Actions]: https://github.com/makenew/serverless-nodejs/actions?query=workflow%3Arelease

## GitHub Actions

_GitHub Actions should already be configured: this section is for reference only._

The following repository secrets must be set on [GitHub Actions]:

- `NPM_TOKEN`: npm token for installing and publishing packages.
- `AWS_DEFAULT_REGION`: The AWS region Serverless will deploy to.
- `AWS_ACCESS_KEY_ID`: AWS access key ID.
- `AWS_SECRET_ACCESS_KEY`: AWS secret access key.
- `GH_TOKEN`: A personal access token that can trigger workflows.

These must be set manually.

### Secrets for Optional GitHub Actions

The version and format GitHub actions
require a user with write access to the repository.
including access to trigger workflows.
Set these additional secrets to enable the action:

- `GH_TOKEN`: A personal access token for the user.
- `GIT_USER_NAME`: The GitHub user's real name.
- `GIT_USER_EMAIL`: The GitHub user's email.
- `GPG_PRIVATE_KEY`: The GitHub user's [GPG private key].
- `GPG_PASSPHRASE`: The GitHub user's GPG passphrase.

[GitHub Actions]: https://github.com/features/actions
[GPG private key]: https://github.com/marketplace/actions/import-gpg#prerequisites

## Contributing

Please submit and comment on bug reports and feature requests.

To submit a patch:

1. Fork it (https://github.com/makenew/serverless-nodejs/fork).
2. Create your feature branch (`git checkout -b my-new-feature`).
3. Make changes.
4. Commit your changes (`git commit -am 'Add some feature'`).
5. Push to the branch (`git push origin my-new-feature`).
6. Create a new Pull Request.

## License

This Serverless project is licensed under the MIT license.

## Warranty

This software is provided by the copyright holders and contributors "as is" and
any express or implied warranties, including, but not limited to, the implied
warranties of merchantability and fitness for a particular purpose are
disclaimed. In no event shall the copyright holder or contributors be liable for
any direct, indirect, incidental, special, exemplary, or consequential damages
(including, but not limited to, procurement of substitute goods or services;
loss of use, data, or profits; or business interruption) however caused and on
any theory of liability, whether in contract, strict liability, or tort
(including negligence or otherwise) arising in any way out of the use of this
software, even if advised of the possibility of such damage.
