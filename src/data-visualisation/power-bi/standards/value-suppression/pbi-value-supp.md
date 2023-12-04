---
layout: article
title: "Suppression of values"
description: "Standards around the suppression of values with Power BI"
status: DRAFT
tags: [power-bi, pbi-val-supp, pbi-home, pbi-standards]
order:
    power-bi: 2
    pbi-val-supp: 1
    pbi-home: 6
    pbi-standards: 2
related:
  tag: pbi-standards
---
## Statistical Disclosure Control (SDC) Protocol  
  
The [Statistical Disclosure Control Protocol][link 1] was developed to suppress identifiable information and data from individuals where there is a small base size of between 1-4. Absolute 0 values are able to be shown within a table or chart. It is important to be mindful of percentages when implementing the SDC Protocol, as if the count can be worked out based on percentages, this will need to be suppressed.  
  
This chart is an example of what suppression of a count of between 1-4 can look like:  
  
![ alt text](../images/value-image.png)  
  
Note that the values of between 1 and 4 have been replaced with an asterisk (*) to indicate to the users that these values have been suppressed, and the bar size is shown as 0, to not give away the values.  
  

## Power BI implementation  
  
It is important to be able to implement this suppression within Power BI. To do this, an example will be shown using counts of leavers across the directorates.  
  
This is an example of the data to be used:  
  
![Alt text](../images/value-image2.png)  
  
The today or before column was created to filter on only dates only up to today’s date (in the past, rather than future amendments):  
  
= Table.AddColumn(#"Sorted Rows1", "Custom", each if [termination_month] > #date(2023, 11, 28) then null else [termination_month])  
  
Next a line chart was created with termination_month on the x axis, and Count on the y axis.  
  
The following measure was then created:  
  
![Alt text](../images/value-image3.png)  
  
'# Count' does the following:  
- sums up the counts
- makes sure for any missing combinations, 0 is shown
- if the Count is 0, 0 is returned
- if the count is 4 or less, -0.01 is returned, otherwise the original values are present  
  
Now any values higher than 0 but equal or less than 4 will be given the arbitrary value of -0.01. This is so that the values are marked out as distinct from 0, for use in other measures.  
  
'Chart Count' was next created as a measure:  
  
![Alt text](../images/value-image4.png)  
  
This replaces any -0.01 values with 0. This measure is used for the y axis.  
The minimum value for the y axis has been set as 0 for consistency.  
  
![Alt text](../images/value-image5.png)  
  
Redacted values of between 1 and 4 were not yet being labelled correctly for the user to see.
'# Headcount Label' was created as a measure to select these values. The below says if any values of '# Count' are greater than or equal to -0.001 (which all apart from the -0.01 values will be), then display 0*. The asterisk indicates to the user that low base sizes have been redacted. It is important to include this as a disclaimer on the dashboard so users are aware.  
  
![Alt text](../images/value-image6.png)  
  
Add '# Headcount Label' on as a tooltip:  
  
![Alt text](../images/value-image7.png)  
  
To make this clear to users, so that they can clearly see the 0* values, toggle Data labels as on, and add '# Headcount Label' in as a Custom label:  
  
![Alt text](../images/value-image8.png)  
  
Next, add the disclaimer onto the dashboard by toggling on a subtitle.  
  
Some text to use as the disclaimer:  
"To protect personal identifiable information, small base sizes between 1-4 have been replaced with 0*."  
  
![Alt text](../images/value-image9.png)  
  
Check and test the values against the raw data and the SDC Protocol should now be implemented within your chart. To reduce overhead, you can duplicate this chart and amend the measures/values where needed if the SDC Protocol is needed to be added to multiple charts.  
  
    
## Power BI Standards




  


[link 1]: https://www.nhsbsa.nhs.uk/sites/default/files/2020-10/nhsbsa-sdc-protocol.pdf