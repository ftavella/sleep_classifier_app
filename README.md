# sleep_classifier_app

This Flutter app runs a TFLite model on CSVs of spectrogram data. The spectrogram should be derived from accelerometer data (re)sampled at 32 Hz. See [the original model's page](https://github.com/MADSOLSEN/SleepStagePrediction), and Arcascope's [pisces project](https://github.com/Arcascope/pisces) for more information about creating this model, [finetuning it on Apple watch data](https://github.com/Arcascope/pisces/pull/9) co-recorded with PSG, and more.

## Getting Started

You will need Flutter 3.19.6+, and to follow some [start up directions with `tflite_fltuter`](https://pub.dev/packages/tflite_flutter). Specifically, you'll need to [build the TensorFlow C library](https://www.tensorflow.org/lite/guide/build_cmake) and add them to the appropriate per-platform projects. The saved model weights from our finetuning are available in `assets/`; these are distributed under the same license as this repository, and were derived from the [orignal open weights](https://github.com/MADSOLSEN/SleepStagePrediction/tree/master/models/pretrained_weights), as [shared in 2022](https://github.com/MADSOLSEN/SleepStagePrediction/commit/05d2d6e5a560e9dd53e5af4a6c39a6c2f30d9ff8).