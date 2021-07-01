# test-del-cli
> Cross-platform CLI example for deleting files and folders

To delete files in the "results" folder, execute NPM script

```shell
$ npm run delete
```

The script in [package.json](./package.json) uses [del-cli](https://github.com/sindresorhus/del-cli) to delete files. Make sure to pass the wildcards using quotes to let the `del-cli` find the files.

```json
{
  "scripts": {
    "delete": "del-cli 'results/*'"
  },
}
```

If you want to use `del-cli` without NPM package script command, simply use NPX

```shell
$ npx del-cli 'results/*'
```

Note: if there are no files matching the pattern, `del-cli` exits with code 0
