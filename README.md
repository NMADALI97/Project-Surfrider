# Project-Surfrider

Instructions and code for the course project - based on ONG Surfrider detection of plastics in rivers.

![Surfrider logo](surfrider.png?raw=true "Surfrider")

## Surfrider - Plastic Monitoring on Rivers

This course project makes use of an ongoing open source project led by [Surfrider Europe](https://surfrider.eu/), which aims at quantifying plastic pollution in rivers through space and time.
Plastic Waste in oceans mostly comes from rivers (80%), and it is very difficult to assess precisely where they come from.
This will be used to monitor river banks to take local decisions, measure effectiveness of policies at local and global scales, and has thus a very concrete importance.

In practice, video streams are captured on river banks from kayaks (with their geolocalisation), and then fed to a model which aims at quantifying the number and types of objects.
In the first version, there are three types (classes) of plastic litter:
- Plastic Bottles: ![Plastic Bottles](bottle.png?raw=true "Plastic Bottles")
- Plastic Fragments: ![Plastic Framents](fragment.png?raw=true "Plastic Fragments")
- Other types of waste

Your goal is to build a short project around plastic detection using modern Deep Learning algorithms.

