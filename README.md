# MS-Workset Dataset
## Introduction
MS-Workset is an open-source dataset that primarily focuses on participatory mobile crowdsensing (MCS), in which users are
actively involved in the sensing process by accepting or declining task requests, and workers may exhibit various
forms of misbehavior.
In this proposed dataset, three main representative misbehavior scenarios are modeled:
+ Multi-account behavior,
+ Low-quality data submission,
+ Location data manipulation (GPS Spoofing).
## Dataset Overview
### Faking_GPS Folder:
+ All-rows.csv: represents the raw dataset that contains coordinates of legitimate and malicious workers. It contains: account ID (a unique account associated with a unique worker), Task ID, and Worker coordinates (lat, lon).
+ accepted-rows.csv: represents the list of legitimate workers with correct coordinates
+ blacklist.csv: represents the blacklisted workers, by ID, with fake coordinates
+ deleted-rows.csv: represents the list of deleted workers with fake coordinates
### Low-Quality Workers Folder:

The Low-Quality Workers Folder contains 4 files described as follows:

+ All-rows.csv: represents the raw dataset that contains legitimate and malicious workers
+ accepted-rows.csv: represents the list of legitimate workers with high-quality contributions
+ blacklist.csv: represents the blacklisted workers, by ID, with limited contributions
+ deleted-rows.csv: represents the list of deleted workers with limited contributions

#### Attribute Description

| Attribute           | Data Type | Description                                                                                                                                                      |
| ------------------- | --------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Account ID`        |   Integer | Represents the account identifier associated with the worker's platform account.                                                                                     |
| `Task ID`           |   Integer | A unique identifier for the crowdsensing task assigned to the worker.                                                                                            |
| `Subtasks`          |   Numeric | The total number of subtasks associated with the assigned task.                                                                                                  |
| `Finished Subtasks` |   Numeric | The number of subtasks successfully completed by the worker.                                                                                                     |
| `Quality`           |     Float | A numerical score representing the assessed quality of the worker’s contribution.|
| `Rating`            |     Float | The rating assigned to the workers based on their contribution.                             |
| `Latitude`          |     Float | The latitude associated with the worker’s contribution.                                                                                     |
| `Longitude`         |     Float | The longitude associated with the worker’s contribution.                                                                                    |


### Workers_With-Multi-accounts Folder:
+ All-reports.csv: represents the raw dataset that contains workers IDs and their associated accounts. The dataset is labeled where the malicious accounts are labeled as "True" and the legitimate ones as "False".
+ blacklist.csv: represents the blacklisted accounts.
+ All-reports-500-500.csv: Small sample of the raw dataset with 500 workers. Could be used for a small simulation.
+ blacklist-500-500.csv: blacklisted accounts from the sample dataset

#### Attribute Description

| Attribute | Data Type | Description |
|---|---|---|
| `Worker ID` | Integer | Represents the worker identifier. |
| `Account ID` | Integer | Represents the account identifier associated with the worker's platform account. A worker can possess multiple accounts. |
| `Task ID` | Integer | A unique identifier for the crowdsensing task in which the worker participated. |
| `Variance` | Float | Variance of the reported data submitted by the worker account for the executed task. |
| `Rating` | Float | A numerical score representing the worker's assessed reliability. |
| `Latitude` | Float | The latitude associated with the worker's location. |
| `Longitude` | Float | The longitude associated with the worker's location. |
| `Malicious` | Boolean | The target label indicating whether the account was classified as malicious. `True` denotes a malicious account, while `False` denotes a non-malicious account. |
