# real-time-audio-transcription
Read wav audio files and get their audio chunks transcribed by Google Speech API in real time.

This program takes an audio file as an input and uses Google Speech API to output a text transcription.

# Requirements
## Node.js

version 5 and above should work

## A Google Speech API enabled project

The `GOOGLE_APPLICATION_CREDENTIALS` must be properly set and point to a
valid service account file.

If you need to get service account, you need to :
  - Create or select a project
  - Enable the Cloud Speech API for that project
  - Create a service account
  - Download a private key as JSON

And then et the environment variable GOOGLE_APPLICATION_CREDENTIALS to the
file path of the JSON file that contains your service account key.
More info here : https://cloud.google.com/nodejs/

# Usage
```
Usage: node ${basename(process.argv[1])} [options] filename

  finename                   Audio file to transcribe, a WAV container

Options:
  -l, --lang                 Transcription language code, e.g. : en-US, fr-FR.
                             Defaults to en-US.
  -c, --chunkduration        The duration in seconds of audio buffer to submit
                             to Google for transcription. Defaults to 10
                             seconds, and must not exceed 60 seconds.
  -d, --debug                debug mode
  -h, --help                 This help message
```
