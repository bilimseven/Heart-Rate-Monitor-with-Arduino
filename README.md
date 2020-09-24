# Heart-Rate-Monitor-with-Arduino

Hello everyone, in this article, we will learn to read the pulse data using the Pulse pulse sensor, one of the medical sensors, and display the result on the Nokia 5110 screen. In this way, we will have produced our own heart rate monitor.

Materials you need for the project described in this article: 
*Arduino UNO 
*Pulse Pulse Meter 
*Nokia 5110 Screen 
*Jumper Cables

![WhatsApp-Image-2019-08-26-at-14 39 41-1280x720](https://user-images.githubusercontent.com/71852248/94204158-6a171280-fec9-11ea-8099-0754ee2b3d53.jpg)

What Is a Pulse Heart Rate Monitor and How Does It Work?
First of all, let's start by getting to know Pulse Pulse Meter, one of the most important materials of our project. Pulse Heart Rate Meter is a sensor that can be fixed to your fingertip or ear to measure your heart rate easily. It is possible to supply this sensor with 3V or 5V. You can take a clean and stable measurement thanks to the noise canceling circuit on it.

The working principle of the Pulse Pulse Meter is as follows: The sensor measures how much of the light it sends to your fingertip or your ear is reflected and gives an analog value between 0 and 1023 on the signal pin. This value rises during the pulse rate and then decreases again. The code we will write to Arduino measures our pulse rate per minute using these changes.

Heart Rate Monitor Project
Our project will consist of two parts. In the first part, we will make the connection between Pulse sensor and Arduino. After successfully completing this part, we will reflect the pulse rate we obtained to our 5110 screen. Let's start with the first part.

We make the sensor connections like this:
