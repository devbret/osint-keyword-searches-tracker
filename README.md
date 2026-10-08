# OSINT Keyword Searches Tracker

![A screenshot from the main application UI, with search terms blocked from view.](https://hosting.photobucket.com/bbcfb0d4-be20-44a0-94dc-65bff8947cf2/df5e6e15-1efb-4b33-8d94-c0ab70d67b54.jpg)

Centralize keyword management, enable one-click platform searches, track user activity and visualize search behavior through the analytics dashboards.

## Application Overview

This application stores a list of search keywords in a JSON file, lets the user add or delete keywords and displays each keyword with quick links to search for it across platforms like Google, YouTube, Reddit and Bluesky. Every time a keyword list is loaded, updated, deleted or clicked, the Flask server logs the activity to a CSV file and updates click counts for the selected keyword.

On the frontend, the app provides a (1) live search bar for filtering keywords, (2) custom multi-keyword search popup for building combined searches and (3) stats modal which visualizes usage patterns with D3 charts, including daily activity trends, platform activity, top searches and an hourly activity heatmap.

## Basic Setup Instructions

Below are the prerequisite programs and setup steps for operating this software on a Linux machine.

### Programs Needed

- [Git](https://git-scm.com/downloads)

- [Python](https://www.python.org/downloads/)

### Steps

1. Install the above programs

2. Open a terminal

3. Clone this repository: `git clone git@github.com:devbret/osint-keyword-searches-tracker.git`

4. Navigate to the repo's directory: `cd osint-keyword-searches-tracker`

5. Create a virtual environment: `python3 -m venv venv`

6. Activate your virtual environment: `source venv/bin/activate`

7. Install the needed dependencies: `pip install -r requirements.txt`

8. Run the primary script: `python3 app.py`

9. Access the frontend in a browser: `http://localhost:5501`

10. When finished, stop the server: `CTRL + C`

11. Exit the virtual environment: `deactivate`

## Analytics Dashboard

This application includes usage analytics which can be accessed through the `Stats` button located at the upper-right corner of the primary interface. The analytics dashboard reads from the application’s activity log and presents several data visualizations, including:

- `Number Of Actions Daily` - Overall day-by-day interaction volume

- `Activity By Platform` - How often users are launching searches on platforms such as Google, YouTube, Reddit and Bluesky

- `Top Searches` - Surfaces the most frequently used keywords and shows how their activity is distributed across platforms

- `Hourly Activity` - Heatmap for exploring usage patterns by hour of day and day of week

Together, these charts make it easy to understand engagement trends, identify the most active search behavior and spot when and where the application is being used most often.

## Other Considerations

Below you will find information not covered in the installation and use sections above. Including the abilities this repo is intended to demonstrate. As well as an overview of the license this code is made available with. And a way to contact the maintainer with questions, suggestions and collaboration opportunities.

### Abilities Demonstrated

This project repo is intended to demonstrate an ability to do the following:

- Provide a centralized dashboard to manage, track and organize search keywords across multiple platforms

- Use D3.js visualizations to transform activity logs into insights through heatmaps, bar charts and calendars

- Allow users to create custom combined search queries and monitor engagement metrics in a single interface

- Track keyword performance and visualize user behavior patterns over time across various digital platforms

### License Information

This repository is distributed under the MIT License. You are free to use, copy, modify, merge, publish, distribute, sublicense and sell copies of this software, including as part of proprietary or commercial work. The single condition is the copyright and permission notices contained in the LICENSE file must be included with any copy or substantial portion of the software that you redistribute. The software is provided "as is", without warranty of any kind, and the copyright holder is not liable for any claim or damages arising from its use.

If you have any questions or would like to collaborate, please reach out either on GitHub or via [my website](https://bretbernhoft.com/).
