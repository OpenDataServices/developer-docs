# jq

https://stedolan.github.io/jq/

## Useful examples

Concatenating multiple files of OCDS releases into one file:

```bash
jq -s '{"releases": [.[].releases[]]}' *.json
```
