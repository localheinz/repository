# repository

You

* have an idea for a project involving PHP
* can't wait to get started
* are tired of creating the basics from scratch all the time

and this project provides a template for creating a new PHP project faster.

Follow the example steps outlined below to get started!

## 1. Create a project

Let's assume we want to create the project in `~/Sites/foo/bar`, so let's run

```
$ composer create-project localheinz/repository ~/Sites/foo/bar dev-php
```

to create a project based on the [`php`](https://github.com/localheinz/repository/tree/php) branch.

For reference, see https://getcomposer.org/doc/03-cli.md#create-project.

Now, change into the newly created project so we can move forward:

```
$ cd ~/Sites/foo/bar
```

## 2. Modify starting point to your needs

### `.travis.yml`

After you have enabled the project on https://travis-ci.com, you probably want to

* obtain and encrypt a `GITHUB_TOKEN`
* obtain and encrypt a `CODECLIMATE_REPO_TOKEN`

to replace the existing, encrypted tokens (they will not work for you).

```yml
env:
  global:
    - secure: "..."
    - secure: "..."
```

For encrypting tokens, you need [`travis-ci/travis.rb`](https://github.com/travis-ci/travis.rb), see their [installation instructions](https://github.com/travis-ci/travis.rb#installation).

### `composer.json`

You probably want to adjust

* `name`
* `description`
* `author`
* `license`
* `autoload` and `autoload-dev` configuration

For details see https://getcomposer.org/doc/04-schema.md.

### `README.md`

You probably want to adjust

* title
* links for badges
* etc.

## 3. Initialize git project

Run

```
$ git init
```

to initialize a git project.

Run

```
$ git add .
```

to add the existing files.

Run

```
$ git commit -m 'Initial commit'
```

to create an initial commit.

## 4. Push to remote

Assuming you have created a corresponding GitHub project `foo/bar`, run

```
$ git remote add origin git@github.com:foo/bar.git
```

to add the remote.

Then run

```
$ git push origin
```

:+1: Voilà, you have created your project - happy coding!
