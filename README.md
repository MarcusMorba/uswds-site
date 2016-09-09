**DISCLAIMER: This repository is a WIP for the work documented in [this issue](https://github.com/18F/web-design-standards/issues/1343) in the main repo.**

# Draft U.S. Web Design Standards documentation

Website and documentation on using the Draft U.S. Web Design Standards: [https://standards.usa.gov](https://standards.usa.gov).

## Running locally

The Draft U.S. Web Design Standards documenation is built using Jekyll for the file framework, gulp for task management, and the node module for the Standards.

You will need to make sure you have the following installed on your machine before following the commands below:

1. Ruby v2.2.2+, [Installation guides](https://www.ruby-lang.org/en/documentation/installation/)
1. Node v4.2.3+, [Installation guides](https://nodejs.org/en/download/)

The documentation is built using [gulp](http://gulpjs.com/) automation. To use gulp, first make sure you have it installed on your machine (globally):

```sh
npm install --global gulp-cli
```

To start, run the following command to install project dependencies:

```sh
npm install
```

Next, you'll perform a build step to copy and compile all of the necessary files that create the site:

```sh
npm run build
```

Now that all of your dependencies are installed, you can run you local server by running the following command:

```sh
npm start
```

Go to `127.0.0.1:4000` in your browser — you should be viewing a local instance of [standards.usa.gov](https://standards.usa.gov).

Here is a reference to a few other utility commands:

- `npm run clean`: Cleans out copied-over dependency assests.

- `npm run lint`: Runs `eslint` and `sass-lint` against JavaScript and Sass files.

- `npm test`: Runs `npm run lint` and can also be used to run any tests.

### Using the latest version of `uswds` package

Sometimes you will want to use the latest version of the `web-design-standards` repo. Use the following steps to do so:

- Clone the latest version of the [`web-design-standards` repo](https://github.com/18F/web-design-standards/tree/staging).
- Run `npm link` in the _root level_ of the `web-design-standards` directory on your local machine.
- Run `npm link uswds` in the _root level_ of the `web-design-standards-docs` directory on your local machine.

You are now using the latest version of the Standards via your cloned version on your local machine. To stop using this version, type `npm unlink uswds` from the _root level_ of the `web-design-standards-docs` directory.

**NOTE: Reminder that you will want to be "watching" the `uswds` package if you plan on making updates to that package.**

## Contributing

Please read through our [contributing guidelines](CONTRIBUTING.md). These guidelines are directions for opening issues and submitting pull requests, and also detail the coding and design standards we follow.
