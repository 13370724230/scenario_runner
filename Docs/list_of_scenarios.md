# List of Supported Scenarios

Welcome to the ScenarioRunner for CARLA! This document provides a list of all currently supported scenarios, and a short description for each one.

ScenarioRunner has several scenarios already implemented which have been taken from the NHTSA pre-crash typology. These are:

Control Loss:    The blue vehicle enters a slippery surface, modifying its control, and has to adjust to avoid crashing.
Lane Change: The blue vehicle has to detect that the in front is moving very slow and either move to a side lane or overtake it invading the opposite lane
Obstacle Detection: The ego vehicle has to brake due to an entity crossing the road in front of it. This is also done but with a vehicle in front, blocking its view
Handling intersection: The ego vehicle is about to arrive at an intersection and has to decide how to procede next. Four different scenarios can appear here, apart from the normal one (where the traffic light is green)
    · A vehicle runs a red light from any direction
    · The ego vehicle has to go left but the opposite lane is busy with vehicles
        · The ego vehicle want to go right but its traffic light is red (this is an unreal situation for Europe but it is allowed at USA)
        · Unsignalized junctions

> Pics? 

### FollowLeadingVehicle
The scenario realizes a common driving behavior, in which the user-controlled ego vehicle follows a leading car driving down a given road in Town01. At some
point the leading car slows down and finally stops. The ego vehicle has to react accordingly to avoid a collision. The scenario ends either via a timeout, or if
the ego vehicle stopped close enough to the leading vehicle. 

### FollowLeadingVehicleWithObstacle
This scenario is very similar to 'FollowLeadingVehicle'. The only difference is, that in front of the leading vehicle is a (hidden) obstacle that blocks the way.

### VehicleTurningRight
In this scenario the ego vehicle takes a right turn from an intersection where a cyclist suddenly drives into the way of the ego vehicle,which has to stop
accordingly. After some time, the cyclist clears the road, such that ego vehicle can continue driving.

### VehicleTurningLeft
This scenario is similar to 'VehicleTurningRight'. The difference is that the ego vehicle takes a left turn from an intersection.

### OppositeVehicleRunningRedLight
In this scenario an illegal behavior at an intersection is tested. An other vehicle waits at an intersection, but illegally runs a red traffic light. The
approaching ego vehicle has to handle this situation correctly, i.e. despite of a green traffic light, it has to stop and wait until the intersection is clear
again. Afterwards, it should continue driving.

### StationaryObjectCrossing
In this scenario a cyclist is stationary waiting in the middle of the road and blocking the way for the ego vehicle. Hence, the ego vehicle has to stop in
front of the cyclist.

### DynamicObjectCrossing
This is similar to 'StationaryObjectCrossing', but with the difference that the cyclist is dynamic. It suddenly drives into the way of the ego vehicle, which
has to stop accordingly. After some time, the cyclist will clear the road, such that the ego vehicle can continue driving.

### NoSignalJunctionCrossing 
This scenario tests negotiation between two vehicles crossing cross each other through a junction without signal. The ego vehicle is passing through a junction without traffic lights And encounters another vehicle passing across the junction. The ego vehicle has to avoid collision and navigate across the junction to succeed.

### ControlLoss
In this scenario control loss of a vehicle is tested due to bad road conditions, etc and it checks whether the vehicle is regained its control and corrected its course.

### ManeuverOppositeDirection
In this scenario vehicle is passing another vehicle in a rural area, in daylight, under clear weather conditions, at a non-junction and encroaches into another
vehicle traveling in the opposite direction.

### OtherLeadingVehicle
The scenario realizes a common driving behavior, in which the user-controlled ego vehicle follows a leading car driving down a given road.
At some point the leading car has to decelerate. The ego vehicle has to react accordingly by changing lane to avoid a collision and follow the leading car in
other lane. The scenario ends via timeout, or if the ego vehicle drives certain distance. 

### SignalizedJunctionRightTurn
In this scenario right turn of hero actor without collision at signalized intersection is tested. Hero Vehicle is turning right in an urban area, at a signalized intersection and
turns into the same direction of another vehicle crossing straight initially from a lateral direction.

### SignalizedJunctionLeftTurn
In this scenario hero vehicle is turning left in an urban area, at a signalized intersection and cuts across the path of another vehicle coming straight crossing from an opposite direction.
