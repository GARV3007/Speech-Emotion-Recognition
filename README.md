# Speech-Emotion-Recognition (SER)

Gourav Verma(\br)
DSC-680 302, Spring-2021(br)
GitHub Portfolio URL - TBD(br)

Which Domain?
Emotion recognition from speech signals has been research topic since many years. Among all the ways of communication speech signal is one of the fastest. Recognition of emotion is natura for humans but very difficult for machines. In this project I will be using Python programming language and relative packages to identify emotions of human speeches. 
For the study speech signals can be collected from Phone calls, Customer Services, Voice Chats, Public Speeches, Debates, Interviews, Songs, Teaching, Counselling, Public hearings.   
Which Data?
For this project I will be using data available from ZENODO.  The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS) contains 7356 files (total size: 24.8 GB). The database contains 24 professional actors (12 female, 12 male), vocalizing two lexically-matched statements in a neutral North American accent. Speech includes calm, happy, sad, angry, fearful, surprise, and disgust expressions, and song contains calm, happy, sad, angry, and fearful emotions. Each expression is produced at two levels of emotional intensity (normal, strong), with an additional neutral expression. All conditions are available in three modality formats: Audio-only (16bit, 48kHz .wav), Audio-Video (720p H.264, AAC 48kHz, .mp4), and Video-only (no sound). 

I will not be using whole 24.8 GB, instead a portion of the RAVDESS which contains 1440 files: 60 trials per actor x 24 actors = 1440. Data can be found at location: https://www.kaggle.com/uwrfkaggler/ravdess-emotional-speech-audio 


File naming convention
Each of the 1440 files has a unique filename. The filename consists of a 7-part numerical identifier (e.g., 03-01-06-01-02-01-12.wav). These identifiers define the stimulus characteristics:


Filename identifiers
•	Modality (01 = full-AV, 02 = video-only, 03 = audio-only).
•	Vocal channel (01 = speech, 02 = song).
•	Emotion (01 = neutral, 02 = calm, 03 = happy, 04 = sad, 05 = angry, 06 = fearful, 07 = disgust, 08 = surprised).
•	Emotional intensity (01 = normal, 02 = strong). NOTE: There is no strong intensity for the 'neutral' emotion.
•	Statement (01 = "Kids are talking by the door", 02 = "Dogs are sitting by the door").
•	Repetition (01 = 1st repetition, 02 = 2nd repetition).
•	Actor (01 to 24. Odd numbered actors are male, even numbered actors are female).

Filename example: 03-01-06-01-02-01-12.wav
1.	Audio-only (03)
2.	Speech (01)
3.	Fearful (06)
4.	Normal intensity (01)
5.	Statement "dogs" (02)
6.	1st Repetition (01)
7.	12th Actor (12)
8.	Female, as the actor ID number is even.

Research Questions? Benefits? Why analyzes these data?
Speech of human being is the most natural way of expression. Recognition of emotion was not felt so important till we were exposed to other communication form like text messages and emails. Emojis of often used to express the emotion associated with messages. SER system is collection of different methodologies that process and classify speech signals to identify their embedded emotions. 

We can categories features of speech into three classes namely, the lexical features (Vocabulary used), the visual features (expression of the speaker), and the acoustic features (properties of sound like pitch, tone, jitter etc.). In this project I will be performing emotion detection using acoustic features. This research will be capitalizing on the fact that voice often reflects underlying emotion through tone and pitch.

Applications
1.	SER (Speech Emotion Recognition) is used in call center for classifying calls according to emotions and can be used as the performance parameter for conversational analysis thus identifying the unsatisfied customer, customer satisfaction and so on. for helping companies improving their services

2.	It can also be used in-car board system based on information of the mental state of the driver can be provided to the system to initiate his/her safety preventing accidents to happen.

What Method?
Emotion recognition is the part of speech recognition which is gaining more popularity and need for it increases enormously. Although there are methods to recognize emotion using machine learning techniques, this project attempts to use deep learning to recognize the emotions from data.

librosa is a Python library for analyzing audio and music. It has a flatter package layout, standardizes interfaces and names, backwards compatibility, modular functions, and readable code.

I will load the data, extract features from it, then split the dataset into training and testing sets. Then, I will initialize an MLPClassifier and train the model. Finally, we will calculate the accuracy of our model.

Potential Issues?
I have never worked with Audio file for the analysis. This will be a challenging project and I am trying to make it interesting as well so that I will be able to complete it on time. 
Concluding Remarks
Speech Emotion Recognition, abbreviated as SER, is the act of attempting to recognize human emotion and affective states from speech. With recent advancements of Deep Learning, better hardware and more open sourcing of data, this enables us to build the capability that we couldn't before. For the research I am using a portion of the RAVDESS contains 1440 files. I will use the audio to generate a spectrogram and then use a neural network for images and pass the spectograms to the model.

References:
Livingstone SR, Russo FA (2018) The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS): A dynamic, multimodal set of facial and vocal expressions in North American English. PLoS ONE 13(5): e0196391. https://doi.org/10.1371/journal.pone.0196391.

Livingstone, S. (2019, January 19). RAVDESS emotional speech audio. Retrieved March 22, 2021, from https://www.kaggle.com/uwrfkaggler/ravdess-emotional-speech-audio 

Python mini project - Speech emotion recognition With librosa. (2021, March 14). Retrieved March 22, 2021, from https://data-flair.training/blogs/python-mini-project-speech-emotion-recognition/ 

Ingale, A. B., & Chaudhari, D. S. (2012). Speech emotion recognition. International Journal of Soft Computing and Engineering (IJSCE), 2(1), 235-238.

Huang, Z., Dong, M., Mao, Q., & Zhan, Y. (2014, November). Speech emotion recognition using CNN. In Proceedings of the 22nd ACM international conference on Multimedia (pp. 801-804).

Yenigalla, P., Kumar, A., Tripathi, S., Singh, C., Kar, S., & Vepa, J. (2018, September). Speech Emotion Recognition Using Spectrogram & Phoneme Embedding. In Interspeech (pp. 3688-3692).

