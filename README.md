# Swarmathon Code Documentation
----------
## <a name="variable"></a>Variables

----------
## Objects
----------
## Structures

----------
## Files
----------

 1. Controller.h - This header serves as a template for every class created. but by itself it does nothing.

	 <b>Public</b>
	  >   Methods
	  > * Controller()
	  > *  virtual void Reset() - Resets internal state to defaults
	  > *  virtual Result DoWork() - Determines what action should be taken based on current internal state and data.
	  > *  virtual bool ShouldInterrupt()
	  > *  virtual bool HasWork()

	  <b>Protected</b>
	  > Methods
	  > * virtual void ProcessData()


 2. DriveController.h - This header houses everything related to the robot's driving. This includes the PID configuration and a state machine.

    <b>Public</b>
    >  Methods
    > * DriveController() - Default Constructor
    > * ~DriveController() - Default Destructor [test](#variable)
    > * void Reset() override
    > * Result DoWork() override
    > * bool ShouldInterrupt() override
