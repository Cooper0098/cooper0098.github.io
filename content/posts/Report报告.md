+++
title = 'Report报告'
date = 2025-01-01T17:12:47+08:00



categories = ["报告"] 
tags = ["报告" ]

+++



### Gesture Recognition System Design Based on STM32F429 and MPU6050

---

## **Part 1: Hardware Design**

### **1.1 Hardware Platform Setup**
The hardware platform for this project is designed to collect, process, and classify gesture data using the STM32F429 development board paired with an MPU6050 gyroscope. This combination provides a robust environment for data acquisition and real-time interaction.

#### **Key Components**
1. **STM32F429 Development Board**: Serves as the primary computational unit for reading sensor data, processing, and running the machine learning model.
2. **MPU6050 Gyroscope**: Collects motion data, including acceleration and angular velocity, enabling gesture detection and recognition.
3. **Button**: Facilitates user interaction for tasks such as initiating data collection or resetting the system.
4. **LED Indicators**: Provides visual feedback for system status, including readiness, data collection, and gesture recognition results.
5. **Serial-to-TTL Module (e.g., CH340)**: Ensures seamless communication between the microcontroller and a PC, enabling data transfer and debugging.

#### **1.2 System Integration**
The components are connected as follows:
- The MPU6050 communicates with the STM32F429 via the I²C protocol, providing reliable data transmission.
- A button is attached to one of the GPIO pins configured for interrupt handling to trigger specific actions.
- LEDs are connected to other GPIO pins, configured for output mode to signal various statuses.
- The Serial-to-TTL module is linked to the UART pins on the STM32, enabling bidirectional communication with the PC.

---

## **Part 2: Algorithm Design**

### **2.1 Gesture Recognition Algorithm**
The gesture recognition algorithm is based on a convolutional neural network (CNN) architecture, optimized for embedded environments using the **nnom** library. 

#### **Key Adjustments**
1. **Sampling Frequency**: The data collection frequency was set to 100 Hz to ensure smooth and accurate gesture tracking.
2. **Network Architecture**:
   - Reduced the number of convolutional layers from 4 to 2, balancing model complexity and computational efficiency.
   - Modified the stride of convolution and pooling layers to 3, improving the model's ability to extract meaningful features.
3. **Training Data**: Collected new datasets with 20 samples per gesture to improve the model's generalization and recognition accuracy.

#### **2.2 Training Process**
1. **Data Collection**:
   - Configure the microcontroller in data collection mode by uncommenting `SYSTEM_MODE_DATA_COLLECT` in the `config.h` file.
   - Use a Python script to save raw sensor data from the MPU6050 to the PC.
2. **Model Training**:
   - The collected data is labeled and preprocessed (e.g., normalization).
   - The model is trained using TensorFlow, generating an `.h5` file for testing and a `.h` file for deployment.
3. **Model Deployment**:
   - Quantize the trained model for the STM32 platform using **nnom**.
   - Integrate the quantized model into the microcontroller's firmware.

#### **2.3 Gesture Recognition**
The trained model recognizes at least five gestures with high accuracy. The system classifies actions in real time and provides outputs such as LED signals or serial communication messages based on the recognized gesture.

---

## **Part 3: Interface Design**

### **3.1 User Interface Features**
The system features a user-friendly UI that facilitates interaction between the hardware and the user. The interface is divided into the following components:
1. **System Login**: Ensures secure access to the gesture recognition system.
2. **Hardware Control**: Allows users to initiate or stop hardware operations, such as data collection or model deployment.
3. **Data Management**: Provides options for transferring raw data from the microcontroller to the PC.
4. **Automatic Gesture Recognition**: Displays the recognized gesture in real time with visual indicators (e.g., LEDs or graphical elements on the PC).
5. **Real-Time Interaction**: Enables users to observe and interact with the system's behavior dynamically.

### **3.2 UI Implementation**
The UI is designed using a cross-platform framework (e.g., PyQt5). It includes the following key elements:
- **Buttons and Dropdowns**: Facilitate task selection, such as data collection or model testing.
- **Status Indicators**: Display system states, such as "Collecting Data" or "Gesture Recognized."
- **Graphical Display**: Visualizes raw sensor data and classification results for better understanding.

---

## **Part 4: Insights and Detailed Design Description**

### **4.1 Design Insights**
This project provided valuable insights into embedded systems, machine learning, and human-computer interaction:
1. **Hardware Optimization**: Ensuring seamless communication between the MPU6050 and STM32 required careful attention to protocol configuration and timing constraints.
2. **Algorithm Efficiency**: Reducing the CNN's depth and adjusting hyperparameters enhanced the model's performance while maintaining compatibility with the STM32's limited computational resources.
3. **Real-Time Processing**: Achieving real-time gesture recognition involved optimizing both data acquisition and inference processes.

### **4.2 Challenges and Solutions**
1. **Limited Computational Resources**:
   - **Challenge**: The STM32F429 has restricted processing power compared to traditional machine learning platforms.
   - **Solution**: Used the lightweight nnom library and quantized models to minimize resource consumption.
2. **Data Variability**:
   - **Challenge**: Variations in gesture execution among users affected recognition accuracy.
   - **Solution**: Increased the diversity of training data and applied data augmentation techniques.
3. **System Integration**:
   - **Challenge**: Synchronizing data collection, processing, and classification.
   - **Solution**: Designed modular code with clear separation between hardware interaction, data handling, and inference.

### **4.3 Experiences**
1. **Modular Development**: Breaking the project into hardware, algorithm, and interface modules simplified testing and debugging.
2. **Iterative Refinement**: Regular testing and refinement improved both the hardware setup and the model's accuracy.
3. **Practical Learning**: This hands-on experience deepened my understanding of embedded systems and the practical application of machine learning.

---

### **Conclusion**
The STM32-based gesture recognition system demonstrates a seamless integration of hardware, software, and machine learning. It offers a robust solution for recognizing gestures with real-time interaction, paving the way for further advancements in human-computer interfaces. Through this project, I gained practical knowledge in embedded development, algorithm optimization, and user interface design, laying a strong foundation for future innovations.



------



# 第二篇----------------------------------------



**Comprehensive Report on Gesture Recognition System Design Based on STM32F429**

------

### **Part 1: Hardware Platform Setup for Gesture Collection**

#### **Introduction to Hardware Components**

To design a robust gesture recognition system, a carefully selected combination of hardware components and configurations is essential. The system utilizes the STM32F429 development board and the MPU6050 gyroscope module, coupled with supplementary peripherals, to achieve precise gesture data collection. The design was inspired by the Cyberry Potter Electromagic Wand basic project, emphasizing simplicity and adaptability.

#### **Key Hardware Elements**

1. **STM32F429 Development Board**:
   - A high-performance microcontroller featuring an ARM Cortex-M4 processor.
   - Equipped with ample computational power and memory to handle embedded machine learning tasks.
2. **MPU6050 Gyroscope Module**:
   - Combines a 3-axis gyroscope and a 3-axis accelerometer.
   - Provides motion tracking data critical for gesture recognition.
3. **Peripheral Components**:
   - **Button**: Used to switch between system modes and control data collection.
   - **LED Indicators**: Visual feedback for system states, such as data collection or inference.
   - **Serial-to-TTL Module (CH340)**: Facilitates communication between the STM32 board and a PC for data transfer and debugging.

#### **System Features**

1. **Data Communication**:
   - The STM32 microcontroller communicates with the MPU6050 via I2C protocol.
   - Serial communication is employed to transfer data to the PC for analysis and training.
2. **System States**:
   - **Data Collection Mode**: Activated by uncommenting `SYSTEM_MODE_DATA_COLLECT` in the configuration file.
   - **Inference Mode**: Default operation mode for gesture recognition.
3. **Sampling Frequency**:
   - Adjusted to 100Hz to balance data accuracy and system performance.

#### **Hardware Setup Process**

1. Connect the MPU6050 to the STM32 board via I2C pins.
2. Attach the CH340 module to enable serial communication.
3. Configure the button and LED connections for system interaction.
4. Verify hardware connections and test the data output using debug scripts.

------

### **Part 2: Gesture Recognition Algorithm Design**

#### **Algorithm Overview**

The core of the gesture recognition system is a convolutional neural network (CNN) model deployed on the STM32 platform. The algorithm processes motion data from the MPU6050 to classify gestures accurately.

#### **Model Architecture**

1. **Input Layer**:
   - Accepts 6-dimensional motion data (3-axis gyroscope + 3-axis accelerometer) sampled at 100Hz.
2. **Convolutional Layers**:
   - Reduced from 4 to 2 layers to optimize for the STM32’s computational capacity.
   - Stride set to 3 for convolution and pooling layers to improve efficiency.
3. **Output Layer**:
   - Classifies gestures into 5 predefined categories.

#### **Training Process**

1. **Data Collection**:
   - Each gesture is sampled 20 times using the data collection mode.
   - Data is preprocessed and segmented into training and validation sets.
2. **Model Training**:
   - Conducted on a PC using the NNOM embedded ML library.
   - Hyperparameters tuned to achieve a balance between accuracy and execution time.
3. **Model Deployment**:
   - The trained model is converted into an `.h` file for integration into the STM32 firmware.
4. **Performance Evaluation**:
   - Achieved recognition accuracy improvements through iterative model tuning.
   - Serial testing script validates the deployed model’s performance in real-time.

#### **Insights**

1. Simplifying the model architecture while maintaining accuracy is crucial for resource-constrained platforms.
2. A robust dataset significantly enhances model reliability.

------

### **Part 3: Gesture Recognition UI Design**

#### **UI Features**

1. **System Login**:
   - Ensures secure access to the gesture recognition system.
2. **Hardware Control Panel**:
   - Provides options to toggle between data collection and inference modes.
3. **Data Visualization**:
   - Displays real-time motion data from the MPU6050.
4. **Automatic Recognition**:
   - Initiates gesture classification and shows results on the interface.

#### **UI Implementation**

1. Developed using a Python-based framework for cross-platform compatibility.
2. Integrated serial communication to interact with the STM32 board.
3. Designed an intuitive layout to facilitate user interaction and debugging.

#### **Benefits**

1. Real-time feedback enhances user experience.
2. Modular design supports future feature expansion.

------

### **Part 4: Detailed Design Description, Insights, and Experiences**

#### **Challenges and Solutions**

1. **Challenge**: Balancing model complexity with STM32’s resource limitations.
   - **Solution**: Simplified the CNN architecture and optimized hyperparameters.
2. **Challenge**: Ensuring accurate data collection.
   - **Solution**: Implemented rigorous calibration and preprocessing steps.
3. **Challenge**: Real-time system response.
   - **Solution**: Adjusted sampling frequency and optimized data processing pipelines.

#### **Lessons Learned**

1. Embedded ML projects require careful consideration of hardware constraints.
2. Iterative testing and debugging are essential for reliable performance.
3. Collaboration between hardware and software components enhances system robustness.

#### **Future Prospects**

1. Expand gesture categories to recognize more complex actions.
2. Integrate advanced ML models to improve classification accuracy.
3. Develop a mobile app interface for remote control and monitoring.

#### **Conclusion**

This project provided a comprehensive learning experience in embedded systems, machine learning, and human-computer interaction. By designing and implementing a gesture recognition system, I have gained valuable insights into integrating hardware, algorithms, and user interfaces to create an efficient and user-friendly solution.

------

**Appendices**

1. Configuration Files
2. Training Scripts
3. UI Source Code
4. Hardware Schematics
5. Performance Metrics and Logs



# 第三 ---------------------------



### Experimental Report on Gesture Recognition System Based on STM32F429 and MPU6050

#### Abstract

This report describes the design, implementation, and evaluation of a gesture recognition system based on the STM32F429 microcontroller and the MPU6050 gyroscope. The system aims to recognize at least five different gestures using machine learning algorithms, specifically convolutional neural networks (CNNs), and deploys the model on the STM32 platform for real-time inference. The system involves hardware setup, gesture data collection, model training, and deployment, as well as the creation of an intuitive user interface for real-time interaction.

The report is divided into four main sections: hardware setup, algorithm design, interface design, and insights from the development process. These sections will cover all relevant aspects of the project and provide detailed explanations for each of the steps taken during the project.

------

### 1. **Hardware Design**

The hardware platform for the gesture recognition system consists of a **STM32F429 development board** and an **MPU6050 gyroscope** sensor, along with supporting components such as buttons, LEDs, and serial communication modules. The hardware setup is designed to collect real-time data from the MPU6050 sensor, process this data, and transmit it for model inference.

#### 1.1 **STM32F429 Development Board**

The STM32F429 is a powerful microcontroller with a Cortex-M4 core that is suitable for handling complex tasks like gesture recognition. It supports multiple communication protocols, including **I2C**, which is used to communicate with the MPU6050 sensor, and **USART** for serial communication with a PC.

**Key features of the STM32F429 board:**

- 180 MHz ARM Cortex-M4 processor
- 2 MB Flash memory and 256 KB SRAM
- Multiple GPIO pins for interfacing with external sensors and peripherals
- Rich peripheral set including I2C, SPI, USART, and timers

This microcontroller provides enough computational power to process sensor data and run the gesture recognition model efficiently in real-time.

#### 1.2 **MPU6050 Gyroscope and Accelerometer**

The **MPU6050** is a popular motion tracking device that combines a 3-axis gyroscope and a 3-axis accelerometer. It communicates with the STM32 via the I2C protocol and provides real-time motion data. The sensor is capable of detecting changes in orientation and movement, making it ideal for gesture recognition applications.

**Key features of the MPU6050 sensor:**

- 3-axis accelerometer with a range of ±2g, ±4g, ±8g, and ±16g
- 3-axis gyroscope with a range of ±250°/s, ±500°/s, ±1000°/s, and ±2000°/s
- I2C interface for communication with the microcontroller
- Built-in Digital Motion Processor (DMP) for filtering and processing raw sensor data

In this system, the MPU6050 is used to collect acceleration and gyroscopic data for different gestures. The data is processed and passed on to the embedded machine learning model for classification.

#### 1.3 **Button Control and LED Indicators**

Buttons are used for user interaction, enabling users to switch between modes (e.g., data collection mode or inference mode) or trigger specific actions in the system. The **LED status indicators** provide feedback to the user about the current state of the system (e.g., data collection, model training, or gesture recognition).

- **Button control**: Used to start/stop data collection or switch between operational modes.
- **LED indicators**: Indicate the current mode (data collection, model testing, or inference).

#### 1.4 **Serial Communication (CH340 Module)**

The **CH340 USB-to-TTL module** is used for serial communication between the STM32F429 and a PC. This enables data transfer between the hardware and the PC for both training the model and testing the gesture recognition in real-time. It also allows for debugging and monitoring of the system’s status.

#### 1.5 **Hardware Connections and Wiring**

- **STM32F429 to MPU6050**: The I2C bus is used to connect the STM32 to the MPU6050 sensor. SCL (clock) and SDA (data) lines are used for communication, along with power and ground connections.
- **Buttons and LEDs**: These components are connected to specific GPIO pins on the STM32F429 to provide user control and status indication.

------

### 2. **Algorithm Design**

The core of the system is the **gesture recognition algorithm**, which involves processing data from the MPU6050 sensor and using machine learning techniques to classify the gestures. This section discusses the design of the gesture recognition model, including the data preprocessing steps, the model architecture, and the training process.

#### 2.1 **Data Collection and Preprocessing**

Before training the model, data for each gesture must be collected from the MPU6050 sensor. The sensor provides continuous data in the form of acceleration and gyroscope readings, which must be formatted into a suitable format for model training.

**Steps for data collection:**

1. **Activate Data Collection Mode**: By modifying the `config.h` file and setting `SYSTEM_MODE_DATA_COLLECT`, the STM32F429 enters data collection mode. In this mode, the system reads raw data from the MPU6050 sensor and prints it to the serial port.
2. **Gestures**: The system collects data for a minimum of five predefined gestures. Each gesture consists of a series of data points recorded over time.
3. **Data Labeling**: Each data sample is labeled according to the gesture it corresponds to. The data is then stored in a structured format, ready for model training.

The collected data is preprocessed to normalize the sensor readings and ensure consistency across different gestures. This step is crucial for improving model accuracy.

#### 2.2 **Convolutional Neural Network (CNN) Design**

The system uses a **Convolutional Neural Network (CNN)** for gesture recognition. The model takes raw sensor data as input and classifies it into one of the predefined gesture classes.

**Key components of the CNN model:**

- **Input Layer**: The raw sensor data is processed as a time-series input with each data point consisting of accelerometer and gyroscope readings.
- **Convolutional Layers**: Two convolutional layers are used to extract features from the time-series data. These layers apply filters to detect patterns such as changes in movement and orientation.
- **Pooling Layers**: Pooling layers reduce the dimensionality of the data while retaining important features. The stride is set to 3 to ensure efficient feature extraction.
- **Fully Connected Layers**: After the convolutional and pooling layers, the model uses fully connected layers to perform classification.
- **Output Layer**: The final layer produces the predicted gesture class.

The CNN model is trained using a supervised learning approach, with the labels for each gesture used to guide the model’s learning process. The training data consists of 20 samples per gesture, with the sampling frequency set to 100 Hz.

#### 2.3 **Model Training**

To train the model, the data collected from the MPU6050 is used as input, and the labels for each gesture serve as the target output. The model is trained using the **nnom** library, an embedded machine learning library optimized for STM32 microcontrollers.

**Training process:**

1. The collected data is split into training and testing sets.
2. The model is trained using the training set and evaluated on the testing set.
3. The model’s accuracy is measured, and hyperparameters (e.g., learning rate, number of epochs) are adjusted to optimize performance.
4. After training, the model is saved as an `.h5` file for PC testing and a `.h` header file for deployment to the STM32.

#### 2.4 **Model Deployment**

After the model is trained, it is deployed to the STM32F429 microcontroller. The `.h` header file is compiled along with the firmware, allowing the STM32 to perform real-time gesture recognition.

The **nnom library** is used to convert the trained model into a form suitable for deployment on the STM32. The library provides functions to perform inference on the microcontroller using the trained model.

------

### 3. **User Interface Design**

The **user interface (UI)** for the gesture recognition system is designed to facilitate interaction with the hardware and software. It provides a simple and intuitive way for users to collect data, train the model, and test gesture recognition.

#### 3.1 **System Login and Control**

The UI begins with a login screen where the user can access the system’s main functions. The main control panel allows users to start and stop data collection, configure system settings, and initiate model training.

#### 3.2 **Data Collection and Transfer**

The UI includes features for collecting gesture data from the hardware and transferring it to the PC for model training. It allows users to visualize the raw sensor data in real-time and monitor the progress of data collection.

#### 3.3 **Model Training and Testing**

The UI provides an option to train the model on the collected data. After training, users can test the model by running it on the STM32 and visualizing the predicted gestures. This allows for real-time feedback and validation of the system’s performance.

#### 3.4 **Gesture Recognition Display**

Once the model is deployed on the STM32, the UI displays the recognized gesture in real-time as the user performs the corresponding action. The system provides feedback, including a visual representation of the recognized gesture.

------

### 4. **Insights and Experiences**

The development of the gesture recognition system provided valuable insights into embedded machine learning, real-time data processing, and hardware-software integration.

#### 4.1 **Challenges and Solutions**

One of the main challenges in this project was optimizing the CNN model for deployment on

an embedded device with limited resources. The STM32F429 has limited processing power and memory, which required careful tuning of the model’s architecture. Reducing the number of convolutional layers and adjusting the stride of the pooling layers helped balance performance and resource usage.

Another challenge was ensuring reliable data collection from the MPU6050 sensor. Noise and drift in the sensor readings required the implementation of data filtering techniques to improve the quality of the collected data.

#### 4.2 **Key Learnings**

This project reinforced the importance of **data preprocessing** in machine learning applications. Proper normalization and filtering of sensor data are crucial for achieving high recognition accuracy. Additionally, the experience of deploying a machine learning model to an embedded system demonstrated the complexities of working with resource-constrained devices.

#### 4.3 **Future Improvements**

Future work on this project could involve improving the accuracy of gesture recognition by using more advanced models, such as recurrent neural networks (RNNs), to better capture temporal dependencies in the sensor data. Additionally, adding more sensors or improving the sensor calibration could lead to more robust and accurate gesture recognition.

------

### Conclusion

The gesture recognition system based on the STM32F429 development board and the MPU6050 gyroscope is a successful implementation of embedded machine learning for real-time gesture classification. The system demonstrates the feasibility of deploying a convolutional neural network model on an embedded platform for gesture recognition and provides an intuitive user interface for interacting with the system. This project serves as a valuable learning experience in embedded systems, machine learning, and hardware-software integration.



