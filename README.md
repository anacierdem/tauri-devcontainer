# Tauri devcontainer setup

Very basic devcontainer setup for running headful Tauri. Works with Linux & MacOS.

### Run the app

    npm run tauri dev

## Compatibility

| Host OS | Basic support | HW acceleration | Audio |
| --- | ----------- | --- | --- |
| Fedora | ✅ | ✅ | Pulse Audio |
| Ubuntu | TODO | TODO | TODO |
| Windows | TODO | TODO | TODO |
| MacOS (x86) | TODO | ❌ | ❌ |
| MacOS (ARM) | TODO | ❌ | ❌ |

### Access to your host files

By default devcontainer have your host homes attached at `/var/home`. You can use this location to copy/link any important configurations you have for your user into the container's `/home/node`. You can use [`dotfiles`](https://code.visualstudio.com/docs/devcontainers/containers#_personalizing-with-dotfile-repositories) to do so.

Out of the box, devcontainer will also create a volume for the container user (i.e `home/node`) so that it can persist bash history and such across container recreations.