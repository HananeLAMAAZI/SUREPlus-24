The Low Quality Workers Folder contains 3 files described as follows:

All-Workers.csv: represents the raw dataset that contains legitimate and malicious workers

Legitimate-Workers.csv: represents the list of legitimate workers with high-quality contributions

Low-Quality-Workers.csv: represents the list of low-quality workers with limited contributions


| Attribute           | Data Type | Description                                                                                                                                                      |
| ------------------- | --------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Account ID`        |   Integer | An anonymized identifier assigned to the crowdsensing worker or participant.                                                                                     |
| `Task ID`           |   Integer | A unique identifier for the crowdsensing task assigned to the worker.                                                                                            |
| `Subtasks`          |   Numeric | The total number of subtasks associated with the assigned task.                                                                                                  |
| `Finished Subtasks` |   Numeric | The number of subtasks successfully completed by the worker.                                                                                                     |
| `Quality`           |     Float | A numerical score representing the assessed quality of the worker’s contribution.|
| `Rating`            |     Float | The rating assigned to the workers based on their contribution.                             |
| `Latitude`          |     Float | The latitude associated with the worker’s contribution.                                                                                     |
| `Longitude`         |     Float | The longitude associated with the worker’s contribution.                                                                                    |

