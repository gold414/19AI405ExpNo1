<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Saravanan N</h3>
<h3>Register Number/Staff Id: TSML006</h3>


<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Medicine prescribing agent:</h3>
<p>Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>Medicine prescribing agent</strong></td>
    <td><strong>Treating unhealthy, agent movement</strong></td>
     <td><strong>Rooms, Patient</strong></td>
    <td><strong>Medicine, Treatment</strong></td>
    <td><strong>Location, Temperature of patient</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>STEP 1:Identifying the input:</h3>
<p>Temperature from patients, Location.</p>
<h3>STEP 2:Identifying the output:</h3>
<p>Prescribe medicine if the patient in a random has a fever.</p>
<h3>STEP 3:Developing the PEAS description:</h3>
<p>PEAS description is developed by the performance, environment, actuators, and sensors in an agent.</p>
<h3>STEP 4:Implementing the AI agent:</h3>
<p>Treat unhealthy patients in each room. And check for the unhealthy patients in random room</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented</p>

## Code:
```
import random

performance = 0

rooms = {
    "Room 1": 98,
    "Room 2": 102,
    "Room 3": 99,
    "Room 4": 101,
    "Room 5": 97
}

def display_patients():
    print("Patient Temperatures")
    print("----------------------")
    for room, temp in rooms.items():
        print(room, ":", temp, "°F")

def check_patients():
    global performance

    print("\nChecking Patients...\n")

    room_names = list(rooms.keys())
    random.shuffle(room_names)

    for room in room_names:
        print("Agent moved to", room)
        performance -= 1

        temperature = rooms[room]

        if temperature > 98.5:
            print("Temperature:", temperature, "°F")
            print("Patient has Fever")
            print("Medicine Prescribed")
            performance += 10
        else:
            print("Temperature:", temperature, "°F")
            print("Patient is Healthy")

        print()

def show_performance():
    print("----------------------")
    print("Final Performance =", performance)

display_patients()
check_patients()
show_performance()
```

## Output:

<img width="1668" height="823" alt="Screenshot 2026-07-24 105012" src="https://github.com/user-attachments/assets/611789bc-c8b5-4049-8ae7-92437a5329e3" />

## Result

The above algorithem run successful and the cleaning process was running successfully
