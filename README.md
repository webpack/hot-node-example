# hot-node-example

Example for very simple Hot Module Replacement with webpack.

## Running the app with HMR

```
npm install
npm run hot

# in a new terminal
npm start
```

## Running the app without HMR

```
npm run build
npm start
```

## Real app

In a real application you should do this things too:

* Put any normal node.js module in `externals` config
  * For performance
  * Not all node.js modules can be bundled
  * Specify `output.libraryTarget: "commonjs2"` to default to import by require.
* Use `webpack/hot/signal` instead of polling
  * Send a signal to the process to trigger the HMR
* Enable SourceMaps and source-map-support for node.js
* Handle the case when a hot update fails, i. e. because of errors or not accepted modules


