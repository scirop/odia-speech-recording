**Odia Speech Recording** is a small web application to collect short snippets
of speech, and upload them to cloud storage. It's designed to help gather open
speech data sets to train machine learning systems, specifically in the Odia language.

The entire framework and most of the readme has been copied from Mr. Pete Warden's [work](https://github.com/petewarden/open-speech-recording)

Minor edits for accommodating Odia words have been made by Swarup Sahoo (swarupsahoo@utexas.edu)

It's based around a small Flask app that will run on Google App Engine. This
serves up a client-side Javascript app that prompts for a series of words,
records the audio, and then POSTs the results back to the server.

## Running

To get started, you'll need to edit app.yaml to point to your own storage bucket
and update the session key. If you have the Google Cloud SDK set up, you should
be able to run a local copy with this command:

```
dev_appserver.py app.yaml
```

I've often had trouble getting local copies of the app to work with cloud
storage, so you may see errors on the final upload stage with this setup. To
deploy it to an appspot instance, run this:

```
gcloud app deploy
```

## Credits

Origially written by Pete Warden, pete@petewarden.com.
