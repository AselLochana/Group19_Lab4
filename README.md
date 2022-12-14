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

<img src = "https://user-images.githubusercontent.com/111522334/185549955-b46265aa-3ba2-4233-a8ad-ecdfae03fb34.png" width = "900" height = "500"/>

<p>
 
 
 </p>
 
#### Code Development
<li> Configuration bits and Interrupt Service Routine
<img src = "https://user-images.githubusercontent.com/111522334/185663463-da0c525d-a96d-44b2-85fe-dbd216f81ef8.png" width = "1200" height ="600"/>
<li> Main program
<img src = "https://user-images.githubusercontent.com/111522334/185663891-b8271524-f3e2-4d71-a3bc-29e941cf7914.png" width = "1000" height ="600"/>
<p>
 
 </p>

### Circuit Manufacturing Procedure
The foundation of the PCB which is the laminate board comprises of epoxy resin and glass fiber. A suitable body for holding the copper that supports the PCB is laminate. The foundation of the PCB is made of robust, dust-resistant substrate material. Each side of the copper was already bonded. To disclose the pattern from the films, the copper is whittled away during the process. The inner layers were aligned with the outer layers by the registration holes. The layers were inserted into an apparatus known as an optical punch, allowing precise correspondence for the precise punching of registration holes.

<p>
 
 </p>


#### PCB Layout

<img src = "https://user-images.githubusercontent.com/111522334/185552363-5a16de92-25a2-4aaa-bf95-781fc5cd8978.png" width = "800" height = "600"/>

<p>
 
 </p>

#### 3D PCB Layout
<img src = "https://user-images.githubusercontent.com/111522334/185554075-ae9bf24a-fbbc-41be-9a97-31692c311f6d.jpg" width = "800" height = "400"/> 

<p>
 
 </p>

#### PCB Design
<img src = "https://user-images.githubusercontent.com/111522334/185554429-1f19be33-a856-46b2-aa2d-e6655c30034c.png" width = "800" height = "600"/>

<p>
 

 </p>


### Final Build

<img src = "https://user-images.githubusercontent.com/111522334/185660446-04e12651-464d-4ab2-9d3d-12c5eb47b705.jpeg" width = "600" height = "500"/>
<img src = "https://user-images.githubusercontent.com/111522334/185647379-c049fcc3-38c1-4686-b8b6-bf6e88d136a2.png" width = "900" height = "500"/>

Even though the PCB acts as the main system of operation, the external peripherals such as the LEDs, DC motors, and sensors were placed externally on a breadboard and connected with jumper cables to build up the working system. 

<p>
 
 
 </p>

## RESULTS AND OBSERVATIONS
When the sensors 1 alone is activated the motor 1 switches on. Furthermore, when sensor 1 and 2 are both activated the motor 1 continued to be switched on. However, when sensor 1, 2, and 3 were activated together the motor 1 switched off while motor 2 switched on for 500 milli seconds.
 
https://user-images.githubusercontent.com/111522334/185673345-ce0db8b1-97f9-4cb1-b29b-215a215a8d7d.mp4

 
## DISCUSSION
In this laboratory experiment, a PCB based circuit was created. However, the DC motors and the IR obstacle sensors were connected to breadboards and then were externally connected to the PCB. The main reasons for choosing IR obstacle sensors were the ease of use and the ability to obtain digital inputs rather than analog inputs. Furthermore, these sensors sends a logic low as an input once activated. Therefore, the code which was developed for switches which was programmed to give a logic high when activated had to be changed accordingly. When taking the two DC motors into consideration, the motors could not be directly connected to the output ports and a 2-relay module was used to connect the motors. However, in order to check the accuracy of the edited code and the sensors 2 LED bulbs were used instead of motors. Once the code and the accuracy of the components were determined the experiment was done using the DC motors.
 
#### Components which were externally connected
<img src = "https://user-images.githubusercontent.com/111522334/185676258-70c2077b-7a92-4bf2-a015-0a6eb1633a44.png" width = "500" height = "600" />


## CONCLUSION 
The lab activity was completed with the aid of the Proteus 8 professional software and physical components. The schematic layout was constructed on the Proteus software and the relevant PCB layout was derived. DC motors, sensors, PIC16F877A microcontroller along with other components were properly used to build the circuit. The properties and special features of these components were understood. The required 'C language code' was constructed on MPLabs. More knowledge was gained about microcontroller programming and associated concepts such ???Interrupts???, ???delays???, and their application scope because of performing this experiment. During this task certain errors were found and were rectified using necessary measures.
