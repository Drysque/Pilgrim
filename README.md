# Pilgrim

Versioning for all the files scattered on your pc that you want to backup.

Save your shells configurations files in one place and push it to a private remote.

### Disclaimer

Don't actually use this.<br />
This is a project done during my spare time to uncover the `argparse` module.

## Usage

```
pilgrim.py [-h] [-r path] [--debug] [-y] [-v] [-s] [-d] [--add file [file ...]] [--commit [message]] [-p]

Versioning for all your backups

optional arguments:
  -h, --help                    show this help message and exit
  -r path, --repository path    path of repository where backups are. Default: ~/.pilgrim
  --debug                       print parsing results and exits
  -y, --yes                     skips confirmation
  -v, --verbose                 be verbose
  -s, --status                  perform a status check
  -d, --diff                    perform a diff
  --add file [file ...]         files to add
  --commit [message]            perform a commit with a message (optional)
  -p, --push                    perform a push to remote
```


Check the repo status and add a file:<br />
`pilgrim -s --add ./importantFile ../config `<br />
Check the work done and commit it:<br />
`pilgrim -d --commit "Added important backup files"`<br />
Push to the remote:<br />
`pilgrim --push`<br />


# Pilgrim on an everyday basis

`pilgrim -py --add ./importantFile --commit`<br />
This will add a file to the repo and push it to the remote with a default commit message.<br />
It won't ask for confirmation.<br />
