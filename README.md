# AI Gatekeeper

A simple python program that monitors an IPC stream for known faces and controls a wicket gate. It does realtime object detection with Google Coral through rest API achieving >20 FPS. Having detected person or car arriving, it zooms in the IPC and does face recognition with Deepstact with ~4 FPS. When a known face is recognized with confidence of 80% or higher, the program opens wicket gate (Dahua VTO2000). It also communicates with Home Assistant with MQTT. 

## Object detection
20+ FPS (max IPC frame rate) is achieved on 8GB RPi4 with Google Coral USB accelerator accessible through https://github.com/sickidolderivative/tensorflow-lite-rest-server. 

## Face recognition
4 FPS is achieved on Deepstack running on 4GB Jetson nano: https://forum.deepstack.cc/t/deepstack-release-on-jetson/ 


The program is specific to my home setup, but perhaps someone finds parts of it useful. 
