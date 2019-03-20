# Remediations Client

TypeScript client for [Remediations API](https://access.redhat.com/r/insights/platform/remediations/v1/openapi.json) generated using [openapi-generator](https://github.com/OpenAPITools/openapi-generator).

## Usage

```sh
npm i --save remediations-client
```

```js
import { RemediationsApi } from '@redhat-cloud-services/remediations-client';

const api = new RemediationsApi();
const remediations = await api.getRemediations();
```

## Known issues

* https://github.com/OpenAPITools/openapi-generator/issues/2154
  * worked around in [postProcess.sh](./blob/master/postProcess.sh)
* https://github.com/OpenAPITools/openapi-generator/issues/1714
  * worked around by skipping spec validation in [package.json](./blob/master/package.json)
