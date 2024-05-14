# Rain ITU Project

_by:_


_Abdullelah Al-Hussain    221423053_


_Hussain AlMazyadi        221428946_


_Saud Al-Hathlool         221407718_



## Objective

Rain_ITU is a project dedicated to developing an innovative rainfall detection system that makes use of sound data to accurately classify different levels of rainfall intensity. By recording, segmenting, and analyzing audio data, the project strives to establish a working and reliable method for quantifying rainfall intensity. This project aims to provide accurate, real-time measurements that can be useful for weather forecasting and climate research, improving our understanding and response to meteorological conditions.


## Material
 
|number | name        |
|------ |-------------|
|01     |Edge Impulse |
|02     |Arduino Nano BLE33 |
|03     |TML Shield   |
|04     |Microphone OV7675 |





## Introduction

The project is pioneering and is designed to detect and classify rainfall intensity through the analysis of sound data. This involved capturing a 2-hour audio recording of rainfall, which is then segmented into one-second intervals. Each segment is analyzed to determine its root mean square (RMS) and decibel (dB) levels. Following this, the data is uploaded to the Edge Impulse platform, where it undergoes further processing, including detailed classification and machine learning training. This methodical approach aims to refine the accuracy of rainfall intensity measurement using audio analysis techniques.

## Steps Involved

1. Audio Recording: A clip of rainfall is recorded.
2. Segmentation: The audio clip is divided into individual second-long segments.
3. Data Analysis: RMS and dB values are extracted from each segment.
4. Data Uploading: The segmented audio data is uploaded to Edge Impulse for further processing.
5. Classification: Edge Impulse is used to classify the sound data into different rainfall intensities.
6. Training: The data is trained to improve the accuracy of rainfall intensity classification.
7. Arduino Library: A library is created for Arduino to interface with the rainfall detection system.
8. Hardware Setup: The system is deployed on an ESP32 WROOM microcontroller, connected to a microphone for real-time recording.
9. Rainfall Detection: The system can now detect and quantify rainfall intensity based on recorded sound data.


<img width="348" alt="Screenshot 2024-05-13 at 8 50 16 PM" src="https://github.com/SaudNJMH/Rain-ITU/assets/167855783/265a0945-9391-418f-9661-13710f5aabaa">


In the development of the project, using recorded audio, several steps are involved. Initially, audio of rainfall is captured and segmented into one-second intervals. Each segment is then analyzed for its root mean square (RMS) and decibel (dB) levels, which quantify the audio's power and perceived loudness. This segmented data is uploaded to the Edge Impulse platform, which is leveraged for further processing and analysis.

In the classification phase, Mel Frequency Cepstral Coefficients (MFCC) inputs are used because of their effectiveness in handling audio data. This method transforms the audio signals into a representation that captures the power spectrum of sound, making it suitable for audio classification tasks. The system classifies each data sample into one of ten classes based on rainfall intensity, ranging from R1 (the lowest intensity) to R10 (the highest intensity). This classification helps in accurately assessing the intensity of rainfall from the recorded audio data.

To enhance the accuracy of the system, the classified data goes to a training phase. This training optimizes the system's ability to distinguish between different intensities of rainfall, making the detection more reliable. An Arduino library is created to interface seamlessly with the rainfall detection system, allowing for integration into larger projects or systems.

The hardware setup for this project involves deploying Arduino Nano, which is connected to a microphone for real-time audio recording. both of these are connected to a tiny machine learning (TML) board. This setup enables the system to continuously monitor and detect rainfall intensity based on the recorded audio, providing live updates and data.

Overall, this system represents a significant advancement in environmental monitoring technologies, allowing for the automated and accurate detection of rainfall intensity, which can be crucial for weather forecasting, agricultural planning, and management of water resources.

## Block Diagram

The block diagram illustrates the workflow of a system designed to classify rain audio using an Arduino Nano and Edge Impulse. The process starts with rain audio being captured by a microphone. This audio signal is then sent to a TML Shield connected to the Arduino Nano, which handles the preliminary processing. Simultaneously, code is uploaded to the Arduino Nano to control the data flow and processing steps. The TML Shield, interfacing with Edge Impulse, processes the audio signal further to extract relevant features. These features are then fed into a processing unit that applies machine learning models to classify the audio data. The final output consists of classifications and their corresponding accuracy metrics. The system ensures real-time processing and accurate classification of rain audio, making it useful for various applications in environmental monitoring and smart city infrastructure.


<img width="936" alt="Screenshot 2024-05-14 at 11 23 02 AM" src="https://github.com/SaudNJMH/Rain-ITU/assets/167855783/03313148-8d4e-4c0b-b6f9-b6e32809f5f3">




## Observations and Results

We tested a few samples in different regions in Saudi Arabia throughout 2024, notable variations in rainfall intensity were recorded. Specifically, the Abha region experienced significantly higher rainfall, classified in the highest intensity class, R10, with a recorded precipitation of 11 mm. This contrasts with the drier Al-Ahsa area, where rainfall was classified at a much lower intensity, R4, with precipitation measuring only 3 mm.

These findings illustrate the difference in rainfall patterns within Saudi Arabia, highlighting the potential of the developed system to provide detailed and localized weather monitoring. The ability to classify rainfall intensity through audio data offers a practical tool for resource management, agricultural planning, and emergency preparedness in regions prone to varying weather conditions. Such detailed data acquisition is important for enhancing the accuracy of weather forecasting models and for implementing region-specific strategies to mitigate the impacts of weather variability.


The data explorer visualization demonstrates a clear distinction in the classification of correct and incorrect labels across multiple samples, underlining the effectiveness of our feature extraction process. This affects the accuracy of the data, checking whether the location is correct or not.


![Data Explorer Results](https://github.com/SaudNJMH/Rain-ITU/assets/167855783/888f06a0-0b9a-47f6-8b92-304f79411fa7)


The confusion matrix from our model testing shows a high overall accuracy of 95.33%, with certain classifications ranging from R1 to R10, which affirms the model's capability in handling real-world variability.

<img width="545" alt="Screenshot 2024-05-13 at 10 39 03 AM" src="https://github.com/SaudNJMH/Rain-ITU/assets/167855783/0d4fdbbb-7169-43ed-a805-5409e285ef8a">

**Spectrogram Analysis**: 
This spectrogram shows Mel Energies, the focus is on how sound energy distributes across various frequencies, reflecting different characteristics of the rainfall. The Mel scale enhances the analysis by aligning more closely with human auditory perceptions, which is beneficial for applications that involve human interaction or that mimic human sensory processing, such as advanced sound engineering or environmental sound recognition systems. 

This analysis will help in the development of algorithms that predict weather conditions from acoustic data, potentially offering a novel approach to weather monitoring that could complement traditional methods like radar and satellite imagery. This could be particularly useful in remote areas or in developing countries where traditional, expensive weather monitoring infrastructure is not feasible.


![mel)](https://github.com/SaudNJMH/Rain-ITU/assets/167855783/75f2b140-fcd2-409f-872b-d86f5a814bf9)



These findings and visual representations validates the project's approach but also underscore its potential to enhance rainfall monitoring through sound data analysis. The successful classification and real-time application of our model highlight its potential benefits for weather forecasting and environmental monitoring, particularly in regions prone to varying rainfall intensities like Saudi Arabia.


## Challenges Faced

Throughout the development, the team found several challenges. Making sure the quality of audio recordings was hard because of the environmental noise and the different rainfall patterns. The extraction of meaningful features from the audio, such as RMS and dB values, required signal processing techniques. Additionally, training models for accurate rainfall intensity classification demanded a large dataset, which was challenging to gather. Integrating the system with ESP32 WROOM microcontrollers also needed technical expertise to ensure ideal hardware performance. Deploying the system in real-world conditions brought even more challenges, including managing power consumption, ensuring reliable connectivity, and coping with environmental conditions. Despite these obstacles, the Rain_ITU project has demonstrated the practicality of using sound data for rainfall detection and highlighted the potential for further technological advancements in this area.

## Future Directions

As the project progresses, several key areas are targeted for enhancement. The team plans to add to the existing dataset with more recordings from multiple geographical locations and rainfall intensities to improve the robustness of the model. There is also a focus on exploring advanced signal processing techniques and machine learning algorithms to boost the accuracy and efficiency of rainfall intensity classification. Efforts are being made to design the system for scalability and ease of deployment in diverse settings, including both rural and urban environments. Furthermore, engaging with the community is a priority to gather valuable feedback, foster collaboration, and promote the widespread adoption of this innovative rainfall detection technology. Through ongoing research and development, Rain_ITU is committed to contributing to more precise and accessible methods for rainfall monitoring and prediction.

## Acknowledgments

We give our thanks to the contributors who were involved in the project. Their dedication and support have been good in advancing the field of rainfall detection and monitoring. We deeply appreciate their continued commitment to this innovative endeavor.

## Conclusion

In conclusion, the Rain_ITU project has achieved significant progress in developing a reliable rainfall detection system using sound data. Through meticulous recording, segmenting, and analyzing rainfall audio, we have succeeded in accurately classifying rainfall intensity. The deployment of this system on ESP32 WROOM microcontrollers facilitates real-time monitoring of rainfall, which holds potential applications in weather forecasting, agriculture, and urban planning. This advancement underscores the project's contribution to enhancing our understanding and management of weather-related phenomena.
