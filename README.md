# LocalStackExchange

LocalStackExchange is free script that will copy and deploy a local version of any StackExchange server (stackoverflow, math, superuser, askubuntu, serverfault, etc.) into your machine.


Exemple:
* Raspberry Pi 4 with a 1 TB hard disk

## Features
* Start and continue the deployment script at any moment (download paused, etc.) even using CTRL-C
* Manage any StackExchange website ([listed here](https://archive.org/download/stackexchange))
* Download links, website, PDF, images in posts and comments for a full offline mode
* Links between posts, comments and more are working offline
* Custom your own HTML display or select available templates
* Homemade search engine for code (filter by keywords, tags, etc.)
* Local domain name setup options (in local you can re-route all stackoverflow links to the LocalStackExchange  server)

## Requierements
You will need at least:
* An internet connection (just for the downloading part)
* An Unix OS (not working on Windows, not even using WSL)
* A file system that can accept up to 4 billions files in a single directory
* For Stackoverflow only: 8 GB of RAM and 1 TB storage drive
* For Other servers sites: 4 GB of RAM and 500 GB storage drive

## Installation

Git clone

```bash
cd /path/to/my/harddrive/empty
git clone https://github.com/huguesdpdn/LocalStackExchange.git LocalStackExchange
cd LocalStackExchange
```

Open `sites.txt` with your favorite IDE or text editor
```bash
vi sites.txt
emacs -nw sites.txt
nano sites.txt
```

Add all websites or server you want to get in local. Example of the content of `sites.txt`:
```text
stackoverflow.com
https://archive.org/download/stackexchange/superuser.com
https://archive.org/download/stackexchange/raspberrypi.stackexchange.com.7z
```

Download, install and deploy:
```bash
downloadInstallDeploy.sh
```

## Advanced usage (NOT part of the installation chapter)
You can use the `--clean` option to restart from scratch. It will remove all download, unzipped files, HTML files, databases, and launch jobs. Use it only if you are sure that you want to reset the whole machine: 
```bash
downloadInstallDeploy.sh --clean
```


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
By Hugues DU POUGET DE NADAILLAC under [MIT license](https://choosealicense.com/licenses/mit/)
