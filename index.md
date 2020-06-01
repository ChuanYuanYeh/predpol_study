---
layout: page
title: A Dive Into How Predictive Policing Works and its Effectiveness
description: A Dive Into How Predictive Policing Works and its Effectiveness
---
## Overview
As many cities move toward using machine learning in their policing systems, we want to explore how these systems affect the people being policed. Several cities have implemented the use of predictive policing algorithms including New York City NY and Santa Cruz CA. The models built for ‘predictive policing’ claim to have reduced crime and increased efficiency in police resources. These claims have led us to  investigate the question:  “How is predictive policing being used and what is the effect on traffic stops?”. 

Our goal is to see if there is a causal effect of reducing crime, and assess possible model bias in PredPol. We will look at data from the LAPD, and although the results cannot necessarily generalize, the structure of the predictive policing algorithms being used is similar: optimizing police resources to deter crime before it happens. 

The LAPD began deploying PredPol in three divisions (Foothill, Southeast, North Hollywood) back in 2013. It was then extended to all 21 divisions in 2015 as shown in the map below.

<style>.embed-container {position: relative; padding-bottom: 80%; height: 0; max-width: 100%;} .embed-container iframe, .embed-container object, .embed-container iframe{position: absolute; top: 0; left: 0; width: 100%; height: 100%;} small{position: absolute; z-index: 40; bottom: 0; margin-bottom: -15px;}</style><div class="embed-container"><iframe width="500" height="400" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" title="DSC180B_Viz_Intro" src="//ucsdonline.maps.arcgis.com/apps/Embed/index.html?webmap=2d68197739f54884b4d81f9329bb0376&extent=-118.7307,33.7142,-118.0585,34.4002&zoom=true&previewImage=false&scale=true&legend=true&disable_scroll=false&theme=light"></iframe></div>

We will proceed by looking at how trends in traffic/pedestrian stops, crimes, and arrests have changed since PredPol was deployed.

## How have crimes and arrests changed?
If PredPol's claims are true, we should be able to see a reduction in crime numbers once it was deployed. However, the animation below tells a different story. Although a few divisions did see a drop in crime numbers starting in 2013, most divisions saw an increase in 2015 when PredPol was deployed in all of them.
![Annual Crimes in LA](/assets/ezgif.com-gif-maker.gif)
On the other hand, arrest numbers in all divisions except for Hollywood and Central saw gradual decreases according to the animated map below. Our guess was that perhaps not all types of crimes were affected the same by PredPol. For example, increasing police presence in an area might discourage people to commit crimes that can be easily spotted in public. However, crimes that are more subtle such as computer hacking and fraud would not be affected as much. Thus, we then looked at how the distribution of crime types changed after PredPol was deployed.
![Annual Arrests in LA](/assets/arrests_animated.gif)

The interactive maps below show the statistics from testing how the proportions of each crime type changed in each division after PredPol was deployed. The first map displays the proportion of crimes committed while the second one shows the proportion of arrests being made for the selected crime type. For the tests, our null hypothesis was that the proportions are the same regardless of PredPol's deployment. At a significance level of 0.05, we reject the null hypothesis if the p-value falls under 0.05 and say that the proportion was either higher or lower depending on the sign of the statistic. By going through the different crime types, we can see that PredPol did not affect all crimes equally. Specfically, there was an overall increase in the proportions of property crimes being committed and arrested. On the other hand, financial crimes and other miscellaneous crimes saw decreases in both fields.

{% include crime_arrest_final.html %}

## Traffic & Pedestrian Stops
{% include stops.html %}


## Conclusion
