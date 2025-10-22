# SChat [![Discord](https://img.shields.io/discord/1196075698301968455?style=social&logo=discord&label=Soncresity-Industries)](https://discord.gg/uqbQvAHHve)
A mod for Discord's mobile apps.

## Installing

### Android

- **Root** with Xposed - [SChatXposed](https://github.com/Soncresity-Industries/SChat-Xposed/releases/latest)
- **Non-root** - [SChatManager](https://github.com/Soncresity-Industries/SChat-Manager/releases/latest)

### iOS
- [**SChatTweak**](https://github.com/Soncresity-Industries/SChat-Tweak) - Get prebuilt rootful and rootless `.deb` files or the prepatched `.ipa `

## Building
1. Install a SChat loader with loader config support (any mentioned in the [Installing](#installing) section).
1. Go to Settings > General and enable Developer Settings.
1. Clone the repo:
    ```
    git clone https://github.com/Soncresity-Industries/SChat
    ```
1. Install dependencies:
    ```
    pnpm i
    ```
1. Build SChat's code:
    ```
    pnpm build
    ```
1. In the newly created `dist` directory, run a HTTP server. I recommend [http-server](https://www.npmjs.com/package/http-server).
1. Go to Settings > Developer enabled earlier. Enable `Load from custom url` and input the IP address and port of the server (e.g. `http://192.168.1.236:4040/schat.js`) in the new input box labelled `SChat URL`.
1. Restart Discord. Upon reload, you should notice that your device will download SChat's bundled code from your server, rather than GitHub.
1. Make your changes, rebuild, reload, go wild!

Alternatively, you can directly *serve* the bundled code by running `pnpm serve`. `schat.js` will be served on your local address under the port 4040. You will then insert `http://<local ip address>:4040/schat.js` as a custom url and reload. Whenever you restart your mobile client, the script will rebuild the bundle as your client fetches it.

> [!IMPORTANT]
> This repo has been forked from the @bunny-mod/Bunny Repo.
> This project is merely a continuation of the original Software just under a different name and more features that we have planned for the future.
> As such all credit goes to the anazing creators of Bunny and BunnyTweak.
> **This project is licensed under the BSD License (BSD)**