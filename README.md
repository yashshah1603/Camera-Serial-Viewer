# Camera-Serial-Viewer
This project includes python project for Camera Image Detection
```markdown

This project provides a graphical user interface (GUI) to interact with a camera (using the Toupcam SDK) and serial data communication. The application allows users to configure camera settings, view live video feed, adjust exposure, white balance, and capture images. It also reads and displays data from a serial port.

## Features

- **Camera Interaction**: 
  - Open/close camera
  - Set resolution
  - Control exposure time and gain (both manual and automatic)
  - Adjust white balance (temperature and tint)
  - Capture still images
  - Display live video feed with frame rate info

- **Serial Data Reading**: 
  - Connect to a serial port
  - Display X, Y, Z data from serial communication (for example, from an accelerometer or another sensor)

## Requirements

- Python 3.x
- PyQt5
- toupcam SDK (for interacting with the Toupcam camera)
- PySerial (for reading from serial ports)

## Installation

### 1. Clone the repository:

```bash
git clone https://github.com/yashshah1603/Camera-Serial-Viewer.git
cd Camera-Serial-Viewer
```

### 2. Install required dependencies:

```bash
pip install -r requirements.txt
```

> Note: You will need the Toupcam SDK for your camera, and it must be installed and configured correctly for this project to work. 

### 3. Set up Serial Communication:

- Make sure your serial device (e.g., an accelerometer or sensor) is connected to a valid serial port on your system (e.g., `/dev/ttyUSB0` on Linux or `COM3` on Windows).

## Usage

### Run the application:

```bash
python main.py
```

### Camera Interaction:

- The main window displays the live video feed and allows you to adjust camera settings like exposure time, gain, and white balance.
- You can take a snapshot by clicking the "Snap" button.
- The "Open" button allows you to open/close the camera.

### Serial Data Interaction:

- Serial data (X, Y, Z) will be displayed in the "Serial Data" group box.
- The serial port connection is managed through the GUI, and you can connect/disconnect the serial port easily.

### Sample Output:

After opening the serial port and camera, you will see the following:

- The video feed from the camera.
- Real-time frame rate displayed at the bottom of the video feed.
- Serial data (X, Y, Z) from the sensor will be shown in the "Serial Data" section.

## Configuration

### Serial Port Configuration:
- The serial port can be opened with a specified port name. For example, to connect to `/dev/ttyUSB0`, use:

```python
mw.openSerialPort('/dev/ttyUSB0')
```

### Camera Configuration:
- The camera resolution and other parameters can be adjusted via the GUI.
- Make sure the Toupcam SDK is correctly installed and the camera is properly connected.

## Troubleshooting

- **Serial Port Connection Error**: 
  - Ensure that the correct port is selected and the serial device is properly connected.
  - Check the serial port settings such as baud rate (115200 in the current configuration).

- **Camera Not Detected**:
  - Ensure the camera is connected to the system and recognized by the Toupcam SDK.
  - If using a USB camera, try reconnecting it and restarting the application.


---

Feel free to modify the code or adapt it to suit your needs. Contributions are welcome!

```
