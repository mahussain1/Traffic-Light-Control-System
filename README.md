# Traffic Light Control System- A Model-Based Software Design approach
In this project, a Traffic Light Control System (TLCS) was designed using a model-based software approach. The project was carried out according to **Agile Software Development Process** where a project was first planned, and system requirements were listed in Requirement Specification Sheet. Then a software design process was followed by creating the system architecture of TLCS. Later, a Software Design Block diagram was developed and implemented using **Simulink/State Flow Graphs**. After that, a test harness was created in which different test cases were verified to check if the requirements of the project are met.

The task was to develop a new traffic light control system that automatically controls the lights for pedestrians and cars. The system must react to user-operated push-button requests. The requests must be indicated with an optical indicator. The lights for cars may have the following exclusive states: 

- green
- yellow
- red
- red-yellow

The lights for pedestrians can have the exclusive states green and red. The control system must control a pedestrian light, a push button, and an optical indicator on each side of the road. Push-button actions on one side must be indicated on the other side too. There is one light for the cars in each direction.

Below are the four main requiremnts that were used to test in test verification process:

- Vehicle stopping
- Vehicle pre-crossing
- Vehicle crossing
- Vehicle stopping

The time between these was dependent upon wheather a push button is pressed by Pedestrain or not. For a demonstation prupose, only the time for Vehicle crossing state is reduced by 5 sec when a push button is pressed to cross the road. The Finite State Machine (FSM) implementated using Signal Flow Graphs follows the pattern as shown in the table below.

 
  
<table>
  
   <tr>
    <td colspan="5"><p align="center"><strong>Individual State durations (Sec) </strong></p> </td>
  </tr>
  
  <tr>
    <td rowspan="1"><b> States </b></td>
    <td colspan="2"><b> Push button pressed</b> </td>
    <td colspan="2"><b> Push button not pressed </b></td>
  </tr>
  
  <tr>
    <td></td>
    <td>Individual state time</td>
    <td>Time elasped</td>
    <td>Individual state time</td>
    <td>Time elasped</td>
  </tr>
  
   <tr>
    <td>Initialization</td>
    <td>2</td>
    <td>2</td>
    <td>2</td>
    <td>2</td>
  </tr>
     <tr>
    <td>Vehicle Stopping</td>
    <td>10</td>
    <td>12</td>
    <td>10</td>
    <td>12</td>
  </tr>
     <tr>
    <td>Vehicle Pre-crossing</td>
    <td>5</td>
    <td>17</td>
    <td>5</td>
    <td>17</td>
  </tr>
     <tr>
    <td>Vehicle Crossing</td>
    <td>15</td>
    <td>32</td>
    <td>20</td>
    <td>37</td>
  </tr>
     <tr>
    <td>Vehicle Precrossing</td>
    <td>3</td>
    <td>35</td>
    <td>3</td>
    <td>40</td>
  </tr>
</table>
