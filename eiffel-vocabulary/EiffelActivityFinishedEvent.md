# EiffelActivityFinishedEvent (ActF)
The EiffelActivityFinishedEvent declares that a previously started activity (declared by [EiffelActivityTriggeredEvent](./EiffelActivityTriggeredEvent.md) followed by [EiffelActivityStartedEvent](./EiffelActivityStartedEvent.md)) has finished.

## Data Members
### data.outcome
__Type:__ Object  
__Required:__ Yes  
__Description:__ The outcome of the activity.

#### data.outcome.conclusion
__Type:__ String  
__Required:__ Yes  
__Legal values:__ SUCCESSFUL, UNSUCCESSFUL, FAILED, ABORTED, TIMED_OUT, INCONCLUSIVE  
__Description:__ A terse standardized conclusion of the activity, designed to be machine readable.  
SUCCESSFUL signifies that the activity was concluded and the outcome matched expectations.  
UNSUCCESSFUL signifies that the activity was concluded, but the outcome did not match expectations. To exemplify, a compilation job was successfully invoked, but compilation failed.  
FAILED signifies that the activity could not be successfully executed. To exemplify, a compilation could not be invoked, e.g. due to misconfiguration or environment issues.  
ABORTED signifies that the activity was aborted before it could be concluded.  
TIMED_OUT signifies that the activity did not conclude within the allowed time frame.  
INCONCLUSIVE signifies that the outcome of the activity could not be determined.

#### data.outcome.description
__Type:__ String  
__Required:__ No  
__Description:__ A verbose description of the activity outcome, designed to provide human readers with further information.

### data.persistentLogs
__Type:__ Object[]  
__Required:__ No  
__Description:__ An array of persistent log files generated during execution. 

#### data.persistentLogs.name
__Type:__ String  
__Required:__ Yes  
__Description:__ The name of the log file.

#### data.persistentLogs.uri
__Type:__ String  
__Required:__ Yes  
__Description:__ The URI at which the log can be retrieved.

## Version History
| Version   | Introducing Commit |
| --------- | ------------------ |
| 1.0.0     | _Current version_  |

## Examples
* [Simple example](../examples/events/EiffelActivityFinishedEvent/simple.json)