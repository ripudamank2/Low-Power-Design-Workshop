# Low-Power-Design-Workshop
 Low Power Design is a cluster of techniques and studies that aim at reducing the overall power in the integrated circuit. The integrated circuit designs from CMOS(complementary metal-oxide-semiconductor). Why we choose CMOS because they have low power consumption and high noise immunity. But with low power consumption that doesn't mean it doesn't require power reduction techniques. When the complexity of the circuits increases, power demand also increases. Hence we need to work toward the low power techniques development for all the embedded devices, which you see in your daily life.





### Table of Content
   ##### 1. Introduction to Low Power Design
           a. Why Low Power Desing?
           b. Introduction to CMOS and voltage control techniques
   ##### 2. Low Power Techniques
           a. Low Power Fundamentals
           b. Voltage Control Techniques
   ##### 3. Multi-Voltage Terminology
           a. Deep-Dive into state-space
           b. Basic multi-volatge terminology
   ##### 4. Power Management and Verification
           a. Volatge aware booleans
           b. Power Management and typical errors
           c. Verification strategies of MV design
   ##### 5.Island Ordering and Mobility
           a. Routing and design rule check (DRC)
           b. Power Distribution Network and routing
           c. TritonRoute Features
   ##### 6. Refrences
   ##### Acknowledgements



## DAY_1 - Intorduction to CMOS and Low power Design
System Perofrmance correspond with processing power or circuit speed. Perofrmance of a circuit is measure in MIPS(millions of instruction per second). In old days major concern of VLSI designer was to focus on Area and Time implementation for the Integrated Circuit on Silicon wafer because with increase in complexitiy of circuit the cost of wafer increases. But area and time are not the only parameters which can measure the performance of the circuits. Power consumption also play major role in circuit designing. 

  In all the portable electronics where ever you see the battery, designer need to focus on minimizing power or energy in order to improve the battery life. Hence total power conusmption has become the major concern and surpassed speed-area constraints.
  
 We will not deepdive into Power or Energy formula but will try to understnad the economics of Power/Energy while designing circuits. 
 
 1. Performance --> Reducing power will improve performance.
 
 2. Cost --> Packaging , Battery capacity and shipping also affect Power of the embedded devices.
 
 3. Weight --> Power is a measure of how fast an amount of work is done.
 
 4. Form Facor --> it depends upon the nanometer technolgy used and affect power.
 
 5. Functionality --> how fast your system is performaning.
 
 6. Context of use --> Optimizing power or energy according to the embedded devices we are using.
 
 7. Comfort/Safety --> Heating issue should be considered while designing the circuit.
 


Further more we will try to analyze some case studies related to power or energy in the electronics world.  
**Case 1 :** Why do some devices like the Samsung Note have explosions and others don't ?

 The Phones dont have cooling system like laptops, PC or electric vehicle, so heat must spread out. If that is not happening , the heat will generate faster and material of the battery will start to break down while triggering the chemical reaction. This will leads to a process called **Thermal Runway**. So engineers are working on the design of batteries so that thermal runway can be solved. 
 
   ![FIG:1](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/Screenshot%20from%202021-07-16%2011-39-52.png)

  This picture is thermal image of the different components showing heat produce my the components. 
 
 
 **Case 2:** Cost of fans to be mounted on CPUs in laptops and its characteristics
 
  Cooling is a major concern while designing a PC or laptop. When the workload increases, the hardware starts generating heat. So the performance of the system will reduce with an increase in power consumption. So its very important how you designed and placed the fans so that Airflow should be properly maintained. 
  Thats why fan cost are also increasing slowly in the market . 
 
 
 **Case 3:** The IPhone 6 battery degradation lawsuit
 
 This was also a major problem problem in battery manufacturing where the performance of the IPhone was degrading. So they need to do some upgrades in software to improve the perofrmance of the battery.
 
 
 
 #### Why we Choose CMOS?
 
Voltage Control has become the number 1 choice for Power Management and CMOS are the device which are Voltage Controlled and Current Source. Since you can control the voltage Hence you can maintain the Power in the CMOS devices. 

Voltage is a measure of electric field/force.

Current is rate at which charge flows.

Resistance, Capacitance and Inductance affect the current in cmos devices. 

                                 Mosfet Region of Operation 
![FIG:2](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/MOSFET.svg)

                                 The 7 degree of Voltage Control in CMOS 
                                
![FIG:2](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/volatge_control.png)


                                 Voltage Control Techniques(VCT)

![FIG:3](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/voltage_tech.png)


                                 Application of VCT
                                 
![FIG:4](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/application.png)



## DAY2 - Low Power Techniques

  Power in the CMOS is the combination of Dynamic Power and Static Power. 


![FIG:5](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/power.png)


Below picture show how the power is distributed when we use the laptop for different application.

![FIG:6](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/power_distibution.png)



So this picture explain CPU is not a major culprit of power optimiation but there are lots of other components and process which consume lots of power. 



Power Management tips while designing the circuit. They will sound simple but actually it take lots of knowledge and techniques to apply those concept in real circuit. 


![FIG:7](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/power_energy.png)

There are 4 major parameter in Low Power Design.
1. Denisty 
2. Delivery
3. Leakage
4. Lifetime

![FIG:8](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/balance_power.png)



There are different way to control the Power while playing with voltage of CMOS,  which you can see in the below pictures. 

![FIG:9](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/power_gating.png)

![FIG:10](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/low-vdd.png)

![FIG:11](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/DVS.png)

![FIG:12](https://github.com/ripudamank2/Low-Power-Design-Workshop/blob/main/retention.png)



## DAY_3 - Multi Voltage Terminology





