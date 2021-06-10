## ArduinoSousVide Documentation 

### Project Description.
Our project was orginially intended to be a homemade SousVide using Arduino. A SousVide is a way to cook food to an exact temperature by placing the food in water that is at the exact  temperature that is desired for the food you are cooking. This allows the food you are cooking to virtually never be over cooked due to the temperature of the water never going above the desired temperature of your food. We quickly realized the heating element of the project would be near impossible in the time we had so we decieded to make a waterproof theremoter, with a built in timer. Our project is able to set a desired time and temperatue, and is able to start the set timer once the deisred temperature is reached. This can be used as a sous vide as long as the user has a heating element.


### Psuedo Code
In Psuedocode.ino file
#### Description
The Psuedo code gives us a clear outline for the code, which will help greatly in the long run.

## Onshape Link
[Onshape Link](https://cvilleschools.onshape.com/documents/c3962513f441d4007ffeae5e/w/b6f45b338eec284bfbfb06f5/e/f69b6bea835e3a074534029c)
### Onshape Progress
3/1:

I added a button to the assembly that would turn the tempature sensor on.
Also, I added a Led that would turn on when the tempature reached the desired heat.
I am not totally sure whether we will be able to finish on time or not.

3/19:

I made a final box that has connecters and has the correct demensions and should be able to be printed.
### Pictures of the Current Onshape
  #### These Pictures are of the origanal design for the box, however this design was quickly scraped for a newer version
<img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/zoomedoutversionof%231.PNG" width="500">
<img src ="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/FinalBoxSousVide.PNG" width="500">

### This is a zoomed in version of the Prototype
  #### We quickly realized this design would make no sense and could not really work and would be very hard to put together so we quickly scraped it.
<img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/OnshapeProgress%231.PNG" width="500">

## Sous Vide progress

### Picture of Temp sensor running
<img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/TempSensorWorking.png" width="500">


### Hows the project going?  Are you on time?
 For the coding part of the project I feel like I am on time. I have connected the Temp sesnor to the LCD and it is printing the reading.
 
 
### What major obstacle is keeping you from making better progress on your project?
 For the coding, I am trying to figure out how to code a timer to start when the tempature reading reaches a certain tempature. I coded a timer, but the tempature sensor code is connected to a different library, so im not sure to code that.
 
 ###  "When I return from Spring break
I will add a piezo buzzer to the temp sesnor, so it will be able to alert the user when their deeisred tempature has been reached, and when the timer is up.

### Onshape completion assembly & final box finished early may, documented 5/27
The box after lots of changes and refining was finished and laser cut and even though there had to be two changes that were made manually after it was laser cut I felt that I did a fairly good job in the design and the final product, while not perfect works well enough now that it has been all assembled.

  #### This was a picture of the final drawing that was used to laser cut the final box.
<img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/Cad%20drawing.PNG" width="500">

### The link to the code for the Sous Vide tempature sensor as of 6/3
[Link to the full code](https://github.com/CallanSmith/ArduinoSousVide/blob/main/SousVide.ino/Code)

## Coding Process 
The first major coding problem I ran into was coding the temperature sensor. I came into the project with no knowledge of how to code this paticular sensor ([Link to sensor](https://www.adafruit.com/product/381)) but with these videos ([Helpful wiring video](https://www.youtube.com/watch?v=lIpgGru2Wv0&t=115s), [Helpful coding video](https://www.youtube.com/watch?v=hIkUQZuaTE4&t=399s)) I was able to figure out most of the coding and wiring. The most important things about coding the temperature sensor was inculding the dallas temperature library and the onewire library ([Dallas temp library](https://github.com/milesburton/Arduino-Temperature-Control-Library), [One wire library](https://github.com/PaulStoffregen/OneWire)) and figuring out how to grap and print the code from the sensor itself. I did this by requesting temp with "sensors.requestTemperatures();" and then making the temperatue from the sensor into a value. "tempVal = sensors.getTempFByIndex(0);".
From there I could use the tempVal however I wanted.
The next obstacle of the project coding wise was coding the timer. I orginally was using a countdown timer derived from a project using buttons as the input. I though if I could change the input to tempVal then the timer would work just the same. This however was wrong and the timer was very messy and unneccesarily long. After this the timer code was completly redone using some elements from the old code but also going off the basis of
 hrs = (timeleft / 3600000);
      Min = ((timeleft / 60000) - (hrs * 60));
      sec = ((timeleft / 1000) - ((hrs * 3600) + ( Min * 60)));.

### Pictures of the wiring 
   #### The wiring was fairly easy to do as most things had solutions online of where to put things however, we did have some diffuclty making sure the wires could all fit in the box without disrupting eachother.
 <img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/14A69878-8F72-4409-B98E-1497EADC917C.jpeg" width="500">
 <img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/4B5E5A06-D472-439A-AD14-A4E6F4631837.jpeg" width="500">
 <img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/903867F7-AB3B-468E-ACB7-92A824439F26.jpeg" width="500">
 <img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/B686F7F1-BD84-4023-9FDA-18EBF134B77B.jpeg" width="500">
 <img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/D7A4F2C7-9900-4D98-82B7-F3E741A6B475.jpeg" width="500">

### Pictures of the Completed box
 #### This was the design of the box we finally settled on after lots of tweaking and fiddiling to make sure we had all the parts we needed and places to fit and put them. Even though we had to edit a few things after it was laser cut the box seems to work as intended.
<img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/Assembly%201.PNG" width="500">
<img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/Assembly%202.PNG" width="500">
<img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/Final%20box%20%232.PNG" width="500">
<img src="https://github.com/CallanSmith/ArduinoSousVide/blob/main/images/Final%20box.PNG" width="500">

### Materials List
 * One Button
 * One Piezo Buzzer
 * One Potentiometer + washer 
 * One Breadboard
 * One Lcd with I2C Backpack
 * One tempature sensor
 * 4 Arduino stands
 * 6 laser cut walls, two bottom/top, two sides(same size), other sides(same size)
 * Arduino formatting shield
 * Adequate amount of wires, screws, nuts and bolts
