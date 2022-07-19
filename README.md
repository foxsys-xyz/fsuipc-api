<br/>

<img align="left" src="./public/img/Logo [Dark Background].svg" width="64" />

<br/><br/><br/>

## foxsys-xyz \\ x-crew
The main foxsys-xyz application. Still a work in progress.

## installation
```sh
$ yarn add @fsuipc/api
```

## complete example

```typescript
import { FsuipcApi } from '@fsuipc/api';

const fsuipcApi = new FsuipcApi(Simulator.FSX);

fsuipcApi.init().then(() => {
  fsuipcApi.listen(1000, [
    'gs',
    'altitude',
    'comFreq',
    'lights',
  ]).subscribe((result) => {
    // Use the result here
    console.log(JSON.stringify(result));
  });
}).catch((e) =>
  console.error(e)
);
```
