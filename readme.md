
# ANOMALY DETECTION

Most machine learning (ML) proposals in the Internet of Things (IoT) space are designed and evaluated on pre-processed datasets, where the data acquisition and cleaning steps are often considered a black box. Therefore, the data acquisition stage requires additional data cleaning/anomaly techniques, which translate to additional resources, energy, and storage. We propose to carry out such techniques not in the cloud servers and closer to the data source, on the IoT device itself. Consequently, this application defines three anomaly detection steps using smoothing filters, unsupervised learning, and deep learning techniques (hybrid model) to detect the different variations of anomalies, focusing on a small computational/memory footprint.

## DATASET: 

To explain tamper situations, a test box was built to collect data from three different scenarios. The test box is made with a computer fan to cool the box, an incandescent bulb to warm up the box, and a small door that people can smoke or blow over the sensor. Therefore, label 1 is considered when the box is warming/cooling in normal conditions, label 2 when the sensor is tampered with by people blowing on it, label 3 is defined when people smoke near the sensor, and label 4 when the sensor detects fire. The IoT device has a well-known CO2, temperature, and humidity sensor SCD-30, the LoPy4 as a microcontroller and a relay board to manage the fan and the bulb. 
