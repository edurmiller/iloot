iLoot
=====

Using this CLI tool you can download backups of devices assigned to your AppleID. Based on [iphone-dataprotection](https://code.google.com/p/iphone-dataprotection/) script, so copyrights belong to respective owners. Offset operations added and other minor bugs fixed. Thanks to [dlo](https://github.com/dlo) for his additions.

Download you iCloud Backups Recovery here [www.myicloudbackup.com](https://www.myicloudbackup.com/)

**This tool is for educational purposes only. Before you start, make sure it's not illegal in your country.**

Follow us on twitter [@hackappcom](https://twitter.com/hackappcom)  and [facebook](https://www.facebook.com/groups/1480690882187595/)

Hackapp [blog](blog.hackapp.com)

Mobile Applications Scanner [hackapp.com](https://hackapp.com)

Requirements
============

```bash
pip install -r requirements.txt
```

Example
======

```bash
$ python iloot.py -h
usage: iloot [-h] [--output OUTPUT] [--combined] [--snapshot SNAPSHOT]
             [--itunes-style] [--item-types ITEM_TYPES [ITEM_TYPES ...]]
             [--domain DOMAIN]
             apple_id password

positional arguments:
  apple_id              Apple ID
  password              Password

optional arguments:
  -h, --help            Show this help message and exit.
  --output OUTPUT, -o OUTPUT
                        Output directory.
  --combined            Do not separate each snapshot into its own folder
  --snapshot SNAPSHOT   Only download data the snapshot with the specified ID.
                        Negative numbers will indicate relative position from
                        newest backup, with -1 being the newest, -2 second,
                        etc.
  --itunes-style        Save the files in a flat iTunes-style backup, with
                        mangled names.
  --item-types ITEM_TYPES [ITEM_TYPES ...], -t ITEM_TYPES [ITEM_TYPES ...]
                        Only download the specified item types. Options
                        include address_book, calendar, sms, call_history,
                        voicemails, movies and photos. E.g., --types sms
                        voicemail
  --domain DOMAIN, -d DOMAIN
                        Limit files to those within a specific application
                        domain
```

By default, the tool will download everything in a backup. If you'd only like to download a specific item type (such as all SMSs), just specify the `--item-types` argument. For instance:

```bash
python iloot.py <appleID> <password> --item-types sms call_history voicemails
```

![iLoot](https://raw.githubusercontent.com/hackappcom/iloot/master/iloot.png "iloot")

