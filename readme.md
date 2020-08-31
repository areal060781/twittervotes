# Twitter votes
Terminal application that casts votes on Twitter, by making use of its REST API.
This app configure which hashtags are going to be monitored and it will automatically, from time to time, fetch the latest
tweets matching that hashtag, count them and display them in a user interface.

### Setup
```shell
cd twittervotes
python3 -m venv venv
. twittervotes/bin/activate
pip install -r requirements.txt
```