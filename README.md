# Real Time Whisper Transcription

This is a POC app to transcribe speech, and fire automations on a Mac. 

It works by constantly recording audio in a thread and concatenating the raw bytes over multiple recordings, then running parameterized applescript commands. 

## Installation

### Environment Setup

Some of the packages aren't compatible with the newest version of python.

I recommend starting with pyenv to install python 3.11

```
pyenv install 3.11.5
pyenv local 3.11.5
python --version 
```

If that comes back with anything other than 3.11, make sure you add this to your aliases and source them, or run this directly in your terminal.

```
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
```

Set up a virtual env with
```
python -m venv env
source env/bin/activate
```

### Package Installation

Install pyaudio
```

```

Then, to install dependencies simply run
```
pip install -r requirements.txt
```
in an environment of your choosing.

Whisper also requires the command-line tool [`ffmpeg`](https://ffmpeg.org/) to be installed on your system, which is available from most package managers:

```
brew install ffmpeg
```

For more information on Whisper please see https://github.com/openai/whisper

The code in this repository is public domain.

## Usage

First, make sure you're preferred microphone is set as the default in Mac "Sound Input".

After setting up the environment and packages, you can start the app with
```
python transcribe_demo.py
```

Each time you come back, you'll want to make sure you have the venv loaded:
```
pyenv local 3.11.5
source env/bin/activate
```