# xviz-data

```bash
 npm install http-server -g
 http-server --cors .
```

## Using in xviz

```js
import {XVIZFileLoader} from 'streetscape.gl';

export default new XVIZFileLoader({
  timingsFilePath:
    'http://127.0.0.1:8081//2011_09_26_drive_0001_sync/0-frame.json',
  getFilePath: index =>
    `http://127.0.0.1:8081/2011_09_26_drive_0001_sync/${index +
      1}-frame.glb`,
  worker: true,
  maxConcurrency: 4
});
```