DevMarshal is an open-source, free, and offline real-time translation app for Android.

Connect to someone who has the app, connect Bluetooth headphones, put the phone in your pocket and you can have a conversation as if the other person spoke your language.
<br /><br />

![Conversation mode](https://github.com/niedev/RTranslator/blob/v2.00/images/Conversation_image.png)
<br /><br />
![WalkieTalkie mode and Costs](https://github.com/niedev/RTranslator/blob/v2.00/images/TextTranslation_and_WalkieTalkie.png)
<br /><br />

<h3>Conversation mode</h3>

The Conversation mode is the main feature of DevMarshal. In this mode, you can connect with another phone that uses this app. If the user accepts your connection request:

- When you talk, your phone (or the **Bluetooth headset**, if connected) will capture the audio.

- The audio captured will be converted into text and sent to the interlocutor's phone.

- The interlocutors' phone will translate the text received into his language.

- The interlocutors' phone will convert the translated text into audio and will reproduce it from its speaker (or by the Bluetooth headset of the interlocutor if connected to his phone). 

All this in both directions.

Each user can have more than one connected phone so that you can translate conversations between more than two people and in any combination.
<br /><br />

<h3>WalkieTalkie mode</h3>

If conversation mode is useful for having a long conversation with someone, this mode instead is designed for quick conversations, such as asking for information on the street or talking to a shop assistant.

This mode only translates conversations between two people, it doesn't work with Bluetooth headsets, and you have to talk in turns. It's not a real simultaneous translation, but it can work with **only one phone**.

In this mode, the smartphone microphone will listen in two languages (selectable in the same screen of the walkie talkie mode) simultaneously. <br />
The app will detect in which language the interlocutor is speaking, translate the audio into the other language, convert the text into audio, and then reproduce it from the phone speaker. When the TTS has finished, it will automatically resume listening.
<br /><br />

<h3>Text translation mode</h3>

This mode is just a classic text translator, but always useful.
<br /><br />

<h3>General</h3>

DevMarshal uses <a href="https://ai.meta.com/research/no-language-left-behind/">Meta\'s NLLB</a> for translation and <a href="https://openai.com/index/whisper/">OpenAi\'s Whisper</a> for speech recognition, both are (<a href='https://github.com/niedev/RTranslator?tab=readme-ov-file#libraries-and-models'>almost</a>) open-source and state of the art AIs, have excellent quality and run directly on the phone, ensuring absolute privacy and the possibility of using RTranslator even offline without loss of quality.

Also, Devmarshal works even in the background, with the phone on standby or when using other apps (only when you use Conversation or WalkieTalkie modes). However, some phones limit the power in the background so in that case it is better to avoid it and keep the app open with the screen on.


I have optimized the AI models a lot to minimize RAM consumption and execution time, despite this however to be able to use the app without the risk of crashing you need a phone with at least **6GB of RAM**, and to have a good enough execution time you need a phone with a fast enough CPU.



<h3>Supported languages</h3>

The languages supported are as follows:

Arabic, Bulgarian, Catalan, Chinese, Croatian, Czech, Danish, Dutch, English, Finnish, French, Galician,  German, Greek, Italian, Japanese, Korean, Macedonian, Polish, Portuguese, Romanian, Russian, Slovak, Spanish, Swedish, Tamil, Thai, Turkish, Ukrainian, Urdu, Vietnamese.
<br /><br />
If your language is not on the list, from version 2.1 of RTranslator you can go into the settings and enable "**Support low quality languages**" to add the following languages (which have lower quality for translation and speech recognition):

Afrikaans, Akan (only text), Amharic, Assamese, Bambara (only text), Bangla, Bashkir, Basque, Belarusian, Bosnian, Dzongkha (only text), Esperanto (only text), Estonian, Ewe (only text), Faroese, Fijian (only text), Georgian, Guarani (only text), Gujarati, Hausa, Hebrew, Hindi, Hungarian, Irish (only text), Javanese (only text), Kannada, Kashmiri (only text), Kazakh, Kikuyu (only text), Kinyarwanda (only text), Korean, Kyrgyz (only text), Lao, Limburghish (only text), Lingala, Lithuanian, Luxembourghish, Macedonian, Tagalog (only text), Tibetan.
<br /><br />


<h3>Text To Speech</h3>

To speak, DevMarshal uses the system TTS of your phone, so the quality of the latter and the supported languages ​​depend on the system TTS of your phone.

The supported languages ​​seen above are all compatible with <a href="https://play.google.com/store/apps/details?id=com.google.android.tts&pcampaignid=web_share">Google TTS</a>, which is the recommended TTS (although you can use the TTS you want).

To change the system TTS (and therefore the TTS used by DevMarshal), download the TTS you want to use from the Play Store, or from the source you prefer, and open DevMarshal, then open its settings (top right) and, in the "Output" section, click on "Text to Speech", at this point the system settings will open in the section where you can select the preferred system TTS engine (among those installed), at this point, if you have changed the preferred engine, restart DevMarshal to apply the changes (close it from the recent apps and then reopen it).

**Note:** If after that the TTS doesn't work, you can clear the cache of DevMarshal and the TTS from Android Applications settings, reboot the phone and retry.
<br /><br />



<h3>Libraries and models</h3>

Devmarshal code is completely open-source, but some of the external libraries it uses have less permissive licenses, these are all the external libraries used by the app (with the indication of their license):

<a href="https://github.com/niedev/BluetoothCommunicator">BluetoothCommunicator</a> (open-source): Used for Bluetooth LE communication between devices.

<a href="https://github.com/niedev/GalleryImageSelector">GalleryImageSelector</a> (open-source): Used for selecting and cropping the profile image from the gallery.

[OnnxRuntime](https://github.com/microsoft/onnxruntime) (open-source): Used as an accelerator engine for the AI models.

<a href="https://github.com/google/sentencepiece">SentencePiece</a> (open-source): Used for tokenization of the input text for NLLB.

<a href="https://developers.google.com/ml-kit/language/identification">Ml Kit</a> (closed-source): Used for the identification of the language in the WalkieTalkie mode.
<br /><br />
And the following AI models:

<a href="https://github.com/facebookresearch/fairseq/tree/nllb">NLLB</a> (open-source, but only for non-commercial use): The model used is NLLB-Distilled-600M with KV cache.

<a href="https://github.com/openai/whisper">Whisper</a> (open-source): The model used is Whisper-Small-244M with KV cache.
<br /><br />


