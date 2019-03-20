# Platform API Client Template

This project can be used as a template for building TypeScript/JavaScript clients for OpenAPI 3.0 compatible APIs

## Generating API client

1. Fork this repository
1. Modify package.json
    * change name, version, description, keywords and repository sections as appropriate
    * modify `SPEC` assignment in scripts section to point to the OpenAPI specification
1. Run `npm run generate:prod` to generate ts files
1. Run `npm run build` to build dist files

## Using generated client locally

1. In the client repository run `npm link`
1. In the consuming application run `npm link @redhat-cloud-services/<client name>`

## Publishing to npm

After the changes are tested, commited and tagged run `npm publish`.

## Known issues

* https://github.com/OpenAPITools/openapi-generator/issues/2154
  * worked around in [postProcess.sh](./postProcess.sh)
* https://github.com/OpenAPITools/openapi-generator/issues/1714
  * worked around by skipping spec validation in [package.json](./package.json)
