Flask_ML

Demo of serving Transformer models over Flask:

App serves summaries of Wikipedia articles' introductory sections.
The summaries are by BART or T5. We can specify the Wikipedia article name.
Article min and max length may also be specified.

One notebook sets up the Flask server and provides the summarization code.
It also uses the Python Wikipedia package to get the intro sections of the pages asked for.

The other notebook uses the Python requests package to send POST requests
to get the summaries.

These work fine on a local machine with a localhost. Unfortunately, they do not work as is on Colab as each file would have a separate VM. 

Then you need ngrok_flask rather than flask to serve
the pages but that is just the beginning of a can of worms. You also need ngrok to
allow you to serve as if you were a web server. But ngrok requires a signup and then
an authorization token. Each token the ngrok software also needed to be downloaded,
unzipped, and then reinstalled. That was all too much trouble at that point, as this is
all just a demo anyway, showing what could ultimately be run behind a real webserver anyway!
