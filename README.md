# td-agent on Heroku

This repository contains whole stack to run td-agent on Heroku platform. [HTTP plugin](http://fluentd.org/doc/plugin.html#http) is used to receive the streaming logs.

### 1) Clone this repository

    $ git clone git://github.com/treasure-data/heroku-td-agent.git

### 2) Heroku

    $ heroku create --stack cedar
    $ git push heroku master

### 3) Set your API key

    $ vi td-agent.conf

### 4) Test

    $ curl "http://td-agent-on-heroku.herokuapp.com/debug.test?json=%7B%22json%22%3A%22message%22%7D"
    $ curl "http://td-agent-on-heroku.herokuapp.com/td.sample_db.sample_table?json=%7B%22json%22%3A%22message%22%7D"