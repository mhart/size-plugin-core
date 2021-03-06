# size-plugin-core

Core module for [size-plugin](https://github.com/GoogleChromeLabs/size-plugin)/[rollup-plugin-size](https://github.com/luwes/rollup-plugin-size)

## Options

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### Table of Contents

-   [SizePluginCore](#sizeplugincore)
    -   [Parameters](#parameters)
-   [Item](#item)
    -   [Properties](#properties)
-   [Data](#data)
    -   [Properties](#properties-1)

### SizePluginCore

`SizePluginCore(options)`

#### Parameters

-   `options` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** 
    -   `options.compression` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?** compression method(gzip/brotli) to use, default: 'gzip'
    -   `options.pattern` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?** minimatch pattern of files to track
    -   `options.exclude` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?** minimatch pattern of files NOT to track
    -   `options.filename` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?** file name to save filesizes to disk
    -   `options.publish` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)?** option to publish filesizes to size-plugin-store
    -   `options.writeFile` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)?** option to save filesizes to disk
    -   `options.mode` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)?** option for production/development mode
    -   `options.columnWidth` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)?** option for add spacing in message
    -   `options.stripHash` **[function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)?** custom function to remove/normalize hashed filenames for comparison

### Item

#### Properties

-   `name` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Filename of the item
-   `sizeBefore` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** Previous size, in kilobytes
-   `size` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** Current size, in kilobytes
-   `sizeText` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Formatted current size
-   `delta` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** Difference from previous size, in kilobytes
-   `deltaText` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Formatted size delta
-   `msg` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Full item's default message
-   `color` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** The item's default CLI color

### Data

#### Properties

-   `sizes` **[Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Item](#item)>** List of file size items
-   `output` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Current buffered output
