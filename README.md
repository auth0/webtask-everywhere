# Write once, run servers anywhere

Sample project for creating an Express-based server that runs on webtask.io or as a node server with the same codebase.

## How it works

In the project root, there are two files: 1) `server.js`; and 2) `webtask.js`.
These files are the entry-points into the node and webtask versions of the code in `lib/`, respectively.

There is no magic for making this work as a node server.

To make the same code-base work as a webtask, webpack is used to bundle the code _intelligently_. This means modules that are natively available on the Webtask platform will not be bundled, however modules that are not available will.

## Usage

`npm run start` - Start the project as a typical express server.

`npm run build` - Will generate a development build of the webtask's code so that you can inspect it. Webpack is pre-configured to support a wide variety of things.

`npm run deploy-webtask` - First creates a production build of your webtask code and then uses the `wt-cli` command to create a webtask (**note: requires `wt-cli`**).

## Issue Reporting

If you have found a bug or if you have a feature request, please report them at this repository issues section. Please do not report security vulnerabilities on the public GitHub issue tracker. The [Responsible Disclosure Program](https://auth0.com/whitehat) details the procedure for disclosing security issues.

## Author

[Auth0](auth0.com)

## License

This project is licensed under the MIT license. See the [LICENSE](LICENSE) file for more info.
