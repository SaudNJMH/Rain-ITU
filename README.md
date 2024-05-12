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
|01     |ESP32 WROOM  |
|02     |Edge Impulse |


## Introduction

The project is pioneering and is designed to detect and classify rainfall intensity through the analysis of sound data. This involved capturing a 2-hour audio recording of rainfall, which is then segmented into one-second intervals. Each segment is analyzed to determine its root mean square (RMS) and decibel (dB) levels. Following this, the data is uploaded to the Edge Impulse platform, where it undergoes further processing, including detailed classification and machine learning training. This methodical approach aims to refine the accuracy of rainfall intensity measurement using audio analysis techniques.

## Steps Involved

1. Audio Recording: A 19-minute audio clip of rainfall is recorded.
2. Segmentation: The audio clip is divided into individual second-long segments.
3. Data Analysis: RMS and dB values are extracted from each segment.
4. Data Uploading: The segmented audio data is uploaded to Edge Impulse for further processing.
5. Classification: Edge Impulse is used to classify the sound data into different rainfall intensities.
6. Training: The data is trained to improve the accuracy of rainfall intensity classification.
7. Arduino Library: A library is created for Arduino to interface with the rainfall detection system.
8. Hardware Setup: The system is deployed on an ESP32 WROOM microcontroller, connected to a microphone for real-timesound recording.
9. Rainfall Detection: The system can now detect and quantify rainfall intensity based on recorded sound data.



## Challenges Faced

Throughout the development, the team found several challenges. Making sure the quality of audio recordings was hard because of the environmental noise and the different rainfall patterns. The extraction of meaningful features from the audio, such as RMS and dB values, required signal processing techniques. Additionally, training models for accurate rainfall intensity classification demanded a large dataset, which was challenging to gather. Integrating the system with ESP32 WROOM microcontrollers also needed technical expertise to ensure ideal hardware performance. Deploying the system in real-world conditions brought even more challenges, including managing power consumption, ensuring reliable connectivity, and coping with environmental conditions. Despite these obstacles, the Rain_ITU project has demonstrated the practicality of using sound data for rainfall detection and highlighted the potential for further technological advancements in this area.

## Future Directions

As the project progresses, several key areas are targeted for enhancement. The team plans to add to the existing dataset with more recordings from multiple geographical locations and rainfall intensities to improve the robustness of the model. There is also a focus on exploring advanced signal processing techniques and machine learning algorithms to boost the accuracy and efficiency of rainfall intensity classification. Efforts are being made to design the system for scalability and ease of deployment in diverse settings, including both rural and urban environments. Furthermore, engaging with the community is a priority to gather valuable feedback, foster collaboration, and promote the widespread adoption of this innovative rainfall detection technology. Through ongoing research and development, Rain_ITU is committed to contributing to more precise and accessible methods for rainfall monitoring and prediction.

## Acknowledgments

We give our thanks to the contributors who were involved in the project. Their dedication and support have been good in advancing the field of rainfall detection and monitoring. We deeply appreciate their continued commitment to this innovative endeavor.

## Conclusion

In conclusion, the Rain_ITU project has achieved significant progress in developing a reliable rainfall detection system using sound data. Through meticulous recording, segmenting, and analyzing rainfall audio, we have succeeded in accurately classifying rainfall intensity. The deployment of this system on ESP32 WROOM microcontrollers facilitates real-time monitoring of rainfall, which holds potential applications in weather forecasting, agriculture, and urban planning. This advancement underscores the project's contribution to enhancing our understanding and management of weather-related phenomena.
