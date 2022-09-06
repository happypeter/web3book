## build

```
yarn
./node_modules/.bin/honkit build
```

and now your html verion of the book is in `_book/`, now you can deploy it to your Github Pages locations, here is /docs/

```
rm -rf docs/
mv _book docs
```

NOTE: gitbook is now sort of deprecated.
