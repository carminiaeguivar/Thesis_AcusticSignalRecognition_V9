# Reconocimiento de señales acusticas diferentes a la voz humana usando principios de ASR


The approach of this project shows how ASR models can be applied to the recognition of acoustic signals other than the human voice, specifically the proposed model uses audio recordings of
Bolivian birds combined with feature extraction techniques and Deep Learning algorithms. The project was developed in Python language, the input data, which in this case are audio recordings,
are read by the data ingestion module and then passed to the data processing module, where the most relevant features are extracted. of the audio files and specifically the initial audio recognition problem is converted into an image recognition problem. This is achieved by extracting the spectrograms from the audio recordings. This new set of images is passed to the cloud storage module, to then be read by the training module that uses convolutional networks as the classification algorithm. In this phase, there are 4 candidate models with different CNN architectures studied, of which the CNN2-BACTH model is the one that generates the best results with an accuracy of 86 % in the validation stage and 94 % in the training stage. And finally the predictions are made, and the bird species that show the exits are classified.

Recognition of acoustic signals other than the human voice principles using ASR using:

- [BirdsBoliva Dataset](#birdsBolivia)
- [Spectrograms](#Spectrograms)
- [Convolutional Neural Networks](#CNN)


## BirdsBoliva Dataset

For this project, a new recording dataset was created using the files of the Macaulay library but specifically of birds sighted in Bolivian territory, the creation process goes from downloading the audio files, debugging, processing to assembling the dataset itself.  As a result of this entire process, a new dataset called birdsBolivia has been created, consisting of 3000 audio recordings in .wav format belonging to 10 species of birds sighted in Bolivian territory.

## Spectrograms

The spectrogram is a visual representation that allows to identify the different variations of the frequency and intensity of the sound throughout a period of time. For its study, spectral analysis is implemented, which mainly tries to use sounds or fragments made up of multiple components.
In this project, the spectrograms are obtained using the dourier transforms that carry the sound signal from its representation in the time domain to its representation in the frequency domain.
 

## Convolutional Neural Networks

Convolutional neural networks are a type of deep learning algorithm that is primarily used to analyze and learn visual attributes from large amounts of data. They are mainly used for AI applications related to image processing in which they are specialists, this is the reason why audio files are transformed into images (spectrograms).

# IMPORTANT NOTES 

  The models with the best results were:
- CNN1-DropOut ( into the file models_v1  with 61%  of accuracy at the valitation stage)
- CNN2-Batch   ( thelast version for this model in in the file models_v2,  with 86% of accuracy at validation stage and 94% of accuracy at trainning stage  )
- CNN3-LeakyRelu ( into the file models_v1 with 70%  of accuracy at the valitation stage)
- CNN4-DenseNet  ( into the file models_v1 with 54%  of accuracy at the valitation stage)



<!--
## Licencia

La última sección de un archivo README de alta calidad es la licencia. Esto permite que otros desarrolladores sepan lo que pueden y no pueden hacer con su proyecto. Si necesita ayuda para elegir una licencia, consulte [https://choosealicense.com/](https://choosealicense.com/).

---

🏆 Las secciones anteriores son lo mínimo indispensable y su proyecto determinará finalmente el contenido de este documento. También puede considerar agregar las siguientes secciones.

## Insignias

![badmath](https://img.shields.io/github/languages/top/nielsenjared/badmath)

Las insignias en sí mismas no son necesarias, pero demuestran un crédito callejero. Las insignias permiten a otros desarrolladores saber que usted sabe lo que está haciendo. Eche un vistazo a las insignias presentadas por [shields.io](https://shields.io/). Es posible que no comprenda lo que todas ellas representan ahora, pero lo comprenderá con el tiempo.

## Funciones

Si su proyecto tiene muchas funciones, enumérelas aquí.

## Cómo contribuir

Si creó una aplicación o paquete, y desea que otros desarrolladores contribuyan con ella, puede incluir directrices sobre cómo hacerlo. El [Pacto de colaboradores](https://www.contributor-covenant.org/) es un estándar de la industria, pero siempre puede redactar el suyo si lo prefiere.

## Pruebas

Vaya un paso más allá y escriba pruebas para su aplicación. Luego, proporcione ejemplos sobre cómo ejecutarlas aquí.
 -->
