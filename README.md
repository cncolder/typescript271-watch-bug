# typescript271-watch-bug

Run `npm start`.

The first time generated `index.js` like this:

```js
"use strict";
Object.defineProperty(exports, "__esModule", { value: true });
var lib = require("./lib");
exports.demo = function () {
    console.log(lib.seq);
};
```

Then edit `index.ts`. e.g. Press Enter at the end of file. Then save it. `tsc -w` will generate a new `index.js`:

```js
"use strict";
Object.defineProperty(exports, "__esModule", { value: true });
/* Pay attention at this line. The require statement disappeared. */
exports.demo = function () {
    console.log(lib.seq);
};
```
