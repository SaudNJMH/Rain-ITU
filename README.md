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

1. Audio Recording: A 2-hour audio clip of rainfall is recorded.
2. Segmentation: The audio clip is divided into individual second-long segments.
3. Data Analysis: RMS and dB values are extracted from each segment.
4. Data Uploading: The segmented audio data is uploaded to Edge Impulse for further processing.
5. Classification: Edge Impulse is used to classify the sound data into different rainfall intensities.
6. Training: The data is trained to improve the accuracy of rainfall intensity classification.
7. Arduino Library: A library is created for Arduino to interface with the rainfall detection system.
8. Hardware Setup: The system is deployed on an ESP32 WROOM microcontroller, connected to a microphone for real-timesound recording.
9. Rainfall Detection: The system can now detect and quantify rainfall intensity based on recorded sound data.

## Observations and Results

The Rain_ITU project has diligently recorded, analyzed, and classified rainfall intensity using sophisticated sound data processing. Key aspects of the project involved extensive data collection and thorough analysis to ensure accurate rainfall detection and classification.

**Data Collection**: Our data acquisition process captured audio samples across various weather conditions and locations to ensure a comprehensive dataset. Notably, specific attention was given to data collected on April 2024 and May 2024, during which we recorded significant rainfall events in the eastern region of Saudi Arabia. On April, the recorded precipitation reached 11 mm, while on May, it reduced to 3 mm, however, during the making of this project, May has yet to end, but we do not anticipate any upcoming rainall through the rest of may. this data provided us with a different range of intensities to enhance our model's robustness and accuracy. 

According to [Weather Atlas](https://www.weather-atlas.com/en/saudi-arabia-weather-may) On May 2024, the precipitation in Dammam was recorded as 3 mm, which is typical for this period as May marks the onset of the hotter months and generally experiences very low rainfall. This specific measurement aligns with the expected climatic patterns for Dammam during May, where the region sees very limited rainfall days, totaling about 0.8 days of rain throughout the month. [name of link](https://www.weather-atlas.com/en/saudi-arabia/dammam-weather-april) also stated that pn April 2024, Dammam experienced significant rainfall as part of a wider weather pattern affecting the Persian Gulf region, which led to widespread flooding across various areas including Dammam. This event was characterized by heavy rainfall and thunderstorms, causing disruptions such as road tunnel closures and school cancellations in the area. 

In general, the month of April in Dammam is marked by rising temperatures and a modest amount of rainfall, with an average precipitation accumulation of about 11mm over approximately 6.7 days throughout the month. This indicates that the rainfall on April 16th was particularly severe and atypical for the region's usual climate patterns in April. 



**Analysis and Model Testing**: 
- The data explorer visualization demonstrates a clear distinction in the classification of correct and incorrect labels across multiple samples, underlining the effectiveness of our feature extraction process.


![Data Explorer Results](https://github.com/SaudNJMH/Rain-ITU/assets/167855783/888f06a0-0b9a-47f6-8b92-304f79411fa7)


- The confusion matrix from our model testing shows a high overall accuracy of 95.33%, with certain classifications such as light, moderate, and heavy rain showing higher precision, which affirms the model's capability in handling real-world variability.

<img width="545" alt="Screenshot 2024-05-13 at 10 39 03 AM" src="https://github.com/SaudNJMH/Rain-ITU/assets/167855783/0d4fdbbb-7169-43ed-a805-5409e285ef8a">

**Spectrogram Analysis**: 
- The Mel Energies plot is crucial for observing how energy is distributed across different frequencies over time, aiding significantly in our feature extraction strategies. This spectrogram analysis is vital for understanding the characteristics of rainfall sounds.
![mel)](https://github.com/SaudNJMH/Rain-ITU/assets/167855783/75f2b140-fcd2-409f-872b-d86f5a814bf9)


**On-Device Performance and Live Classification**: 
- The on-device performance metrics indicate an inference time of 23 ms on the ESP32 WROOM microcontroller, showcasing the model's effectiveness for real-time applications. This rapid processing capability is critical for deploying the system in real-time scenarios where immediate rainfall detection is required.
![WhatsApp Image 2024-05-12 at 5 33 03 PM (1)](https://github.com/SaudNJMH/Rain-ITU/assets/167855783/9e6efaaf-0832-4a28-bb00-7f07464e06e8)
- Live classification tests further validate our model’s real-world applicability, capturing and classifying audio data in real-time with high accuracy, proving the system's readiness for operational use.
![WhatsApp Image 2024-05-12 at 5 33 02 PM](https://github.com/SaudNJMH/Rain-ITU/assets/167855783/3c7f3f09-96cd-40af-8a99-6e3fe9d9d767)


These findings and visual representations not only validate the Rain_ITU project's methodological approach but also underscore its potential to revolutionize rainfall monitoring through sound data analysis. The successful classification and real-time application of our model highlight its potential benefits for weather forecasting and environmental monitoring, particularly in regions prone to varying rainfall intensities like Saudi Arabia.


## Challenges Faced

Throughout the development, the team found several challenges. Making sure the quality of audio recordings was hard because of the environmental noise and the different rainfall patterns. The extraction of meaningful features from the audio, such as RMS and dB values, required signal processing techniques. Additionally, training models for accurate rainfall intensity classification demanded a large dataset, which was challenging to gather. Integrating the system with ESP32 WROOM microcontrollers also needed technical expertise to ensure ideal hardware performance. Deploying the system in real-world conditions brought even more challenges, including managing power consumption, ensuring reliable connectivity, and coping with environmental conditions. Despite these obstacles, the Rain_ITU project has demonstrated the practicality of using sound data for rainfall detection and highlighted the potential for further technological advancements in this area.

## Future Directions

As the project progresses, several key areas are targeted for enhancement. The team plans to add to the existing dataset with more recordings from multiple geographical locations and rainfall intensities to improve the robustness of the model. There is also a focus on exploring advanced signal processing techniques and machine learning algorithms to boost the accuracy and efficiency of rainfall intensity classification. Efforts are being made to design the system for scalability and ease of deployment in diverse settings, including both rural and urban environments. Furthermore, engaging with the community is a priority to gather valuable feedback, foster collaboration, and promote the widespread adoption of this innovative rainfall detection technology. Through ongoing research and development, Rain_ITU is committed to contributing to more precise and accessible methods for rainfall monitoring and prediction.

## Acknowledgments

We give our thanks to the contributors who were involved in the project. Their dedication and support have been good in advancing the field of rainfall detection and monitoring. We deeply appreciate their continued commitment to this innovative endeavor.

## Conclusion

In conclusion, the Rain_ITU project has achieved significant progress in developing a reliable rainfall detection system using sound data. Through meticulous recording, segmenting, and analyzing rainfall audio, we have succeeded in accurately classifying rainfall intensity. The deployment of this system on ESP32 WROOM microcontrollers facilitates real-time monitoring of rainfall, which holds potential applications in weather forecasting, agriculture, and urban planning. This advancement underscores the project's contribution to enhancing our understanding and management of weather-related phenomena.
