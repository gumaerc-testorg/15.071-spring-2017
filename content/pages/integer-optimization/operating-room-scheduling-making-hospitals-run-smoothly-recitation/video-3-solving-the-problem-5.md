---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '9.4 Operating Room Scheduling: Making Hospitals Run Smoothly  (Recitation)'
parent_type: CourseSection
parent_uid: 1ebaa9f0-a112-c161-92d9-1227cd28b727
title: '9.4 Operating Room Scheduling: Making Hospitals Run Smoothly  (Recitation)'
uid: 162e5921-904a-9507-80e7-596c005168c3
---

*   {{< resource_link 8a92070b-71b9-513e-35b1-c9854c1ef91c "\<Video 2: An Optimization Model" >}}
*   {{< resource_link 1ebaa9f0-a112-c161-92d9-1227cd28b727 "9.4.1Welcome to Recitation 9" >}}
*   {{< resource_link 5e9398f5-808e-614e-c06f-e6634bc50d7e "9.4.2Video 1: The Problem" >}}
*   {{< resource_link 8a92070b-71b9-513e-35b1-c9854c1ef91c "9.4.3Video 2: An Optimization Model" >}}
*   {{< resource_link 162e5921-904a-9507-80e7-596c005168c3 "9.4.4Video 3: Solving the Problem" >}}
*   {{< resource_link 6e8bdbce-3ea9-e644-0e2b-66d90a657d47 "9.4.5Video 4: The Solution" >}}
*   {{< resource_link 6e8bdbce-3ea9-e644-0e2b-66d90a657d47 "\>Video 4: The Solution" >}}

Video 3: Solving the Problem
----------------------------

In this video, we'll be using the spreadsheet Recitation\_ORscheduling. If you are using LibreOffice or OpenOffice, please download and open the file {{< resource_link 0b29d789-102d-f823-4725-6ff5f1e8a2e5 "ORscheduling (ODS)" >}}. If you are using Microsoft Excel, please download and open the file {{< resource_link c2d77b4a-52ea-41b7-fbbd-a781bfb50ed0 "ORscheduling (XLSX)" >}}. The following spreadsheets have the completed model as it is at the end of the video: {{< resource_link f9d0e9bc-adbc-f7fa-b487-085230efbceb "ORscheduling\_Complete (ODS)" >}} and {{< resource_link d0646520-c0ac-9a08-bcbe-fcfc16e416ee "ORscheduling\_Complete (XLSX)" >}}.

If you are using Excel, remember that you can indicate that the decision variables should be integer by adding an additional constraint, like we did in the Sports Scheduling lecture. Also, make sure to set a time limit by going into Options, and then in the Solving Limits section, setting Max Time to 100. The solver will probably give you the following message after 100 seconds: "The maximum time limit was reached; continue anyway?" Go ahead and select Stop, and then select Okay. Even though the solver was not able to prove that this solution is the optimal one, you should see an objective function value of 4.46. If you don't set a time limit, it might take Excel over 10 minutes to settle on the optimal solution!

Also, you might get a different solution than the one Angie gets in the following video. There are _multiple optimal solutions_ to this problem, so your solution might be another feasible solution with the optimal objective function value. You'll see in the next video how the constraints can be adjusted to find the optimal solution that better fits the problem. 

{{< resource 9969df46-1a30-e947-9785-9b83eb2e7ad4 >}}

*   {{< resource_link 8a92070b-71b9-513e-35b1-c9854c1ef91c "BackVideo 2: An Optimization Model" >}}
*   {{< resource_link 6e8bdbce-3ea9-e644-0e2b-66d90a657d47 "ContinueVideo 4: The Solution" >}}