# Wireless Audio Notice Board System

## Objective

The **Wireless Audio Notice Board System** is an IoT-based real-time wireless public announcement system developed using **ESP32 microcontrollers** and a **Flutter mobile application**. The project eliminates the need for traditional wired public address systems by enabling live voice announcements over a Wi-Fi network. Audio can be transmitted either from an **INMP441 I2S MEMS microphone** connected to an ESP32 transmitter or directly from a **Flutter mobile application**, and played through ESP32-based receiver units connected to speakers via the **MAX98357A I2S amplifier**.

The project demonstrates the implementation of embedded systems, wireless communication, and mobile application integration to build a scalable, low-cost, and low-latency audio broadcasting solution suitable for educational institutions, offices, hospitals, factories, and other public environments.

---

## Skills Learned

* Embedded Systems Development using ESP32
* ESP32 Wi-Fi Communication and Networking
* Real-Time Audio Streaming using UDP
* I2S Audio Interface Configuration
* Flutter Mobile Application Development
* Audio Capture and Processing
* Digital Audio Amplification
* IoT System Architecture Design
* Embedded C Programming
* Hardware Integration and Circuit Design
* Network Communication and Debugging
* System Testing and Performance Optimization

---

## Tools Used

* **ESP32 DevKit V1** – Main processing unit
* **Flutter** – Mobile application for wireless voice announcements
* **Arduino IDE** – ESP32 firmware development
* **Embedded C/C++** – ESP32 programming
* **INMP441 MEMS Microphone** – Hardware audio input
* **MAX98357A I2S DAC Amplifier** – Audio output
* **I2S Communication Protocol** – Digital audio transfer
* **UDP Protocol** – Low-latency audio streaming
* **Wi-Fi Network** – Wireless communication
* **Serial Monitor** – Debugging and Testing

---

# Steps

Below are the key implementation stages of the Wireless Audio Notice Board System.

---

## 1. System Architecture Design

The project architecture was designed with a wireless transmitter, Wi-Fi communication network, and multiple receiver units. The system supports audio input from both an ESP32-connected MEMS microphone and a Flutter mobile application.

**Ref 1: System Architecture**

This diagram illustrates the complete architecture of the Wireless Audio Notice Board System, showing communication between the Flutter application, ESP32 transmitter, Wi-Fi router, receiver ESP32, amplifier, and speaker.

```markdown
![System Architecture](https://github.com/Anuranj-P-M/Wireless-Audio-Notice-Board-System/blob/main/System%20Architecture.png)
```

---

## 2. Audio Capture

Voice announcements are captured using either:

* INMP441 Digital MEMS Microphone connected to ESP32
* Flutter Mobile Application acting as a wireless microphone

The ESP32 processes incoming digital audio through the I2S interface before packetizing it for transmission.

**Ref 2: Audio Capture Workflow**

```markdown
![Audio Capture](images/audio_capture.png)
```

---

## 3. Wireless Audio Transmission

The processed audio packets are transmitted over the local Wi-Fi network using the UDP protocol, providing low-latency communication between transmitter and receiver units.

**Ref 3: Wireless Transmission Workflow**

```markdown
![Wireless Transmission](images/wireless_transmission.png)
```

---

## 4. Audio Playback

The receiver ESP32 continuously receives incoming UDP packets, reconstructs the audio stream, and sends it to the MAX98357A I2S Digital Amplifier, which drives the speaker.

**Ref 4: Audio Output Workflow**

```markdown
![Audio Output](images/audio_output.png)
```

---

## 5. Flutter Mobile Application

A cross-platform Flutter application was developed to function as a wireless microphone. Users can connect to the Wi-Fi network, select a receiver, and broadcast live announcements directly from their smartphones.

### Features

* Live Voice Streaming
* Wireless Announcement Transmission
* ESP32 Receiver Selection
* Low Latency Audio
* User-Friendly Interface

**Ref 5: Flutter Application**

```markdown
![Flutter App](images/flutter_app.png)
```

---

## 6. Hardware Integration

The hardware setup consists of:

* ESP32 Transmitter
* ESP32 Receiver
* INMP441 MEMS Microphone
* MAX98357A I2S Amplifier
* Speaker
* Wi-Fi Router
* Power Supply

The transmitter captures and streams audio, while the receiver reproduces the announcements in real time.

**Ref 6: Hardware Setup**

```markdown
![Hardware Setup](images/hardware_setup.png)
```

---

## 7. System Testing

The system was tested for:

* Audio Clarity
* Wi-Fi Stability
* Transmission Latency
* Packet Loss
* Speaker Output Quality

### Results

* Clear real-time audio transmission
* Stable UDP communication
* Minimal transmission delay
* Reliable Wi-Fi connectivity
* High-quality speaker output

**Ref 7: Testing Results**

```markdown
![Testing](images/testing_results.png)
```

---

## Future Enhancements

* Multi-room broadcasting
* Broadcast groups and zone selection
* Audio recording and scheduled announcements
* Secure encrypted audio streaming
* Cloud-based announcement management
* AI-powered noise suppression
* Mesh networking for extended coverage
* Battery-powered receiver units
* Push-to-Talk functionality
* Announcement history and playback

---

## Applications

* Schools and Colleges
* Universities
* Hospitals
* Offices
* Railway Stations
* Airports
* Shopping Malls
* Factories
* Smart Buildings
* Government Institutions

---

## Project Highlights

* Real-time wireless voice announcement system
* Dual audio input (Flutter App + INMP441 Microphone)
* ESP32-based embedded architecture
* Low-latency UDP audio streaming
* Digital audio using I2S protocol
* Cost-effective and scalable design
* Modular hardware architecture
* Mobile-controlled public announcement system
* Suitable for IoT and Smart Campus applications
