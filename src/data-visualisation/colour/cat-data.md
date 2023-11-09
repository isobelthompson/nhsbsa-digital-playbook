---
layout: article
title: "Categorical Data"
description: "Colours used for categorical data at the NHSBSA"
status: DRAFT
tags: [data-viz, data-viz-colour]
order:
    data-viz: 2
    data-viz-colour: 3
---
## Categorical Data  
  
Categorical data can be divided into groups or categories by using names or labels.  
Using four categories is best practice for data visualisation. More than four series can make a chart too cluttered. Consider merging multiple categories or focusing the chart on a single entity if suitable.  
::: details Source
 
[Categorical data colour palette][cat 1]

:::    
  
For categorical data, the following colours taken from the NHS identity guideleines can be used:  

|       Colour       |   Tint   |   Hex Code    |
|--------------------|----------|---------------|
|   NHS Blue         |  100%    |   #005EB8     |
|   NHS Aqua Green   |  100%    |   #00A499     |
|   NHS Pink         |  100%    |   #AE2573     |
|   NHS Orange       |  100%    |   #ED8B00     |
|   NHS Green        |  100%    |   #009639     |
|   NHS Light Blue   |  100%    |   #41B6E6     |
|   NHS Blue         |  50%     |   #80afdc     |
|   NHS Aqua Green   |  50%     |   #80d2cc     |
|   NHS Pink         |  50%     |   #d792b9     |
|   NHS Orange       |  50%     |   #f6c580     |
|   NHS Green        |  50%     |   #80cb9c     |
|   NHS Light Blue   |  50%     |   #a0dbf3     |  
  
    
 ![NHS Blue Gradient](image.png)

Bear in mind that certain colours have certain meanings, and that use of colour is important.  
Whilst over 4 categories and colours is not recommended, you will notice that after the first 6 colours, the colours are repeated at a 50% tint, still distinguishable to the user, and not adding in additional colours.  
::: details Source
 
[NHS Identity guidelines][cat 2]  

:::
  

We recommend using our suggested colour palette in the order given in the list to make sure adjacent colours have enough contrast. It will also mean the colours will work for different types of colour blindness and in greyscale.  
::: details Source
 
[Categorical data colour palette][cat 3]  

::: 


### Simple charts  

Use a single colour for a single line chart, and all bars in vertical column charts and horizontal bar charts where there are no groups to highlight. NHS Blue (#005EB8) is the primary colour to be used across our products, and therefore the first colour in the palette.  
::: details Source
 
[Categorical data colour palette][cat 4] 

:::  
  
### Line charts  
  
As with stacked and clustered bar charts, we advise that line charts should have no more than four series.  
It is difficult to choose colours for line charts with more than two series. This is because it is not possible to have a chart colour palette of more than two colours where all colours have at least a 3 to 1 contrast ratio with:
- the background
- all other colours in the palette  
Lines do not always stay in the same order. So, it is not possible to make sure adjacent colours always have at least a 3 to 1 contrast ratio.  
This means that it is not possible to provide a palette for line charts with more than two series that would meet the contrast ratio requirements. So, you should only use line charts with more than two series when they are essential to getting information across. This will help you meet accessibility success criterion 1.4.11.  
  
Guidance, such as labelling lines, using textures or shapes for data points may work to distinguish multiple categories. You can see more advice on the [Categorical data colour palette][cat 5] page.  
  
  
    
### Pie charts  
  
Pie charts should use different shades of one colour where possible, rather than different colours. This is so a colour-blind user can easily distinguish between the segments with the colours being close together.  
  
::: details Source
 
[Data visualisation: Colours][cat 6]   
[About Colour Blindness][cat 7]

:::    


### RAG (Red/Amber/Green) status  
  
Colour should not be the only method fo conveying information.  
If you are using red to signal 'warning' or 'caution', and green to signal 'approval' or 'correctness' consider addign a symbol to make sure colour-blind users can still understand the message.  
  
Use additional encoding methods such as symbols or positions to convey meaning:  

 
  
[Source - ][cat 8]  


### ONS accessibility tested colours  

  
- Green: #0f8243  
  
  
- Neon yellow: #f0f762  
 

- Sun yellow: #fbc900  
  

- Jaffa orange: #fa6401  
  

- Red: #d0021b  
  

::: details Source
 
[ONS Service manual][cat 9] 

:::   


[Back to Colours home](/nhsbsa-digital-playbook/data-visualisation/colour)




[cat 1]: https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-colours-in-charts/#section-5
[cat 2]: https://www.england.nhs.uk/nhsidentity/identity-guidelines/colours/
[cat 3]: https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-colours-in-charts/#section-5
[cat 4]: https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-colours-in-charts/#section-5
[cat 5]: https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-colours-in-charts/#section-5
[cat 6]: https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-colours-in-charts/
[cat 7]: https://www.colourblindawareness.org/colour-blindness/
[cat 9]: https://service-manual.ons.gov.uk/design-system/foundations/colours