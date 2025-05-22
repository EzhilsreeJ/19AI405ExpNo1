<h1>ExpNo 1 : Developing AI Agent with PEAS Description</h1>
<h3>Name: EZHIL SREE J</h3>
<h3>Register Number: 212223230056</h3>


<h3>AIM:</h3>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>


<h3>Theory</h3>

<h3>Room-Cleaning Agent:</h3>
<p>
An <strong>AI agent</strong> is a system capable of autonomous actions in an environment to achieve a goal. It senses through <strong>sensors</strong> and acts through <strong>actuators</strong>.
The agent's behavior can be modeled using the <strong>PEAS</strong> framework:
</p>

<ul>
  <li><strong>P</strong> – Performance Measure</li>
  <li><strong>E</strong> – Environment</li>
  <li><strong>A</strong> – Actuators</li>
  <li><strong>S</strong> – Sensors</li>
</ul>

<p>
In this experiment, we simulate a <strong>room-cleaning agent</strong> (like a vacuum cleaner), operating in <strong>two rooms (A and B)</strong>. The agent must:
</p>

<ul>
  <li>Check for dirt in the current room.</li>
  <li>Clean if dirty.</li>
  <li>Move to the next room if needed.</li>
</ul>

<p>
Each <strong>cleaning</strong> action improves the performance, while each <strong>movement</strong> reduces it.
</p>

---

<h3>PEAS DESCRIPTION:</h3>

<table>
  <tr>
    <th>Agent Type</th>
    <th>Performance Measure</th>
    <th>Environment</th>
    <th>Actuators</th>
    <th>Sensors</th>
  </tr>
  <tr>
    <td>Room-Cleaning Agent</td>
    <td>Cleanliness, Fewer moves</td>
    <td>Rooms A and B</td>
    <td>Move Left/Right, Clean</td>
    <td>Location Sensor, Dirt Sensor</td>
  </tr>
</table>


<h3>DESIGN STEPS</h3>

<h4>STEP 1: Identifying the input:</h4>
<p>Location of the agent, Dirt status of the rooms</p>

<h4>STEP 2: Identifying the output:</h4>
<p>Actions: Move, Clean, Do nothing</p>

<h4>STEP 3: Developing the PEAS description:</h4>
<p>PEAS description is defined by performance, environment, actuators, and sensors in the AI agent model.</p>

<h4>STEP 4: Implementing the AI agent:</h4>
<p>Simulate the agent behavior to clean dirty rooms and move as required.</p>

<h4>STEP 5: Measure the performance:</h4>
<p>Increment for cleaning action, decrement for each movement.</p>


<h3>PROGRAM:</h3>

```python
# Developing AI Agent with PEAS Description
# Developed by: EZHIL SREE J
# Register Number: 212223230056

class VacuumCleanerAgent:
    def __init__(self):
        # Initialize the agent's state (location and dirt status)
        self.location = "A"  # Initial location (can be "A" or "B")
        self.dirt_status = {"A": False, "B": False}  # Initial dirt status (False means no dirt)

    def move_left(self):
        # Move the agent to the left if possible
        if self.location == "B":
            self.location = "A"

    def move_right(self):
        # Move the agent to the right if possible
        if self.location == "A":
            self.location = "B"

    def suck_dirt(self):
        # Suck dirt in the current location if there is dirt
        if self.dirt_status[self.location]:
            self.dirt_status[self.location] = False
            print(f"Sucked dirt in location {self.location}")

    def do_nothing(self):
        # Do nothing
        pass

    def perform_action(self, action):
        # Perform the specified action
        if action == "left":
            self.move_left()
        elif action == "right":
            self.move_right()
        elif action == "suck":
            self.suck_dirt()
        elif action == "nothing":
            self.do_nothing()
        else:
            print("Invalid action")

    def print_status(self):
        # Print the current status of the agent
        print(f"Location: {self.location}, Dirt Status: {self.dirt_status}")

# Example usage:
agent = VacuumCleanerAgent()

# Move the agent, suck dirt, and do nothing
agent.perform_action("left")
agent.print_status()
agent.perform_action("suck")
agent.print_status()
agent.perform_action("nothing")
agent.print_status()
```
## OUTPUT:
![Screenshot 2025-05-19 205304](https://github.com/user-attachments/assets/49506727-fdbe-4ef2-8b45-b20b91bf4293)

## RESULT:
Thus the Developing AI Agent with PEAS Description was implemented using python programming.
