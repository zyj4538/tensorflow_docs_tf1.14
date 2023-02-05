page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# Module: tf.contrib.signal

Signal processing operations.



Defined in [`contrib/signal/__init__.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/signal/__init__.py).

<!-- Placeholder for "Used in" -->

<a href="../../tf/contrib/signal"><code>tf.contrib.signal</code></a> has been renamed to <a href="../../tf/signal"><code>tf.signal</code></a>. <a href="../../tf/contrib/signal"><code>tf.contrib.signal</code></a> will be
removed in TensorFlow 2.0.

See the
[Contrib Signal](https://tensorflow.org/api_guides/python/contrib.signal)
guide.


[hamming]: https://en.wikipedia.org/wiki/Window_function#Hamming_window
[hann]: https://en.wikipedia.org/wiki/Window_function#Hann_window
[mel]: https://en.wikipedia.org/wiki/Mel_scale
[mfcc]: https://en.wikipedia.org/wiki/Mel-frequency_cepstrum
[stft]: https://en.wikipedia.org/wiki/Short-time_Fourier_transform

## Functions

[`frame(...)`](../../tf/signal/frame): Expands `signal`'s `axis` dimension into frames of `frame_length`.

[`hamming_window(...)`](../../tf/signal/hamming_window): Generate a [Hamming][hamming] window.

[`hann_window(...)`](../../tf/signal/hann_window): Generate a [Hann window][hann].

[`inverse_stft(...)`](../../tf/signal/inverse_stft): Computes the inverse [Short-time Fourier Transform][stft] of `stfts`.

[`inverse_stft_window_fn(...)`](../../tf/signal/inverse_stft_window_fn): Generates a window function that can be used in `inverse_stft`.

[`linear_to_mel_weight_matrix(...)`](../../tf/signal/linear_to_mel_weight_matrix): Returns a matrix to warp linear scale spectrograms to the [mel scale][mel].

[`mfccs_from_log_mel_spectrograms(...)`](../../tf/signal/mfccs_from_log_mel_spectrograms): Computes [MFCCs][mfcc] of `log_mel_spectrograms`.

[`overlap_and_add(...)`](../../tf/signal/overlap_and_add): Reconstructs a signal from a framed representation.

[`stft(...)`](../../tf/signal/stft): Computes the [Short-time Fourier Transform][stft] of `signals`.

