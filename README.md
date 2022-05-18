# Flutter v2 VS Remote - Development Container using Docker

A Dockerfile & config for developing with [Flutter](https://flutter.dev/) and 
the [VS Remote - Containers](https://code.visualstudio.com/docs/remote/containers) 
extension. 

- This project includes zsh as default shell with autocompletion, and a light-weight shell theme. (Check `~/.zshrc` inside the container for more info).
- Please remember, you won't have sudo/root access inside the container.

## Usage

* Install [`ms-azuretools.vscode-docker`](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) extension from vscode marketplace on vscode.
* Clone this repository `git clone https://github.com/predatorx7/flutterv2-vscode-devcontainer.git`
* Optionally, Copy all files from here and paste it in your flutter android project's root. 
* Open it in VS Code `code .`. 
* Click 'Re-open in container' when prompted
* Wait for downloads to complete (this can take a while for the first time, it downloads java, android SDK
and flutter)
* Once the container has started, you can run either `flutter create hello_world` to create a 
new project, clone your source from a repo or work on the files in the mounted workspace if you had copied anything.
* Running on a physical device is supported with `flutter run`, make sure you click the 
dialog on the device in order to trust the computer you are connecting from! (Don't forget to enable file transfer).
* On MacOS or Windows, you might have to use wireless debugging if usb doesn't work.

## Notes

Please note that this container is set to run in 
[privileged mode](https://docs.docker.com/engine/reference/run/#runtime-privilege-and-linux-capabilities) 
in order to access USB devices on the host machine. You should be aware of the security 
implications of this.

Please note when you use this container you're automatically agreeing to the 
[Android SDK terms & conditions](https://developer.android.com/studio/terms)
