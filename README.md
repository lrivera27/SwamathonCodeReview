# Swarmathon Code Documentation
----------
## <a id="variable"></a>Variables

----------
## Objects
----------
## Structures
----------
1. <a id="result"><b><u>Result</u></b></a> - This structure serves as a return for a controller, usually returned by the "DoWork" method.






## Files
----------

1. <b><u>Controller.h</u></b> - This header serves as a template for every class created. but by itself it does nothing.

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
    > * [Result](#resultClass) DoWork() override
    > * bool ShouldInterrupt() override
