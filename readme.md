
# ANOMALY DETECTION

Most machine learning (ML) proposals in the Internet of Things (IoT) space are designed and evaluated on pre-processed datasets, where the data acquisition and cleaning steps are often considered a black box. Therefore, the data acquisition stage requires additional data cleaning/anomaly techniques, which translate to additional resources, energy, and storage. We propose to carry out such techniques not in the cloud servers and closer to the data source, on the IoT device itself. Consequently, this application defines three anomaly detection steps using smoothing filters, unsupervised learning, and deep learning techniques (hybrid model) to detect the different variations of anomalies, focusing on a small computational/memory footprint.

## DATASET: 

To explain tamper situations, a test box was built to collect data from three different scenarios. The test box is made with a computer fan to cool the box, an incandescent bulb to warm up the box, and a small door that people can smoke or blow over the sensor. Therefore, label 1 is considered when the box is warming/cooling in normal conditions, label 2 when the sensor is tampered with by people blowing on it, label 3 is defined when people smoke near the sensor, and label 4 when the sensor detects fire. The IoT device has a well-known CO2, temperature, and humidity sensor [SCD-30](https://sensirion.com/products/catalog/SCD30/), the [LoPy4](https://pycom.io/product/lopy4/) as a microcontroller and a relay board to manage the fan and the bulb. 

## BACKGROUND:

- **Noise:** The sensor's signal is discretized/digitalized to be understandable to the microcontroller. However, errors like voltage fluctuations, non-linearity response, and vibrations insert noise into the electric signal, confusing the ML algorithm in the feature extraction stage. For this reason, signal smoothing is a filter that reduces these noise components when the phenomenon does not have high sampling frequencies getting a cleaner signal.

- **Outlier detection:** These methods are in charge of detecting data with a different distribution than the rest. This process is carried out through an unsupervised analysis.

- **Tamper detection:** In some scenarios, the information acquired by the IoT device can be compromised by malicious users trying to steal or modify data. tamper detection techniques require knowing all the manipulation possibilities to detect them, which needs supervised learning.

## RESOURCES:

- [Python Code](https://github.com/puldavid87/anomaly_detection/blob/main/anomaly_detection.ipynb)
- [Dataset](https://github.com/puldavid87/anomaly_detection/blob/main/anomaly_detection.csv)
- [Webpage project](https://iot4.paulrosero-montalvo.com/anomaly/)
- [Article](https://iot4.paulrosero-montalvo.com/gallery/Hybrid_Anomaly_Detection_Model_on_IoT_Devices%20(1).pdf)
