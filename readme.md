# Twitter votes
Terminal application that casts votes on Twitter, by making use of its REST API.
This app configure which hashtags are going to be monitored and it will automatically, from time to time, fetch the latest
tweets matching that hashtag, count them and display them in a user interface.

* **OAuth** authentication to consume data from the **Twitter API**
* Command-line parser using the **ArgumentParser** module
* Reactive programming using the **Rx** (Reactive Extensions for Python) module
* *concurrent.futures** module to enhance the performance, running multiple requests to the Twitter API in parallel
* User interface using the **Tkinter** module

**Requirements**
- [x] Virtualenv
- [x] [A Twitter developer account and a Twitter application](https://developer.twitter.com/en/portal/projects-and-apps)

### Setup
Inside the project folder, run the commands:
Create the virtual environment, activate it and install the dependencies
```shell
python3 -m venv venv
. twittervotes/bin/activate
pip install -r requirements.txt
```

Copy the configuration file
```shell
cp config-example config.yaml
```

Create an Twitter app on the Twitter developer page

Copy the consumer_key and consumer_secret to config.yaml

Hit ```python app.py``` to authorize and generate the .twitterauth file, close the browser and stop the server

### Run the application
```shell
python app.py --help
```

```
usage: twittervoting [-h] -ht HASHTAGS [HASHTAGS ...]

Collect votes using twitter hashtags.

optional arguments:
  -h, --help            show this help message and exit

require arguments:
  -ht HASHTAGS [HASHTAGS ...], --hashtags HASHTAGS [HASHTAGS ...]
                        Space separated list specifying the hashtags that will be used for the voting. Type the hashtags without the hash symbol.
```