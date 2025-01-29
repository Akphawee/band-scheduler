# 🎸 Band Practice Room Scheduler

This project helps automate scheduling for a band practice room that can only be used by a limited number of members at a time. Instead of manually checking everyone's free time, this program processes the data and finds the best time slots where the most members are available for each song.

## 📌 How It Works
1. **Collect Free Time Data**  
   - Members fill out a **Google Form** indicating their available time slots.  
   - The responses are exported as a CSV file.  

2. **Process the Data**  
   - The script reads the CSV file and finds which time slots have the most available members.  
   - It then suggests the best practice schedule based on the availability of the members playing each song.  

3. **View the Results**  
   - The scheduler can view the processed results and make decisions without manually checking each member's free time.

## 📄 Example CSV Format
The input CSV file should have a structure similar to this:

| Name       | Date 1                  | Date 2                  | Date 3                  | ... |
|------------|-------------------------|-------------------------|-------------------------|-----|
| Member 1   | 9.00-9.30, 9.30-10.00    |                         | 12.00-12.30, 12.30-13.00| ... |
| Member 2   |                         | 12.00-12.30, 12.30-13.00| 12.00-12.30, 12.30-13.00| ... |
| Member 3   | 9.00-9.30, 9.30-10.00    | 12.00-12.30, 12.30-13.00|                         | ... |

In this table:
- The number in each cell represents the time slots (in 30-minute intervals) that each member is available.
- Empty cells indicate when a member is unavailable.

An example CSV file (`example_freetime.csv`) is included in this repository.

## Input Format
The script processes free time data from a CSV file. The form collects:
- Member names
- Time slots (marked as available/unavailable)
  
Example Google Form:
![Form Example(nickname)](https://github.com/Akphawee/band-scheduler/blob/main/ggform_nickname.png)
![Form Example](https://github.com/Akphawee/band-scheduler/blob/main/ggform_freetime_selection.png)


## 🛠️ Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/Akphawee/band-scheduler.git
