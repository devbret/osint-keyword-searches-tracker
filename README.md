# OSINT Keyword Searches Tracker

![A screenshot from the main application UI, with search terms blocked from view.](https://hosting.photobucket.com/bbcfb0d4-be20-44a0-94dc-65bff8947cf2/e72bbd40-7c45-4172-b046-d0bec18646d7.jpg)

Centralizes keyword management, enables one-click platform searches, tracks user activity and visualizes search behavior through analytics dashboards.

## Overview

This application stores a list of search keywords in a JSON file, lets the user add or delete keywords and displays each keyword with quick links to search for it across platforms like Google, YouTube, Reddit and Bluesky. Every time a keyword list is loaded, updated, deleted or clicked, the Flask server logs the activity to a CSV file and updates click counts for the selected keyword.

On the frontend, the app provides a (1) live search bar for filtering keywords, (2) custom multi-keyword search popup for building combined searches and (3) stats modal which visualizes usage patterns with D3 charts, including daily activity trends, platform activity, top searches and an hourly activity heatmap.

## Set Up

Below are the prerequisite programs and setup steps for operating this software on a Linux machine.

### Programs Needed

- [Git](https://git-scm.com/downloads)

- [Python](https://www.python.org/downloads/)

### Steps

1. Install the above programs

2. Open a terminal

3. Clone this repository using `git` by running the following command: `git clone git@github.com:devbret/osint-keyword-searches-tracker.git`

4. Navigate to the repo's directory: `cd osint-keyword-searches-tracker`

5. Create a virtual environment: `python3 -m venv venv`

6. Activate your virtual environment: `source venv/bin/activate`

7. Install the needed dependencies for running the script: `pip install -r requirements.txt`

8. Run the primary script: `python3 app.py`

9. Launch an HTTP server in a new terminal: `python3 -m http.server`

10. To view the frontend GUI, press your `CTRL` key and click the URL link displayed in the terminal

11. Once the main interface has been opened, organize your OSINT keywords searches by clicking on the `Add` button

12. Click on any of the links to visit the relevant platform for a specific timeframe and keyword

13. Exit the virtual environment when finished: `deactivate`

## Analytics

![Screenshot of the first two data visualizations.](https://hosting.photobucket.com/bbcfb0d4-be20-44a0-94dc-65bff8947cf2/e9d5ba13-8b09-4d48-b606-17b6e6bf518c.jpg)

This application also includes usage analytics which can be accessed through the `Stats` button in the upper-right corner of the interface. The analytics view reads from the application’s activity log and presents several data visualizations, including:

- `Number Of Actions Daily` - Overall day-by-day interaction volume

- `Activity By Platform` - How often users are launching searches on platforms such as Google, YouTube, Reddit and Bluesky

- `Top Searches` - Surfaces the most frequently used keywords and shows how their activity is distributed across platforms

- `Hourly Activity` - Heatmap for exploring usage patterns by hour of day and day of week

Together, these charts make it easy to understand engagement trends, identify the most active search behavior and spot when and where the application is being used most often.

## Other Considerations

This project repo is intended to demonstrate an ability to do the following:

- Centralize management of searchable keywords with persistent storage and real-time updates

- Log all user interactions, including searches, additions, deletions and click activity

- Provide cross-platform search launching with one-click access and tracking

- Visualize user behavior and engagement trends via an analytics dashboards

If you have any questions or would like to collaborate, please reach out either on GitHub or via [my website](https://bretbernhoft.com/).
