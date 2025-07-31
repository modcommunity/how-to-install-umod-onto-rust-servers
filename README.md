A guide on how to **download** and **install** [uMod](https://umod.org/) (formerly Oxide) onto your [Rust](https://rust.facepunch.com/) game server.

This guide should work for **Windows** and **Linux** users. The only differences between these operating systems within this guide are how folder and file paths are formatted and usage of terms like *folders* (Windows) and *directories* (Linux).

[**View Guide On TMC (Recommended Due To Better Formatting)**](https://blog.moddingcommunity.com/how-to-install-umod-onto-rust-servers/)

Adding uMod to your Rust server will allow you to install many mods and plugins onto your server! There is a wide range of Rust plugins for uMod available [here](https://umod.org/plugins?page=1&sort=title&sortdir=asc&categories=rust).

## Table of Contents
* [Requirements](#requirements)
* [Back Up Your Server Files & Saves](#back-up-your-server-files--saves)
* [Downloading uMod](#downloading-umod)
* [Installing uMod](#installing-umod)
* [Restart Your Rust Server & Test](#restart-your-rust-server--test)
* [Troubleshooting](#troubleshooting)
    * [Ensure Files Copies Properly](#ensure-files-copies-properly)
    * [File Permissions (Linux)](#file-permissions-linux)
* [Conclusion](#conclusion)
* [See Also](#see-also)

## Requirements
* A Rust game server you can connect to
* Access to upload or move files on the Rust server (e.g., SFTP/FTP clients such as [FileZilla](https://filezilla-project.org/))
* A program to uncompress and extract files from an archive (e.g., [7-Zip](https://www.7-zip.org/))

## Back Up Your Server Files & Saves!
Although it is very unlikely installing uMod onto your server will cause issues with your map saves, we still recommend **backing up** your server files and map servers!

You should back up the entire server identity which is located at `server/<my server name>` from within your Rust game server files.

## Downloading uMod
1. Head to [this](https://umod.org/games/rust) web page and click the **Download** button ([direct download link](https://umod.org/games/rust/download?tag=public)).
2. Save the compressed file and archive to a location on your PC (e.g. your `Downloads` folder or your desktop).

By now, you should have a single compressed file stored on your PC or server that contains the uMod files in it.

## Installing uMod
1. Use a tool like [7-Zip](https://www.7-zip.org/) to uncompress and extract files and folders from the downloaded archive.
    * On Linux, you can use the `tar` or `unzip` commands depending on the archive type to extract the uMod folders and files!
    * By now, you should have a folder on your PC with the uMod files and folders that need to be merged with your server's files.
2. Copy or transfer the `RustDedicated_Data` folder from extracted uMod folders into your server's main directory.
    * You should be merging this folder with the `RustDedicated_Data` folder in your server's install files.

## Restart Your Rust Server & Test
It's time to now restart your Rust server and check if uMod is loading properly.

You should have access to the server's console and if you perform the command `oxide.version`, it should respond with the version of uMod on the server.

If the command responds back with a message saying the command is unknown, then uMod did not install properly.

## Troubleshooting
### Ensure Files Copies Properly
Make sure you copied the uMod folders and files properly.

1. Go to your server's game files folder.
2. Navigate to the `RustDedicated_Data\Managed\` folder and check if see files that have `Oxide` in them.

If you don't have any files with `Oxide` in the name, you didn't copy the uMod folders and files over properly.

### File Permissions (Linux)
If you're facing issues on Linux, it's possible you're running into issues related to file permissions.

1. Navigate to your server's game files directory.
2. Ensure the new uMod files in the server directory are owned by the user running under the server.
    * You can also just perform `chown -R <user>:<group> RustDedicated_Data` to change permissions on all directories and files inside of the server directory.
    * Most files should have `644` permissions.

## Conclusion
That's it! By now, you should have uMod running on your server.

We'd recommend giving the uMod documentation a read [here](https://umod.org/documentation). Additionally, you may read more Rust server guides on our website or from the official uMod website [here](https://umod.org/guides).

## See Also
* [uMod Rust Plugins](https://umod.org/plugins?page=1&sort=title&sortdir=asc&categories=rust)
* [uMod Documentation](https://umod.org/documentation)
* [uMod Discord Server](https://discord.gg/HdhSD8aBXD)
* [uMod Community & Forum](https://umod.org/community)

This guide will be updated over time. If you see any ways to improve this guide, feel free to reach out!