This repo is reproducing a napi-rs issue.

Steps:

1. git clone git@github.com:devongovett/napi-repro.git
2. cd napi-repro
3. yarn
4. yarn build

You may need to run it a few times to see an error.

You can also try linking this [source-map PR](https://github.com/parcel-bundler/source-map/pull/120) locally, which reproduces the error even more frequently.

1. git clone git@github.com:parcel-bundler/source-map.git
2. cd source-map
3. git checkout 236629338fafc6fe0c49f56eaa95dfbc068de4ec
4. yarn build:node-release
5. yarn link
6. cd path/to/napi-repro
7. yarn link @parcel/source-map
8. Repeat steps above.
