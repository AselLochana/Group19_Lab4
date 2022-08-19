# Microcomputers Group19 Lab4 Report
Controlling the waterlevel of a water tank using the PIC16F877A microcontroller and digital sensors

<p>
 
 
 </p>
 
## ABSTRACT
A water level controlling system was developed for a water tank mainly using the PIC16f877A microcontroller. A 'C language code' was developed using the MPLabs software, while a schematic layout of the required circuit was designed on the Proteus software and was converted to a PCB layout to obtain the necessary circuit that was needed. DC motors, IR obstacle sensors, etc were also mainly used. 

<p>
 
 
 </p>

## INTRODUCTION
The PIC16F877A microcontroller consists of 40 pins, while 33 pins are for inputs and outputs. This microcontroller is widely used in microcontroller projects and digital electronic circuits. As a result of having the Flash Program Memory this microcontroller can write-erase as many times as possible which is one of its main advantages. In this assignment, the microcontroller is used to operate the logics under external stimuli input/output to and from it respectively. 
DC motor is an electrical equipment which converts electrical energy into mechanical energy. This conversion is done by creating a magnetic field which is powered by direct current. The main reason for DC motors to be widely used in comparison with other types of motors is The ability to precisely control the speed. A digital sensor is a type of device which measures a physical input and converts its data in a way which can be read by machines and humans. In this experiment IR obstacle sensors were used. 


<p>
 
 
 </p>

### APPARATUS
<ul>
<li>PIC16F877A microcontroller
 <p>   
 </p>

 
<img src = "https://user-images.githubusercontent.com/111522334/185538050-578aa42d-5d42-4172-bd8c-47c57215d083.jpeg" width = "300" height = "100"/>

 <p>  
  
  
 </p>
 
 <li>PicKit 3
 
 <p>
  
  
 </p>
 
<img src = "https://user-images.githubusercontent.com/111522334/185543947-59d9e341-4072-4ce2-a231-3e3bf415df5e.png" width = "300" height = "200"/>

  <p>
  
  
 </p>
 
<li>Jumper wires
<p>   
 </p>

 
<img src = "https://user-images.githubusercontent.com/111522334/185539291-193c86b2-6af5-4ecb-905b-db837cd492db.png" width = "300" height = "200"/>

 <p>  
  
  
 </p>
 
<li>Breadboard
 
 <p>
  
  
 </p>
 
 <img src = "https://user-images.githubusercontent.com/111522334/185539557-84986c8d-99f9-4805-a98d-5440deda2673.png" width = "300" height = "200"/>

 
 <p>
  
 </p>

<li>Copper PCB

 <p>
  
 </p>
 
<img src = "https://user-images.githubusercontent.com/111522334/185540536-77da4b1a-9777-4719-9cdb-138ca2cdaa9a.jpeg" width = "300" height = "265" align = middle/>

 <p>   
  
 </p>
 
<li>LED 
 <p>
  
 </p>
 
<img src = "https://user-images.githubusercontent.com/111522334/185541488-1caeb587-0bdc-48ab-ba5e-f2cb3866692c.png" width = "150" height = "170" align = middle/>

 <p>   
  
 </p>

<li>Crystal oscillator 20Mhz

 <p>
  
  
 </p>
 
 <img src = "https://user-images.githubusercontent.com/111168422/184554894-85998104-95a1-4cae-ba83-5375edf1b312.png" >

 <p>
 </p>
 
<li>22pF Capacitors
 
 <p>
 </p>
 
 <img src = "https://user-images.githubusercontent.com/111168422/184554982-d766fb28-d2b9-4316-828e-3b4dad6428e1.png" width = "150" height = "150" >

 <p>
 </p>
 
<li>IR (Infrared) obstacle detection sensors
 
 <p>
  
  
 </p>
 
 <img src = "https://user-images.githubusercontent.com/111522334/185542171-d9db9a89-e609-4872-b267-e3fdd9aeb904.png" >

  <p>
  
  
 </p>

<li>5V DC motors
 
  <p>
  
  
 </p>
 
 <img src = "https://user-images.githubusercontent.com/111522334/185542721-dcadaacf-fdcd-4076-acb3-a37917446292.png" >
 
  <p>
  
  
 </p>


<li>10k ohm resistor

 <p>
  
  
 </p>
 
 <img src = "https://user-images.githubusercontent.com/111522334/185544255-b4b4dbb6-69de-4f83-bbdd-c2db028962eb.png" >

 <p>
 </p>

 
<li>330 ohm resistor

 <p>
  
  
 </p>
 
 <img src = "https://user-images.githubusercontent.com/111522334/185544333-ff7dec27-b608-4188-a223-98084a2d8cff.png" >

 </ul>
 <p>
 </p>
 

## METHODOLOGY

### Working Process
The water tank has 3 levels of water storage which can be detectable. The tank system consists of 1 input motor (located relatively lower) to pump in water when it is under operation and another motor (located at the top) which expels water from the tank. The first 2 levels can be filled with the input motor uninterruptedly. Once the input motor starts pumping water above the level of sensor in the 3rd level, the input of that sensor will trigger the output motor to expel water for a duration of 500ms and stop and halt the input motor, simultaneously. 
<img src = "https://user-images.githubusercontent.com/111522334/185535647-f1e5bb28-e8c4-4a5a-9f09-cf2eff037f03.png" width = "800" height ="400"/>

<p>
 
 
 </p>

### Truth Table
<img src = "https://user-images.githubusercontent.com/111522334/185536298-f010ee95-7c28-4b6c-9562-18c9bd990ef2.png" width = "800" height ="200"/>

<p>
 
 
 </p>

### Simulation and Implementation
The design for the PCB were developed with the aid of Proteus 8 professional, which is a software that also allows in-system simulationS thus, making it an ideal computer-based tool.
<p>
 
 
 </p>
 
#### Schematic Design 

<img src = "https://user-images.githubusercontent.com/111168422/184474878-cc7ec50e-db44-469c-8861-7aca1c22faf3.jpeg" width = "900" height = "500"/>

<p>
 
 
 </p>
#### Code Development
<img src = "https://user-images.githubusercontent.com/111522334/185546425-b8aadc19-f68e-490a-b58e-92413922640a.png" width = "1200" height ="600"/>
<img src = "https://user-images.githubusercontent.com/111522334/185547025-062fd2f2-79ac-411d-9f59-e6d1f18eee89.png" width = "1000" height ="600"/>
<p>
 
 </p>

### Circuit Manufacturing Procedure
The PCB consists of epoxy resin and glass fiber, and the foundation of the PCB is made of robust, dust-resistant substrate material. Each side of the copper is already bonded. To disclose the pattern from the films, the copper is whittled away during the process. The layers were introduced with alignment punches and once they were all clean and prepared to guarantee that they line up. The inner layers were aligned with the outer layers by the registration holes. The layers were inserted into an apparatus known as an optical punch, allowing precise correspondence for the precise punching of registration holes.

<p>
 
 </p>
 
## PCB Design

<b> A PCB is designed using the Proteus software which is baised on the exsiting schematic design  </b>
<p>
 

 </p>




### PCB layout 

<b> The PCB layout is genarated using the inbuilt PCB designing facilty of the Proteus Software and we use a top Copper Layout </b>

<img src = "https://user-images.githubusercontent.com/111168422/184475254-48a2ccd2-a423-4db6-a665-fbf007c17365.jpeg" width = "900" height = "500"/>

Manual tracing was done using the T50 line since that gives the appropiate width to be practically designed. Marker ink was used to etch the PCB on to the circuit and FeCl3 was used to remove the Copper that had not been etched by the marker ink therefore giving us the required layout of the circuit.   

<p>
 
 </p>

### 3D PCB layout

The three dimensional view of the PCB with the components 

<p>
 
 </p>

#### Bottom View

<img src = "https://user-images.githubusercontent.com/111168422/184476003-4653df47-2c4b-4597-a753-383ee8d157ca.png" width = "900" height = "500"/>

<p>
 
 
 </p>


### Desgined PCB 

The PCB obtained after soldering the circuit 

<img src = "https://user-images.githubusercontent.com/111168422/184480522-3171153e-bba6-4bdd-b64a-f47f7570b89e.png" width = "900" height = "500"/>

A jumper wire was connected since the connection cannot be made using a tracing line since we found no way to avoid the fundermental design error occuring when connecting the grounds therefore to mitigate this error a jumper wire cable is used. The base is used to connect the pic microcontroller.The header connectors are solderd on to the circuit as well as the other componenets. The header connectors are used to interface the circuit with the external sensors and the output.

<p>
 
 
 </p>
 
 
 ### PCB physical design process 
 
<ol>
 <li> Design the PCB in proteus software
 <li> Print out the design onto the shiny side of the transfer paper
 <li> Sand the copper plate so there is a rough surface for the design to stick to when transfered
 <li> Wash the copper with some water and rubbing alcohol and let it dry
 <li> Cut out the designs and place them face down on the copper
 <li> Run the copper plate with the design face down through a laminator 5-7 times until the plate is hot
 <li> Place the PCB into the etching solution and agitate for 25-30 minutes or until all the copper has dissolved around the design
 <li> Once all the copper is gone rinse it in the water bath, let it dry and use rubbing alcohol to remove off the ink transfered onto the PCB
 <li> And now you have an etched PCB board after that we drill the holes
  
  
 </ol> 
 


## Code

// PIC16F877A Configuration Bit Settings

// 'C' source line config statements

// CONFIG

#pragma config FOSC = HS        // Oscillator Selection bits (HS oscillator)

#pragma config WDTE = OFF       // Watchdog Timer Enable bit (WDT disabled)

#pragma config PWRTE = OFF      // Power-up Timer Enable bit (PWRT disabled)

#pragma config BOREN = OFF      // Brown-out Reset Enable bit (BOR disabled)

#pragma config LVP = OFF        // Low-Voltage (Single-Supply) In-Circuit Serial Programming Enable bit (RB3 is digital I/O, HV on MCLR must be used for programming)

#pragma config CPD = OFF        // Data EEPROM Memory Code Protection bit (Data EEPROM code protection off)

#pragma config WRT = OFF        // Flash Program Memory Write Enable bits (Write protection off; all program memory may be written to by EECON control)

#pragma config CP = OFF         // Flash Program Memory Code Protection bit (Code protection off)

// #pragma config statements should precede project file includes.

// Use project enums instead of #define for ON and OFF.

#define _XTAL_FREQ 20000000

#include <xc.h>

#include <htc.h>








void activate1() 

{

    RB1 = 1;
    
    RB3 = 0;       //the condition one was activated triggering the RB! connected motor and not triggering the RB3 connected motor 
    
}

void activate2()

{

    RB1 = 1;
    
    RB3 = 0;      //the condition two was activated triggering the RB! connected motor and not triggering the RB3 connected motor 
    
}


void activate3()

{

    RB1 = 0; //the condition three was activated not triggering the RB1 connected motor and  triggering the RB3 connected motor for 500ms
    
    RB3 = 1;
    
    __delay_ms(500);
    
    RB3 = 0;
   
    
  }

void main()

{

    
    TRISB1 = 0;     //Motor One - RB1  //PortB deaclared as the output ports
    
    TRISB3 = 0;     //Motor Two - RB2
    
    TRISC0 = 1;     //Switch one
    
    TRISC3 = 1;     //Switch two       //PortC deaclared as the input ports
    
    TRISC4 = 1;     //Switch three
    
    
    
    
   
    
    while(1) {           //loop to infinty times till argument is met 
    
    if(RC4 == 0) {                      //check if switch three is not set
        
        
            
            if(RC0 == 1 && RC3 == 0)     //check if switch one and two are not set
            {
                
                activate1();                    //go to condtion one
                
                
                
            }
            
            if(RC0 == 1 && RC3 == 1) {        //check if switch one and two are set 
                
                activate2();                  //If true go to condtion two
                
            }if(RC4 == 1){
                
                break;    
                
            }else{
                
                RB1 = 0;     //else deactivate all motors
                
                RB3 = 0;
                
                
            }
        }
    
    }
    
        if(RC4 == 1)     //check if switch three is not set
        
        {
            
                if(RC0 == 1 && RC3 == 1)     //check if switch one and two are set
                
                {
                
                    activate3();    //goto condtion three
                    
                    
                }else{
                    
                    RB1 = 0;    //if not deactivate all motors
                    
                    RB3 = 0;
                    
                }
                
            }
            
            
            
        
    
}

<p>
 
 
 </p>
      
### Code discussion

The code we use in this programme is created using the MPLAB X IDE V6.00. This was executed without the use of interrupt registers as analogue sensors are used the transtion edges would be spontaneous and instantaneous to be tracked by the intruept service routine therefore we used a regular bit test for each input pin nested within the while loop and test for each loop the corresponding status required and therby calling the subroutine.If loops are used to check the condtions of the input and give the relavant output. 

<p>
 
 
 </p>


## Sensors used
    
 We use a soil moisture sensor to act as the switches of the circuit. This sensor can measure the volumetric content of water inside the soil. This sensor is consists of mainly two parts, one is sensing probs and another one is the sensor module.The probes allow current to flow through the soil, and they then calculate the resistance value based on the soil's moisture content. The Sensor Module receives data from the sensor probes, processes it, and outputs the result as either a digital or analog signal.The Soil Moisture Sensor can provide both types of output Digital output (DO) and Analog output(AO).

### Process of the soil moisture sensor

When more water in the soil then prob’s conductivity will increase and resistance will decrease. So, a Low amount of voltage from the sensing probe is given to the Inverting input (2) of the IC. Then the LM393 Comparator IC compares this voltage with the threshold voltage. In this condition, this input voltage is less than the threshold voltage, so the soil sensor output goes LOW (0).When less water in the soil then prob’s have low conductivity and high resistance. So, a High amount of voltage from the sensing probe is given to the Inverting input (2) of the IC. Then the LM393 Comparator IC compares this voltage with the threshold voltage. In this condition, this input voltage is greater than the threshold voltage, so the sensor output goes High (1).

  
<img align = "middle" src = "https://user-images.githubusercontent.com/111168422/184584803-808fbaf7-6c91-4b04-a66b-87cb958231b6.png" width = "300" height = "300" />


## Uploading the code

we used the pickit 3 development kit to uplaod the c source code into the microcontroller and this was done via the mplab ipe software.The following connections were performed on the board and the program was uploaded
   
   <img src = "https://user-images.githubusercontent.com/111168422/184998581-09e34ba7-7c57-47b0-9495-1a770974c9b0.png">
   <p>
 
 </p>
 
 <p>
 
 
 </p>
 
   
   <img src = "https://user-images.githubusercontent.com/111168422/184998718-62798101-bcc0-4a78-bf4b-39365d39e141.png" >

<p>
 
 </p>
 
 Uploading the programe after production of the programme
 

<img src = "https://user-images.githubusercontent.com/111168422/184999393-72cf3133-bb67-4380-8066-fede9a669d6b.jpeg" height = "300" width = "500" />

## Implementation

<b> We built the circuit using 2 breadboards and placing the sensors and the outputs on the breadboards that we had created as shown below </b> 

<img src = "https://user-images.githubusercontent.com/111168422/185463637-f624bbc6-9b0f-45f6-ba44-268334556899.jpg" >

<b> The sensors were dipped in water to obtain the required output as the sensors would behave as the switches of the system </b>

<img src = "https://user-images.githubusercontent.com/111168422/185464662-efdf0261-e0cb-4a5f-b341-e5280c30cecc.jpg" >

### Issues with the sensors

<li> Since the sensors are not hydrophobic we cannot observe the correct output without observing a certain delay 
<li> We should allocate some time for the sensors to dry probably using a piece of cloth which is non static
<li> The sensors take some time to indicate the changes therefore we have to quickly clean them after use
<li> The reason the LED is blinking out of water is due to 
 
 
</li>

### Output Explanation

When we dip the sensors one and two into the water cup it performs the function of switches and the system should funtction according to the truth table we had created 
     <li> When we dip the third sensor the RED Led at the top should light up
     <li> When we dip the second sensor the RED LED should be still lit up
     <li> When we remove the both the above dipped sensors the RED led at the bottom should light up for 500ms 
     <li> When we dip all the three sensors the LEDS should turn off as all switches are off

We account for the delay observed in obtaining the outputs and we should let the nodes dry before we restart the process      
      
      

 
      
    

https://user-images.githubusercontent.com/111168422/185489325-9fd3bcda-93e7-4ace-bda8-5df5d9dc6ff9.mp4






