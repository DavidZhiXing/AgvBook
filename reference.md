.
├── cereal              # The messaging spec and libs used for all logs
├── common              # Library like functionality we've developed here
├── docs                # Documentation
├── opendbc             # Files showing how to interpret data from cars
├── panda               # Code used to communicate on CAN
├── third_party         # External libraries
├── pyextra             # Extra python packages
└── selfdrive           # Code needed to drive the car
    ├── assets          # Fonts, images, and sounds for UI
    ├── athena          # Allows communication with the app
    ├── boardd          # Daemon to talk to the board
    ├── camerad         # Driver to capture images from the camera sensors
    ├── car             # Car specific code to read states and control actuators
    ├── common          # Shared C/C++ code for the daemons
    ├── controls        # Planning and controls
    ├── debug           # Tools to help you debug and do car ports
    ├── locationd       # Precise localization and vehicle parameter estimation
    ├── logcatd         # Android logcat as a service
    ├── loggerd         # Logger and uploader of car data
    ├── modeld          # Driving and monitoring model runners
    ├── proclogd        # Logs information from proc
    ├── sensord         # IMU interface code
    ├── test            # Unit tests, system tests, and a car simulator
    └── ui              # The UI