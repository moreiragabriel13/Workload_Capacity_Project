# Workforce Workload & Capacity Tracker

This is an Excel-based workforce planning and capacity management tool designed to help, in this case, small teams monitor operational workloads, analyse productivity, and calculate the resources required to manage daily operations.

The tool combines workload tracking, individual task allocation, configurable processing times, and capacity calculations into one integrated solution, supported by an interactive dashboard.

## Dashboard

The workbook includes an interactive dashboard providing a consolidated overview of operational performance and workforce capacity.

Users can select a reporting week and date to explore workload indicators and capacity requirements.

<img width="1046" height="681" alt="image" src="https://github.com/user-attachments/assets/152420af-86de-41f6-b1a8-5d8524ab8d08" />


Key performance indicators include:

- **Incoming Cases:** Total incoming workload for the selected date.
- **Completed Cases:** Total completed workload.
- **Net Backlog Change:** Difference between incoming and completed cases.
- **Completion Rate:** Percentage of incoming cases completed.
- **Average Capacity:** Average capacity required during the selected day / week.
- **Weekly Maximum Capacity:** Highest capacity requirement during the selected week.
- **Capacity Utilization:** Required capacity compared to available team capacity.
- **Available FTEs:** Available full-time equivalent resources.

The dashboard also includes visual charts comparing incoming versus completed volumes and weekly capacity utilisation.

## Key Features

- **Interactive Dashboard:** Centralised overview of workload and capacity KPIs, with selectable reporting periods.
- **Daily Workload Tracking:** Monitor incoming and completed volumes across five different task categories.
- **Individual Workload Allocation:** Track daily task distribution across individual team members.
- **Capacity Planning:** Calculate the workforce capacity required to handle operational volumes.
- **Weekly Capacity Monitoring:** Analyse average and maximum capacity requirements.
- **Configurable Processing Times:** Adjust average handling times for each task category.
- **Performance Monitoring:** Compare incoming and completed volumes to understand changes in operational backlog.

## Workbook Structure

The workbook consists of six interconnected worksheets:

| Worksheet | Description |
|---|---|
| Dashboard | Interactive overview of workload, operational performance and capacity indicators. |
| Volumes | Daily incoming and completed volumes across five task categories. |
| Volume per day per user | Detailed breakdown of daily workload allocated to individual team members. |
| Team capacity | Calculation of processing times and required capacity for each task and working day. |
| Avg Time per task Configuration | Configuration of average processing times for each task category. |
| Rotation Matrix | Defines the weekly rotation of team members across the different tasks. |

## How It Works

The capacity workbook combines three main elements:

1. Daily operational workload volumes.
2. Average processing time per task.
3. Available working time per employee.

### Workload Tracking

Daily incoming and completed volumes are manually recorded across five task categories under the tab `Volumes`. The number of tasks can of course be adjusted as required.

This information is added in the columns called 'In' and 'Out'. These names refer to a task being inside or already outside of the SLA (Service level Agreement). This workbook assumes a SLA of 24h.

### Individual Workload Allocation

The `Volume per day per user` worksheet provides a detailed breakdown of task volumes completed by individual team members. This volume also needs to be manually registered.

This allows the workbook to account for workload distribution and completion across the team. This worksheet is connected to `Volumes` and the registered data appears under the columns called 'Done'. 
This also helps to identify which employee did what task if there is a necessity to track the utilization of resources on an individual level.

<img width="546" height="231" alt="image" src="https://github.com/user-attachments/assets/def14550-a62a-4259-9969-e69d51938ab2" />


### Capacity Calculation

The `Team capacity` worksheet calculates the processing time required for each task category.

The calculation follows two main steps:

**Required Processing Time**

`Task Volume × Average Processing Time`

The `Average processing Time` varies of course from project to project and can be adjusted under the sheet called 'AVG Time per task Configuration':

<img width="353" height="86" alt="image" src="https://github.com/user-attachments/assets/e70281d3-ffe0-4be3-9e82-0e8d1690efe1" />


**Required Capacity (FTE)**

`Required Processing Time / Available Working Time per Employee`

The workbook currently assumes 455 available working minutes per employee per day. Based on 8h of daily subtracting 2 daily breaks of 10 and 15 minutes based on portuguese work law.

The capacity requirements across all five task categories are combined to calculate the total daily workforce capacity required. 
Some conditional formating was also applied to highlight some concerns. For example, whenever the 'Capacity required' column of a task passes 1 or 100%, the cell will turn red. 

<img width="155" height="128" alt="image" src="https://github.com/user-attachments/assets/55da16db-c9b2-4138-9264-44eec831cf4a" />


The same can be observed when consolidating the individual task capacities of a given employee:

<img width="386" height="133" alt="image" src="https://github.com/user-attachments/assets/191c07c7-5cc7-4a19-b2e1-d26a3450e3cf" />


### Dashboard Reporting

The Dashboard brings the underlying information together into a single reporting interface.

Users can select a reporting week and date to review operational performance, workload fluctuations, backlog changes, and capacity requirements.

## Getting Started

1. Download or clone this repository.
2. Open `Workload Capacity Dashboard.xlsx` using Microsoft Excel.
3. Start on the `Dashboard` worksheet to explore the available indicators.
4. Use the week and date selectors to navigate the reporting periods.
5. Update operational volumes in the `Volumes` worksheet.
6. Update individual task completions in the `Volume per day per user` worksheet.
7. Review average processing times in `Avg Time per task Configuration`.
8. Check the calculated workforce requirements in `Team capacity`.
9. Return to the Dashboard to review the updated results.

**Note:** The worksheets are interconnected through Excel formulas. Avoid overwriting formula-driven cells when updating the underlying information.

## workbook Assumptions

The current version of the workbook uses the following assumptions:

- Five operational task categories.
- Four team members.
- 455 available working minutes per employee per day. (8*60-10-15= 455min)
- Configurable average processing times for each task category.
- A predefined four-week team rotation matrix.
- Working days generated using Excel's `WORKDAY` function.

The accuracy of the capacity calculations depends on the quality of the workload inputs and the configured average processing times.

## Tools & Technologies

- Microsoft Excel
- Excel formulas and functions
- Interactive dashboard and data visualisation

## Potential Future Improvements

Possible enhancements for future versions include:

- Monthly workload and capacity reporting as this file only tracks a single month and serves as a simple example
- Historical workload and productivity trend analysis.
- Configurable employee availability and working hours.
- Dynamic team size and task configuration.
- Forecasting future workload and resource requirements.

## Project Purpose

The objective of this project is to provide a practical and accessible workforce planning solution for small operational teams.

By combining workload monitoring and capacity calculations, the tool helps teams better understand their operational demands, anticipate resource requirements, and make more informed workforce planning decisions.

Author: Gabriel Moreira
