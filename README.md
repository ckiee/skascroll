# skascroll

add scroll buttons for pages (WebExtension)

- firefox mobile intended, but others may work.
- project template: https://github.com/samrum/vite-plugin-web-extension
- quite bare
- the interesting file is `src/entries/contentScript/primary/App.svelte`

## how use,, (dev)

```
npm i
```

now these in parallel:

```
npm run watch
```

```
web-ext run --target=firefox-android --source-dir dist
    Applying config file: ./package.json
    Running web extension from /home/ckie/git/skascroll/dist

    Android devices found:
    - XXXXXXXXXXX

    UsageError: Select an android device using --android-device=<name>

web-ext run --target=firefox-android --source-dir dist --android-device=XXXXXXXXXXX
```

u can edit the code now and it should just reload

## license

see `LICENSE` file, it's MIT.
