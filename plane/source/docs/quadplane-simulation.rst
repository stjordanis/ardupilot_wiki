.. _quadplane-simulation:

QuadPlane Simulation
====================

A simple QuadPlane model is available in SITL, allowing you to test the
features of the QuadPlane code without risking a real aircraft.

You can start it like this, from any vehicle's subdirectory:

::

    sim_vehicle.py -j4 -f quadplane --console --map
    
 or add the vehicle type:

    sim_vehicle.py -j4 -v Plane -f quadplane --console --map
    
    
If you have simulated other vehicles in the current directory, you may wish
to add the - w option to the command line to reset the parameters back to
QuadPlane defaults (normal Separate Lift Thrust (SLT) Quadplane in quad configuration).

To visualise the aircraft you can use FlightGear in view-only mode. The
simulation will output FlightGear compatible state on UDP port 5503.
Start FlightGear using the **fg_plane_view.sh** scripts provided in
the **Tools/autotest** directory.

Note that to get good scenery for FlightGear it is best to use a major
airport. I tend to test at San Francisco airport, like this:

::

    sim_vehicle.py -L KSFO -f quadplane --console --map

Using the joystick module with a USB adapter for your transmitter gives
a convenient way to get used to the QuadPlane controls before flying.

If flying at KSFO there is a sample mission available with VTOL takeoff
and landing:

::

    wp load ../Tools/autotest/Generic-Missions/KSFO-VTOL.txt

As usual you can edit the mission using "module load misseditor"
