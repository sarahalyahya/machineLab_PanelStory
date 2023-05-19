# Machine Lab Documentation

## Introduction
This documentation traces the two-month-long work that went into creating our final project for Machine Lab. Our project involves a mechanism that uses six rotating cuboids to display fragments of an image, which come together at a specific time.

## Concept
Our concept was to create a dynamic display using rotating wooden logs that would switch over time, showing different scenery throughout the day. We aimed to bring together elements of movement, design, and time to create an engaging visual experience.
Overtime, our concept shifted slightly to a glitchy image display. 

## Technical Implementation
### Schematic
We started with preliminary sketching to visualize the mechanism and how it would operate. This helped us determine the dimensions and design of the rotating cuboids. We also created a 3D model of the final structure to align our team's vision. The schematic and sketches provided a roadmap for the technical implementation.
![339725760_907543260299120_1735938848632111781_n](https://user-images.githubusercontent.com/57350290/230022350-6f9895e6-8cd6-4281-8086-a843f84c3e58.jpg)

<img width="440" alt="Screen Shot 2023-04-10 at 4 21 27 PM" src="https://user-images.githubusercontent.com/57350290/230901297-a33f8dab-0768-4878-b0a5-bd7c5936060a.png">

### Code
The implementation involved coding the control logic for the stepper motors that rotate the cuboids. We wrote code to synchronize the movements of the cuboids and to display specific image fragments at predetermined times. The code enabled us to control the rotational speed, direction, and timing of the cuboids.
The final I scontrolling the stepper motors, generating random movements, and signaling the progress of the rotation. It is broken down as follows:
- The code starts by including the necessary library, "Stepper.h," which allows us to control the stepper motors.
Next, the code defines the number of steps per revolution for the stepper motors using the constant variable "stepsPerRevolution."
- Then, the code declares two constants, "TRIGGER" and "DONE," which are connected to specific pins on the Arduino board. "TRIGGER" receives a signal from the professor, while "DONE" sends a signal to the professor.
In the setup function, the code initializes the TRIGGER pin as an input and the DONE pin as an output. It also starts the serial communication.
- The loop function is where the main logic of the code resides. Currently, it contains a for loop that iterates 35 times, simulating the reception of a signal from the professor.
- Inside the for loop, a random speed and a random number between 0 and 5 are generated. Each stepper motor's speed is set to the random speed using the setSpeed function.
- Based on the random number generated, the corresponding stepper motor (1 to 6) is moved a quarter of a revolution using the step function.
- After the for loop, there is a delay of 30 milliseconds.
- Finally, the code brings the TRIGGER pin low and sets the DONE pin high to indicate that the operation is complete. It also resets the position of all stepper motors to 0. Then, it brings the DONE pin low again and introduces a delay of 300 milliseconds.

This code primarily serves the glitch concept. However, we also wrote different codes for when our concept required the usage of stepper motors!

### Mechanical Assembly
We designed and built a frame to hold the rotating cuboids. This involved selecting suitable wooden panels and determining the dimensions based on the cuboid size and motor placement. We cut and prepared the wooden panels, drilled metal hubs for attaching the cuboids, and tested the dimensions to ensure smooth rotation.
![IMG_5137](https://user-images.githubusercontent.com/57350290/230916592-1ab7ef33-47e5-495e-85ba-9fc03b1333a8.jpg)
![IMG_5138](https://user-images.githubusercontent.com/57350290/230916676-2fe29cf0-c1fa-40bd-9b02-d3edb860dce6.jpg)
![IMG_5021](https://user-images.githubusercontent.com/57350290/230917293-f13573b5-8854-42aa-98a3-85937ed34eb7.jpg)
### Problems Encountered and Resolutions
Throughout the project, we faced several challenges and problems, including:
- Crooked frame: We discovered that the initial frame we built was not stable. To resolve this, we decided to use two panels—one aluminum for mounting the motors and one wooden for the other end of the metal rods.
- Power supply: We encountered difficulties in determining how to use a single power supply for all the motors. We sought guidance from our professor to find an appropriate solution.
- Wiring complexity: As we connected multiple motors and sensors, managing the wiring became complex. We focused on organizing the wires, soldering them appropriately, and creating wire compartments to ensure a clean and tidy setup.
- Stepper Motor Rotations: Upon connecting our stepper motors, we realized the importance of testing each connection we make, because the motors started behaving in unexpected ways. This meant we had to dedicate hours to debugging (code and wires), rewiring, tightening screws, to make sure that our panels/cuboids are rotating smoothly. 

![IMG_5730](https://github.com/sarahalyahya/machineLab_PanelStory/assets/57350290/fba500bf-d781-425f-b51e-498fe39be403)
![IMG_5729](https://github.com/sarahalyahya/machineLab_PanelStory/assets/57350290/d12a6b2f-8496-4a42-91b1-3720338af8bd)
![IMG_5730](https://github.com/sarahalyahya/machineLab_PanelStory/assets/57350290/7c993374-fed2-4ac7-acf0-333c847f0054)


### Lessons Learned and Future Improvements
Based on our experience, there are a few things we would have done differently:
- More precise frame construction: We would have taken additional care to ensure the frame was perfectly aligned and stable from the beginning.
- Earlier guidance on power supply: We would have sought guidance on power supply configuration earlier to avoid confusion and streamline the wiring setup.
- Advanced planning for wiring: A more detailed plan for wire connections and wire hiding mechanisms would have made the assembly and organization process smoother. 
- Testing more: Instead of testing at the end of every stage, we learned how important it is to test connections as we go!

Overall, we learned the importance of careful planning, precise measurements, and effective collaboration during the implementation of a complex project like ours. We also learned how to adapt to changes and adapt our concept to meet time constraints! 

## Conclusion
This Machine Lab project provided us with hands-on experience in designing and building a mechanism that combines art, technology, and time-based elements. It challenged us to overcome technical hurdles, collaborate effectively, and think creatively. Through this documentation, we hope to share our journey and inspire future students in the Interactive Media department to explore innovative projectsin the realm of interactive installations.
For many of us, this was the first time engaging with a project THIS hands-on. We can definitely say we gained skills that we will carry with us for life!
![IMG_5770](https://github.com/sarahalyahya/machineLab_PanelStory/assets/57350290/85d44111-8fc2-4f91-890a-22bd4ed1d14c)

[Video of it running!](https://youtube.com/shorts/aOi7SYyRU94)
