Assumption: Platoon will follow Leading Truck. Leading Truck will be the same through out the platooning. We are not considering switching of Leading Truck to Follower or vise versa to make things simple. Any Failure in Leading truck will result in stop platooning. (However Failure in following truck or loss of communication to the leader truck will be handled appropriately without effecting the overall system)

Each Vehicle Should broadcast information about its
-Speed
-direction
-location
-braking and turning intent

Protocol of Joining Platoon:
States:

- Idle (free vehicle)
  -Waiting for Response (Transition sends join request)
  -Move to Tail of Platoon (request accepted, otherwise back to Idle)
  -Attach and Start Following
- Idle (Follower)
  Protocol of Platoon Leader:
- Idle (leader)
  -Decide over Request (Receives join request)
  -Wait join Complete (sends acknowedgment and waits for confirmation)
  -Update Platoon
  -Idle leader

Protocol While Platooning:

States:
Leader Truck:
Idle(Leading Truck is moving normally with platoon following)
Braking(Leading Truck is braking, while communicating it to the followers)

Turning lanes(Leading Truck is turning, while communicating it to the followers)

Emergency Stop(Leading Truck has broadcasted emergency stop, could be due to loss of a truck or any other failure in the system)

Safety Stop ( Leading Truck is going to safe stop and exit Platooning)

States

Follower Truck

- Idle ( Nomally following Truck, with ACC and following speed limits and direction by the leader)

- Braking (Receives Brake signals)

- Turning (Receives Turning Signals)

- Emergency Stop (Receives Emergency stop)

- Lost Communication (ACC, Radar, GPS for following) ( next state Idle, if Communication re-estibalished, Safety Stop if Communication Loss for a longer period (above a threshold time))

- Safety Stop
