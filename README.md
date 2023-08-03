# Audio-Analysis-and-Text-Summarization

Downloading the Audio Files:
As far as downloading goes, I tried using the beautifoulsoup, but I got a captcha error, so I used Selenium to get all the links, and then I used wget library to download all the audio files.
I used Google cloud speech API, and if we want to do speech to text for more than 1 minute, I have to store it in the GCP bucket and use the URI to do speech to text.

Run a EDA on the data set:
As this is my first time visualizing the Audio Dataset, I have tried to focus more on the frequency, amplitude, envelope, and decibel (intensity level). 
Several plots, such as the waveform, spectrogram, and Fourier Transform, were really useful.

Summarization:
I tried SpeechRecognition and DeepSpeech but didn't get better results, they are quite naive when compared to Google speech API. With the help of the Google Speech API, I was able to do this. However, I did encounter one limitation with the Google Speech API, it only supports speech-to-text conversion for audio files of up to 1 minute in duration. To overcome this constraint, I had to upload longer audio files to the Google Cloud Platform (GCP) bucket and then use the file's URI for processing.

Compute Talk Ratio:
It’s a good metric to know who's leading the conversation more respected to the speakers.

Emotions (Sentiment Analysis):
At the moment, I have used a basic sentiment analyzer using blob text. However, for enhanced accuracy and more precise results, we have the option to leverage advanced models like BERT or ChatGPT. By integrating these state-of-the-art models into our sentiment analysis pipeline, we can expect significant improvements in the sentiment classification process.

NER:
I used simple NER from scipy to do the POS tagging, however there could be other models that perform very well.

Silence %:
It could be a good feature in terms of cleaning and adjusting the parameters for audio feature extractions.
