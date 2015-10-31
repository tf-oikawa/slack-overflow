# slack-overflow

A programmer's best friend, now in Slack. Search StackOverflow right from Slack without coming off as dumb.

![](http://i.imgur.com/c9HuKw8.gif)

## Usage

From any Slack channel, just type `/overflow [search terms]`. The questions will be shown on the same channel visible just to you.

## Integrate with your team

1. Go to your channel
2. Click on **Configure Integrations**.
3. Scroll all the way down to **DIY Integrations & Customizations section**.
4. Click on **Add** next to **Slash Commands**.
  - Command: `/overflow`
  - URL: `http://{App Domain}/overflow`
  - Method: `POST`
  - For the **Autocomplete help text**, check to show the command in autocomplete list.
    - Description: `A programmer's best friend, now in Slack.`
    - Usage hint: `[search terms]`
  - Descriptive Label: `Search StackOverflow`

## Developing

Add a `config.py` file based on `config.py.example` file. Grab your StackExchange key from http://stackapps.com/

```python
# Install python dependencies
$ pip install -r requirements.txt

# Start the server
$ python app.py
```

## Deploy to Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

You will need to set the `SE_KEY` environment variable in your heroku app in order for this to work. You can read more about it [clicking here](https://devcenter.heroku.com/articles/config-vars#setting-up-config-vars-for-a-deployed-application)


## Contributing

- Please use the [issue tracker](https://github.com/karan/slack-overflow/issues) to report any bugs or file feature requests.
