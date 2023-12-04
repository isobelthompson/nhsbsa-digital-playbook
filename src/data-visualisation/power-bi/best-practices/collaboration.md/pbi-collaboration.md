---
layout: article
title: "Collaborative working"
description: "Best practices for working collaboratively using Power BI"
status: DRAFT
tags: [power-bi, pbi-collab, pbi-home, pbi-best-practice]
order:
    power-bi: 2
    pbi-collab: 1
    pbi-home: 3
    pbi-best-practice: 3
related:
  tag: pbi-best-practice
---
## Version control  
  
For dashboards which are being developed by more than one developer, it is possible for individuals to work on separate sheets in separate dashboards, likely a duplication of the dashboard (accessing to the same data set), developers would then copy the elements into a final dashboard. To do this, it is essential to manage the version control of dashboards, ensuring that dashboards are dated and the changes made to a dashboard are detailed for clarity when merging the dashboards.  
  
## Git integration  
  
[Power BI Desktop projects][link1] is currently in preview, which includes Git integration (a version control software). There are some pre-requisites to using Git included in the link provided. This allows changes to be merged using typical Git functionality. One of the advantages of Fabric is that it beings Git integration to Power BI which should allow more managed collaborative working once Fabric is more widely rolled out.  
  
## Power BI Explorer  
  
[Power BI Explorer is a free tool you can install on your machine][link2]. For dashboards which are being developed by more than one developer, you can create a copy of the dashboard and then compare changes, or compare changes of your report using Git. You can follow a tutorial within the tool itself.  
  
### Comparing reports  
  
Compare reports allows you to see two reports side by side and compare any changes between the two. The visuals and items each have a code which helps to track their changes across the dashboard versions.  
  
You can point this at a Git repository to compare versions, meaning you would not need to keep multiple versions of the same file. For Git, Power BI Explorer knows if your file is in a Git repository which allows you to see changes from a point in time, for example, to compare an uncommitted report to a committed report.  
  
Select 'Compare report':  
  
![Screenshot showing the first page that is shown when you open Power BI Explorer on your desktop, with four boxes in a horizontal row in the centre of the screen. From left to right the boxes are labelled 'Inspect report', 'Compare report', 'Analyze report', 'Guided tour'. The box labelled 'Compare report' has a pale yellow background and contains a simple image of two sheets of paper with an arrow pointing from each one to the other. This entire box is outlined in red to show that it is what you should select when you open Power BI Explorer with the intention of comparing reports.](../images/pbi-explorer1.png)  
  
Select the reports you wish to compare:  
  
![Screenshot of the page that appears after you select 'Compare report' from the initial screen. The page is made up of 4 main sections, with the 2 on the left hand side of the page for one report and the 2 on the right hand side for the second. The top left shows the file name of the left hand side's report, and in this screenshot is outlined in a red box for emphasis. The top right shows the words 'Click to open comparison report' and this is also outlined in a red box.](../images/pbi-explorer2.png)  
  
By expanding Pages you can see which pages have been added/removed/amended:  
  
![Screenshot showing the page that opens after you select 'Pages' on the previous screen. The file names of the 2 reports being compared are at the top of the screen, and the bottom half of the screen has on the left hand side a table for report 1's 'Object/Property' and 'Value', and on the right hand side the same for report 2. In this screenshot only the right table is populated](../images/pbi-explorer3.png)  
  
This section works like Git in that items highlighted in red have been removed, and items highlighted in green have been added.  
  
You can click on items under Visuals and see where they are positioned on the screen:  

![Alt text](../images/pbi-explorer4.png)  
  
You can compare an overview of the pages included in each version below:  
  
![Alt text](../images/pbi-explorer5.png)  
  
You can refine what is shown and what you wish to compare in the drop down below:  
  
![Alt text](../images/pbi-explorer6.png)  
  
![Alt text](../images/pbi-explorer7.png)  
    

### Inspecting reports  
  
This section gives a breakdown of pages and visuals.  
  
Select 'Inspect report' and load in your .pbix file:  
  
![alt text](../images/pbi-explorer8.png)  
  
The Summary page gives you information on: Pages, Visuals, Fields, Filters, Issues and Themes.  
  
![alt text](../images/pbi-explorer9.png)  
  
The Details tab gives further information. You can see a wireframe of the dashboard, and when you select a visual: dimensions, x/y/z coordinates and drilldown functionality:  
  
![Alt text](../images/pbi-explorer10.png)  
  
Values such as dimensions, categories, series can be checked against the default values to see if any values have changed.  
  
Interactions between visuals can be shown:  
  
![alt text](../images/pbi-explorer11.png)  
  
When you hover over some of the visuals the inbound and outbound interactions are highlighted between visuals. These interactions would otherwise be invisible on Power BI Desktop.  
  
Inbound interactions are shown in yellow:  
  
![alt text](../images/pbi-explorer12.png)  
  
Outbound interactions are shown in blue:  
  
![alt text](../images/pbi-explorer13.png)  
  
Track usage in the Data Model Explorer shows which variables are being used and where:  
  
![Alt text](../images/pbi-explorer14.png)  
  
## Power BI Best Practices

[link1]: https://learn.microsoft.com/en-us/power-bi/developer/projects/projects-git
[link2]: https://www.pbiexplorer.com/