# Swarmathon Code Documentation
## <a id="variable"></a>Variables
## Objects
## Enumerators
1. <a id="resultType"><b>ResultType</b></a> - This enumerator is used to identify
2. <a id="behaviorTrigger"><b>BehaviorTrigger</b></a> - This enumerator is used to identify
## Structures
1. <a id="result"><b>Result</b></a> - This structure serves as a return for a controller, usually returned by the "DoWork" method.

    >   Enumerators
    > * [ResultType](#resultType) type
    > * [BehaviorTrigger](#resultType) b

    >   Structures
    > * Waypoints wpts
    > * PrecisionDriving pd
    > * PIDType PIDMode

    >   Variables
    > * float fingerAngle = -1 (Default)
    > * float wristAngle = -1 (Default)
    > * bool reset



## Files

1. <b>Controller.h</b> - This header serves as a template for every class created. but by itself it does nothing.

	  <b>Public</b>
	  >   Methods
	  > * Controller()
	  > *  virtual void Reset() - Resets internal state to defaults
	  > *  virtual [Result](#result) DoWork() - Determines what action should be taken based on current internal state and data
	  > *  virtual bool ShouldInterrupt()
	  > *  virtual bool HasWork()

	  <b>Protected</b>
	  > Methods
	  > * virtual void ProcessData()


2. DriveController.h - This header houses everything related to the robot's driving. This includes the PID configuration and a state machine.

    <b>Public</b>
    >  Methods
    > * DriveController() - Default Constructor
    > * ~DriveController() - Default Destructor
    > * void Reset() override
    > * [Result](#result) DoWork() override
    > * bool ShouldInterrupt() override
