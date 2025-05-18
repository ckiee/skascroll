# skascroll

**skascroll** is a browser WebExtension that adds scroll buttons to web pages, enhancing accessibility for individuals with repetitive strain injury and related conditions. It is primarily designed for Firefox Mobile ([addon link](https://addons.mozilla.org/en-US/firefox/addon/skascroll/)) but may also be compatible with other browsers.

- Based on the [vite-plugin-web-extension](https://github.com/samrum/vite-plugin-web-extension) template.
- The project is minimalistic, the main file is located @ `src/entries/contentScript/primary/App.svelte`.

## Development Setup

To set up the development environment, begin by installing the necessary npm packages:

```bash
npm install
```

Once the dependencies are installed, run the following commands in parallel to start the development process:

1. Begin watching for changes:

   ```bash
   npm run watch
   ```

2. Launch the web extension on a connected Android device running Firefox:

   ```bash
   web-ext run --target=firefox-android --source-dir dist
   ```

   Upon running the command above, you may encounter a message indicating available Android devices. Select a device using the following command:

   ```bash
   web-ext run --target=firefox-android --source-dir dist --android-device=<DeviceID>
   ```

   Replace `<DeviceID>` with the actual ID of your Android device (found in the error message from the last command)

With this setup, you can edit the code, and changes should automatically reload.

Raise an issue if you need help!

## License

This project is licensed under the MIT License. For more details, please refer to the `LICENSE` file.

