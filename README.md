# DISPLAYING-THE-MOISTURE-CONTENT-IN-THE-GARDEN-BY-USING-LCD

# ABSTRACT
This system of displaying the moisture content in the garden by using LCD. It uses LCD to display the moisture content of the garden. the observation and communication between the garden owner or observer and the system is achieved through displaying the information about how the moisture of garden it is. If the moisture of the garden had meet with dryness or wetness due to the lack of enough water or over watering in the garden LCD is there to display the content of the moisture in the garden. This project of displaying the garden information it maintains big roles to the people in this manner. Gardening is a good hobby that can boost our health and provide a good profit if applied in large scales. People in urban areas appreciate and enjoy the beauty of nature as carefully manicured grass and flowers in public gardens. Senior citizens find this place best for their social networking, while children enjoy their recreational activities there. Botanical garden generally refers to a place where, variety of flora species are planted and grown for the purpose of scientific study.[1]


# PROBLEMS STATEMENT
 Nowadays people and public care are engaged to built and provide the garden in their homes and public spaces for different purpose such as fruiting garden, public sitting place and botanical garden for filling their hobby. But the they fail to take care about their garden for making them stay in good condition.
To solve this problem, we proposed to uses this system of displaying the moisture content in the garden by using an LCD. It performed with help of soil moisture sensor. The sensor consists of an element that is resistant to corrosion and gives it a long service life and and LCD to display the content of the garden.
The most existing garden problems of garden workers and owner’s garden they have a lot of disadvantages such as watering their garden by using hand and low knowledge of to mean if soil moisture is wetness or whether is dryness so this project its comes as intelligence one to produce the display of moisture content in the garden whit help of soil moisture sensor and LCD to display the present moisture content quickly in short period of time to the present observer. [2]   
                                                                                                                                                                                                                                               # BLOCK DIAGRAM
                                                                                                                                                                       
 ![image](https://user-images.githubusercontent.com/106546186/171027892-8c15f46a-f280-4990-bb8b-16ac84974d30.png)
                                                                                                                                                                      

# DISCRIPTION OF THE BLOCK DIAGRAM:
•	I. The soil moisture sensor is there in the soil of garden. The sensor consists of an element that is resistant to corrosion and gives it a long service life. by measuring the conductivity of the soil (sensor resistance increases when soil dries out and decreases when soil gets wetter)
•	or by measuring the suction pressure at the tip of the probe (which gives an indication of how hard root have to work to extract water from the soil)
•	the soil moisture sensor measures soil moisture grace to the changes in electrical conductivity of the earth (soil resistance increase with drought ) The electrical resistance is measured between the two electrodes of the sensor. A comparator activates a digital output when adjustable threshold is exceeded.  
II. Potentiometer: the use of potentiometer in soil moisture sensor  is that you can set a threshold by using a potentiometer, so that when the moisture level exceeds the threshold value, the module will output LOW  otherwise HIGH. Again this setup is very useful when you want to trigger an action when certain threshold is reached [3]
III. Microcontroller: the main functions of the microcontroller are reading the values from the soil moisture sensor, displaying appropriate message on the LCD and and also is where the instruction of the programing language is executed 
IV. Liquid crystal display (LCD):
A liquid-crystal display (LCD) is a flat-panel display or other electronically modulated optical device that uses the light-modulating property of liquid crystals combined with polarizers. Liquid crystals do not emit light directly, instead using a backlight or reflector to produce images in color or monochrome.[4]  

# FRITZING CIRCUIT DIAGRAM 
 ![image](https://user-images.githubusercontent.com/106546186/171027949-aff89f9f-e853-4265-9f21-c89876197f16.png)

# SOURCE CODES
#include <LiquidCrystal.h>


int sensorPin = A0; // select the input pin for the potentiometer


int s_V = 0; // variable to store the value coming from the sensor


const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;


LiquidCrystal lcd(rs, en, d4, d5, d6, d7);


void setup(){


  pinMode(sensorPin, INPUT);
  
  
   lcd.begin(16, 2);
   
   
}


void loop(){


 // Get a reading from the Moisture sensor:
 
 
  s_V = analogRead(sensorPin);  
  
  
/*------Display Moisture Sensor Value in Serial Monitor------*/


 lcd.print("M_Sensor Value:");
 
 lcd.println(s_V); 
 
 //Display the Moisture Percentage
 
 float m_Percentage;
 
 m_Percentage= (s_V/1023)*100;

 
 //Display the plant need
 
 if(s_V < 300){
 
  lcd.println("much water, I might get hurt");
  
 }
 
 else if(s_V > 300 && s_V < 700){
 
  lcd.println("I feel so comfortable");
  
 }
 
 if(s_V > 700){
 
  lcd.println("I am thirsty, give me water");
  
 }
 
 lcd.print("\n");
 
 delay(3000);
 
}
# PROTEUS CIRCUIT
 ![image](https://user-images.githubusercontent.com/106546186/171028118-64543c8d-852e-412d-9b7a-71a79dec3620.png)

# PROTEUS SIMULATION WHEN GARDEN THERE IS NO ENOUGH WATER
 ![image](https://user-images.githubusercontent.com/106546186/171028092-e4c292f2-4a78-4e27-a932-b7dbd97702b3.png)

# PROTEUS SIMULATION WHEN GARDEN THERE MUCH WATER THAN WHAT NEEDED
  ![image](https://user-images.githubusercontent.com/106546186/171028146-1fd1b4a6-b097-4691-8449-7a76bedf1f0c.png)
                                      
# Reference
[1]	U. B. Mahadevaswamy, “Design and Development of Soil Moisture Sensor,” vol. 3075, no. 4, pp. 24–28, 2021, doi: 10.35940/ijitee.D8438.021042.
[2]	D. Pdf, D. Full, P. D. F. Package, and T. Pdf, “Automated Gardening Portable Plant Using IoT,” no. 1, pp. 1–8.
[3]	S. M. Sensor, I. Soil, and M. Sensor, “Interfacing Soil Moisture Sensor with Arduino,” pp. 1–13, 2018.
[4]	R. Posts, “Arduino Soil Moisture Sensor with LCD Project,” 2021.

# Implemented by: - UWASE Pascaline
#                 -TURIBAMWE Bonheur
