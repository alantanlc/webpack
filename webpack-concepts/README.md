# Webpack Concepts

Webpack is a _static module bundler_ for modern JavaScript applications. Webpack internally builds a _dependency graph_ which maps every module your project needs and generates one or more _bundles_.

# Core Concepts

1. Entry
1. Output
1. Loaders
1. Plugins
1. Mode
1. Browser Compatibility

# Entry

Entry point (file) that webpack should use to begin building out the internal dependency graph. Default value is `./src/index.js`. Specify a different (or multiple entry points) by setting the `entry` property in the webpack configuration file.

# Output

Where to emit the _bundles_ created and how to name these files. Defaults to `./dist/main.js` for the main output file and to the `./dist` folder for any other generated file.

Configure by specifying an `output` field in the webpack configuratino file.

# Loaders

Used to process other types of files (besides JavaScript and JSON files) and convert them into valid modules that can be consumed by your application and added to the dependency graph.

At a high leve, __loaders__ have two properties in the webpack configuration

1. The `test` property identifies which file or files should be transformed.
2. The `use` property indicates which loader should be used to do the transforming.

# Plugins

To perform a wider range of tasks like bundle optimization, asset management and injection of environment variables.

To use a plugin, need to declare a plugin using `require()` and add a new plugin instance (using `new`) to the `plugins` array.

# Mode

Set `mode` to either `development`, `production`, or `none`. Default value is `production`.
