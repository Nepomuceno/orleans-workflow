# Orleans Workflow
On this project you will find a sampel of how to create a workflow engine using the orleans workflow. 


## Dependencies
This project assumes that you are going to be runing Orleans to run your workflow and that you will be hostiing it on Azure. It can run the workflow trough diferent methods but  use external azure resources in order to get into production.

- Visual Studio 2017
- .Net Framework 4.6.2
- Servcie Fabric

## Project Structure
    -/
    -/src
        Project source and solution file
    -/docs
        How to use the project and the contents insite

## Usage

### Workflow format
The workflow it is expected to be stored in `Json` so you would need this workflow storage that would be providing this workflow information and will query to get this values. 

```json
{
    "name": "workflow-name",
    "id": "unique-id",
    "nodes": [
        {
            "id": "unique-id",
            "fields": [
                {"id": "unique-id"}
            ],
            "type": "task-type",
            "events": [
                {"name": "eventName", "action": "action-id"}
            ]
        }
    ],
    "actions": [
        {
            "id": "unique-id",
            "type": "action-type"
        }
    ]
}
```
