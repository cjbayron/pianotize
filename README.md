# audiate

<p align="center">
  <img src="assets/audiate.png" />
</p>

Ear training game using machine learning (ML/AI) models in the browser

---

#### :trophy: This project is a winning entry to [AIPilipinas](https://aipilipinas.org/) (AI Philippines) TensorFlow Project Showcase 2020-2021!

## About

Audiate, stylized **a**ud**i**ate, is a *play-what-you-hear* type of game wherein you are tasked to repeat the sequence of notes that the app plays, using the instrument of your choice. It aims to test (& train through practice) one's musical memory and relative pitch.

## How It Works

This app runs in your web browser and you can interact with it using the sound of your instrument, fed through your device's microphone. The captured audio is fed to a pitch transcription model running in the browser which transcribes the notes you played, and then checked if matches with the reference notes that the app instructed you to play. Using the transcription model eliminates the need for music interfaces such as MIDI as it can extract the pitch information from plain audio.

Watch [this](https://www.youtube.com/watch?v=VZ3i4V7i7Iw) for a simple demo :)

### Usage Notes

App has been tested to work well in **Chrome** in **Ubuntu**. In **some** tests, Windows 10 and Android Q (yes, on phone) can work too. Note also that the pitch transcription model may not transcribe pitch with 100% accuracy, especially on noisy environments.

You may try the app in the [GitHub pages](https://cjbayron.github.io/audiate/) or on your local machine by cloning this repository and serving the app, for example, via `python`:
```
$ python -m http.server 5000
```

### Development

This app makes use of a pre-trained pitch tracker model, [CREPE](https://github.com/marl/crepe). With only 2MB model size, it can run without hogging much of your device's resources.

An earlier version of **a**ud**i**ate, called *pianotize*, is also available in another [branch](https://github.com/cjbayron/audiate/tree/onsets-and-frames). It makes use of the [Onsets & Frames](https://magenta.tensorflow.org/onsets-frames) piano transcription model but is a lot slower and less accurate for this type of application.

## Libraries used

* [TensorFlow.js](https://github.com/tensorflow/tfjs)
* [Magenta.js](https://github.com/magenta/magenta-js) (old model)
* [Tone.js](https://tonejs.github.io/)
* [Tonal.js](https://github.com/tonaljs/tonal)
* [P5.js](https://p5js.org/)
