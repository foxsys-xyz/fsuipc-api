<br/>

<img align="left" src="https://github.com/foxsys-xyz/fsuipc-api/raw/master/public/logoLight.svg" width="64" />

<br/><br/><br/>

## foxsys-xyz \\ fsuipc-api
an fsuipc api to track simulator events via x-track which works on node. based on @fsuipc/api 🔗

## installation
```sh
$ yarn add @foxsys-xyz/fsuipc-api
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
