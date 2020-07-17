<h1 align="center">FolderClone-Telegram-Bot 🔥</h1> 

<p align="center">
<a href="https://sawankumar.gitlab.io/"><img alt="author" src="https://img.shields.io/badge/author-Sawan%20Kumar-red"/></a>
<a href="https://www.python.org/"><img alt="language" src="https://img.shields.io/badge/Made%20with-Python-1f425f.svg"/></a>
<a href="https://github.com/ellerbrock/open-source-badges/"><img alt="author" src="https://badges.frapsoft.com/os/v1/open-source.svg?v=103"/></a>
</p>

<hr>


> ## FolderClone: A project that allows you copy large folders to Shared Drives.

## Deploy on Heroku

1. Fork this repository.
2. Then clone your repository.
```
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
```
3. Follow this [repository](https://github.com/xyou365/AutoRclone) to generate service accounts.
4. Put all your service accounts (JSON Files) in `accounts` folder.
5. Edit the values in `config.py`.
6. Now open `app.json` file and change it as per the instructions in `line 4` and `line 7` and `line 35` in `README.md`.
```
YOUR_UERNAME - Replace this with your github username.
```
```
YOUR_REPOSITORY_NAME - Replace this with your github repository name.
```
6. Push the files to your github repository.
7. Use `Deploy To Heroku Button`

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/YOUR_UERNAME/YOUR_REPOSITORY_NAME/tree/master)


## Usage in telegram bot
`/folderclone <source_id> <dest_id> <thread> <view> <skip>`

`source_id` - Drive ID of the folder you want to copy from. (Required)

`dest_id` - Drive ID of the folder you want to copy into. (Required)

`thread` - Amount of threads to use. The higher the more resource it requires. Default - 25

`view` - 0 - Tree View. 1 - Basic View. Default - Tree View.

`skip` - ID of the folder to skip to. Default - None. 

## Details about skipping
This is for those that host bot on heroku. Since heroku recycle their dyno approximately every 24 hr, things might stop halfway during cloning.

Folder IDs are printed along side with the normal progress so you can use it for the skip parameter.

Delete all the files within the folder of which the process stopped at first before cloning again. (So that you won't get duplicates)

You need to specify the rest parameter if you want to use the skip parameter.

Example : `/folderclone FSAF3213FD3S2341 FSAF3213FD3S2342 25 0 FSAF3DE45D3S2356`

### Note
`folderclone.py` - Modified version of `multifolderclone.py` from [Multifolderclone](https://github.com/justcopy/Multifolderclone).

## Thanks to :heart:

- [Loli Killer](https://github.com/Loli-Killer/TgFolderClone)