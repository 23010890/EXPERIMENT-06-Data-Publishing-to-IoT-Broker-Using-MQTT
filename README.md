# EXPERIMENT-05-Data-Publishing-to-IoT-Broker-Using-MQTT3
 ## NAME: DHARSHINI S
 ## REGISTER NUMBER: 212223110010
 ## DEPARTMENT: CSE(IOT)
 ## YEAR: III
 ## DATE: 27-02-2026
 ## Aim:
To publish data to an IoT broker using the MQTT protocol.

 ## Apparatus Required:
MQTT Broker: An MQTT broker, such as HiveMQ or Mosquitto, for handling communication.
Python Environment: To run the script for publishing data to the broker.
Internet Connection: For connecting to the IoT broker.
Theory:
MQTT (Message Queuing Telemetry Transport) is a lightweight messaging protocol used in IoT applications. It allows devices to publish data to a broker, where other devices or applications can subscribe to receive updates. This experiment demonstrates how to use MQTT to send messages to an IoT broker using the paho-mqtt library in Python.

 ## Procedure:
Setup MQTT Broker:

You can use a public broker like broker.hivemq.com or set up your own broker using software like Mosquitto.
Choose a topic for the message, e.g., test/topic.
Install MQTT Client Library:

Install the paho-mqtt Python library to facilitate communication with the MQTT broker.
bash
Copy code
!pip install paho-mqtt
Write the Python Script to Publish Data:

Create a Python script to connect to the broker and publish a message to a specific topic.
Code Implementation: Here’s the Python code to publish data to the IoT broker using MQTT:

python
Copy code
import paho.mqtt.client as mqtt

# Broker details
broker_address = "broker.hivemq.com"  # Broker address
broker_port = 1883  # Broker port
topic = "test/topic"  # Topic to publish to

# Initialize the MQTT Client
client = mqtt.Client()

# Connect to the broker
client.connect(broker_address, broker_port, keepalive=60)

# Publish a message to the topic
message = "Hello, MQTT!"  # Message to be published
client.publish(topic, message)

# Disconnect from the broker
client.disconnect()

# Print confirmation message
print(f"Message '{message}' published to topic '{topic}'")
Run the Script:

Execute the script. It will connect to the MQTT broker, publish the message to the specified topic, and then disconnect.
Verify Message Publishing:

You can verify the message by subscribing to the same topic using an MQTT client, such as MQTT.fx or any other MQTT subscriber tool.
 ## Outputs:
Message Confirmation: The script will print a message confirming that the data has been successfully published to the topic.

Example output:

bash
Copy code
Message 'Hello, MQTT!' published to topic 'test/topic'
Broker Message: The message "Hello, MQTT!" will be published to the topic test/topic.

## Python Code 


  




 ## Simulation Screenshots:
(Add screenshots of the MQTT client showing the message subscription and the message published on the broker.)

 ## Results:
The data was successfully published to the MQTT broker. The experiment demonstrated how to use the MQTT protocol to transfer data to an IoT broker, enabling remote communication between devices or applications. The message was confirmed to be received by the topic, and this communication can be extended to more complex IoT systems.
