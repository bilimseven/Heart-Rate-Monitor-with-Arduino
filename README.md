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

![pulse2-696x491](https://user-images.githubusercontent.com/71852248/94204401-da259880-fec9-11ea-9b70-c7fd2ccc3693.png)

It's time to write the code for the Arduino. After opening the Arduino IDE, the first thing we need to do to use our sensor is to install the necessary library on our computer. To do this, we need to click on the "Tools" option from the options above and click on the "edit libraries" option from there. After this process, the tab called "Library Manager" will open. To install the necessary library from here, we need to write "pulse sensor playground" in the search section, select the latest version from the "select version" section and press the "Install" button.

Reading Data From Pulse Sensor
Now that we have successfully installed the required library, we can move on to the next step. As I explained in the section above, Arduino decides whether the pulse occurs or not according to the magnitude of the analog value from the sensor. For this reason, we need to set a threshold in advance. In this way, Arduino will be able to understand that the pulse is happening when a signal is above the threshold value we have determined. In order to determine the threshold value, we need to see the values ​​from the sensor. The easiest way to do this is to use one of the sample codes in the library we downloaded. In order to open the necessary sample code file, we click File> Examples> Pulse Sensor Playground> GettingStartedProject. Then we upload the code opened on the screen to our Arduino. Now we click on Tools> Serial Plotter to view the incoming signals on our computer. You will see a progressive line on the screen in the light of the data from the sensor. Now you need to insert your fingertip into the sensor. Now, you should see that waves are formed on the screen as in the image below. If this is the case, everything is going well and we can continue on our way. However, if you could not get a signal flow similar to the one below, you can review the "Troubleshooting" section at the bottom of this article.

![cmon](https://user-images.githubusercontent.com/71852248/94204619-3d172f80-feca-11ea-8e28-e41eb35046e5.jpg)

Determining the Threshold Value The next step is to set the threshold value according to the graph on your screen. For this, we have to determine such a value that the rises on the chart should rise above this value, but the parts other than the rises should also stay below this value. For example, in the image below, 520 is a suitable threshold value. But you should determine your own value according to the graph on your screen because it may differ.

[cmon-1](https://user-images.githubusercontent.com/71852248/94204739-7f407100-feca-11ea-8cc2-52df00f520a2.jpg)

Now that we have determined our threshold value, we measure the pulse value with our sequence sensor and print it on our Nokia 5110 screen. For this, we must first add our 5110 screen to our circuit. You can see how this is done in the circuit diagram below.

![5110](https://user-images.githubusercontent.com/71852248/94204870-c0d11c00-feca-11ea-8237-614ea6b7cd87.png)
