Club Simulation

Overview
Club Simulation is a Java application that models the dynamics of clubgoers in a club environment. The program utilizes concurrent programming principles to simulate various activities of patrons such as entering the club, getting drinks at the bar, dancing, and eventually exiting. This project aims to showcase threading, synchronization, and concurrency management in Java.

Features

Graphical User Interface: Utilizes a JFrame to display a grid-based representation of the club including exits, a dance area, and a bar.

Thread Management: Each clubgoer is implemented as an individual thread navigating through the grid, showcasing the interaction and synchronization among threads.

Concurrency Control: Employs various synchronization techniques including a CountDownLatch for initial start synchronization and locks for managing access to critical sections such as entrances and exits.

Adjustable Parameters: Users can configure the number of patrons, grid size, and the maximum number of people allowed inside the club.

Interactive Controls: Features buttons to start, pause/resume, and exit the simulation, enhancing user interaction.

Dynamic Counter Updates: The GUI updates counters in real-time displaying the number of clubgoers inside, waiting, and who have left the club.


Classes Used

ClubSimulation.java: Initializes the simulation and user interface.
Clubgoer.java: Defines the behavior and properties of a clubgoer thread.
ClubGrid.java: Manages the grid layout of the club including the positions of clubgoers.
ClubView.java: Handles the graphical representation of the club environment.
GridBlock.java: Represents each block of the grid within the club.
PeopleLocation.java: Tracks the location for each clubgoer.
PeopleCounter.java: Manages counts of clubgoers inside, waiting, and who have left the club.


Requirements

Java Runtime Environment (JRE) and Java Development Kit (JDK) version 8 or higher.


Setup and Installation

Clone the project repository:
git clone [repository URL]
cd [project-directory]


Compile the Java code:
javac clubSimulation/ClubSimulation.java


Run the program:

java clubSimulation.ClubSimulation
Optionally, you can pass parameters to adjust the simulation:

java clubSimulation.ClubSimulation [noClubgoers] [gridX] [gridY] [max]


Example:

java clubSimulation.ClubSimulation 30 10 10 15
Usage
Upon execution, a GUI window will display with controls to start, pause, and quit the simulation. Clubgoers will start outside the club and attempt to enter based on the simulation rules. The GUI provides real-time updates on the number of people inside, waiting outside, and those who have left the club.


Command Line Arguments
The program accepts four optional arguments to tailor the simulation:

noClubgoers: Total number of people to enter the club.
gridX: Number of X grid cells in the club.
gridY: Number of Y grid cells in the club.
max: Maximum number of people allowed inside the club at any one time.


Testing
An example of parameters used to test the simulation: 30 15 15 20. Various synchronization techniques were employed to ensure that entrance and exit doors were accessed by one patron at a time, the maximum number of patrons outside did not exceed the specified limit, and that patrons maintained a realistic distance from each other.

