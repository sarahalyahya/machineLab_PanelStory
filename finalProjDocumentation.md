# Machine Lab Documentation

## Introduction
This documentation traces the two-month-long work that went into creating our final project for Machine Lab. Our project involves a mechanism that uses six rotating cuboids to display fragments of an image, which come together at a specific time.

## Concept
Our concept was to create a dynamic display using rotating wooden logs that would switch over time, showing different scenery throughout the day. We aimed to bring together elements of movement, design, and time to create an engaging visual experience.

## Technical Implementation
### Schematic
We started with preliminary sketching to visualize the mechanism and how it would operate. This helped us determine the dimensions and design of the rotating cuboids. We also created a 3D model of the final structure to align our team's vision. The schematic and sketches provided a roadmap for the technical implementation.

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

### Mechanical Assembly
We designed and built a frame to hold the rotating cuboids. This involved selecting suitable wooden panels and determining the dimensions based on the cuboid size and motor placement. We cut and prepared the wooden panels, drilled metal hubs for attaching the cuboids, and tested the dimensions to ensure smooth rotation.

### Problems Encountered and Resolutions
Throughout the project, we faced several challenges and problems, including:
- Crooked frame: We discovered that the initial frame we built was not stable. To resolve this, we decided to use two panels—one aluminum for mounting the motors and one wooden for the other end of the metal rods.
- Power supply: We encountered difficulties in determining how to use a single power supply for all the motors. We sought guidance from our professor to find an appropriate solution.
- Wiring complexity: As we connected multiple motors and sensors, managing the wiring became complex. We focused on organizing the wires, soldering them appropriately, and creating wire compartments to ensure a clean and tidy setup.

### Lessons Learned and Future Improvements
Based on our experience, there are a few things we would have done differently:
- More precise frame construction: We would have taken additional care to ensure the frame was perfectly aligned and stable from the beginning.
- Earlier guidance on power supply: We would have sought guidance on power supply configuration earlier to avoid confusion and streamline the wiring setup.
- Advanced planning for wiring: A more detailed plan for wire connections and wire hiding mechanisms would have made the assembly and organization process smoother.

Overall, we learned the importance of careful planning, precise measurements, and effective collaboration during the implementation of a complex project like ours.

## Conclusion
This Machine Lab project provided us with hands-on experience in designing and building a mechanism that combines art, technology, and time-based elements. It challenged us to overcome technical hurdles, collaborate effectively, and think creatively. Through this documentation, we hope to share our journey and inspire future students in the Interactive Media department to explore innovative projects in the realm of interactive installations
