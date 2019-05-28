# Signal Conversation Archive Backup
Forked from https://github.com/mattsta/signal-backup
Use to extract messages from Signal desktop client.

## Usage
First clone and install requirements (preferably into a virtualenv):
```
git clone https://github.com/carderne/signal-backup.git
cd signal-backup
pip install -r requirements.txt
```

Then use the script as follows:
```
Usage: scab.py [OPTIONS]

Options:
  --path PATH  Signal directory (on Linux it's ~/.config/Signal/)
  --cont PATH  Output contacts JSON file
  --conv PATH  Output conversation JSON file
  --html PATH  Output HTML file
  --help       Show this message and exit.
```

Then either open the output html file in a browser, or do something with the JSON files.

## Troubleshooting
If you run into issues with `pysqlcipher3`, do as follows to fix:
```
sudo apt update
sudo apt install libsqlcipher-dev
git clone https://github.com/carderne/pysqlcipher3.git
cd pysqlcipher3
python setup.py install
```

