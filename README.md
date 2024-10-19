from pybricks.hubs import PrimeHub
from pybricks.parameters import Direction, Port, Stop
from pybricks.pupdevices import Motor
from pybricks.robotics import DriveBase

# Set up all devices.
prime_hub = PrimeHub()
left = Motor(Port.A, Direction.COUNTERCLOCKWISE)
right = Motor(Port.B, Direction.CLOCKWISE)
top = Motor(Port.E, Direction.CLOCKWISE)
front = Motor(Port.F, Direction.CLOCKWISE)
drive_base = DriveBase(left, right, 81, 99)


# The main program starts here.
# pink attachment holder on 3rd black line
drive_base.turn(-10)
drive_base.straight(560, Stop.NONE)
drive_base.settings(straight_speed=100)
drive_base.curve(85, 77)
drive_base.straight(-45)
front.run_angle(500, -800)
drive_base.straight(-30)
drive_base.curve(85, -77)
drive_base.settings(straight_speed=400)
drive_base.straight(-1000)
