## Repository includes 
  <ul>
    <li>1 Tableau presentation (PDF)</li>
    <li>1 Powerpoint presentation (PDF)</li>
    <li>1 Jupyter Notebook file (IPYNB)</li>
    <li>9 dataset files (CSV)</li>
    <ul>
      <li> 1 for harmful algae blooms data</li>
      <li>8 for water levels data (one dataset per year from 2015 - 2022)</li>
    </ul>
  </ul>

## Data sources
<ul>
  <li>https://iris.who.int/bitstream/handle/10665/42591/9241545801.pdf?sequence=1</li>
  <li>https://tidesandcurrents.noaa.gov/waterlevels.html?id=8726520</li>
  <li>https://geodata.myfwc.com/datasets/myfwc::recent-harmful-algal-bloom-hab-events/about</li>
</ul>

## Explanation of variables
<ul>
  <li>Algae blooms are defined by various sources as a sudden increase in algae cell concentration of anywhere from 1,000 - 3,000 cells/mL. We will be using the 3,000 cells/mL threshold for this analysis.</li>
  <li>WHO sets official health guidelines for freshwater algae blooms rather than coastal or marine blooms. For the purposes of setting concrete parameters for data analysis, we will be using WHO's freshwater standards for cell count/mL.
  <li>Whether a bloom is "harmful" depends on the species and concentration of algae.</li>
</ul>
<b>Harmful algae bloom (HAB) risk levels:</b>
  <ul>
    <li>0 - 3,000 cells/mL: Within normal range</li>
    <li>3,000 - 20,000 cells/mL: Indicates probable algae bloom with very low probability of health effects</li>
    <li>20,000 - 100,0000 cells/mL: Relatively low probability of adverse health effects</li>
    <li>100,000+: Moderate probability of adverse health effects</li>
  </ul>
</ul>
<b>Water level changes</b>
<ul>
  <li>Assessed relation of water level changes to HAB events with a rolling 1-week standard deviation in water levels.</li>
</ul>
<b>Fields</b>
<ul>
  <li>DEPTH: depth of sample taken</li>
  <li>LOCATION: approximate location where sample was retrieved</li>
  <li>NAME: name of algae species</li>
  <li>OBJECTID: numeric ID of measurement</li>
  <li>HAB_ID: string ID of measurement</li>
  <li>risk_level: string (none, low, med, high)</li>
  <li>risk_level_int: integer indicator of risk level (1 = med/high, 0 = none/low)</li>
  <li>hab_event_int: integer indicator of active hab event (1 = >3k cell count, 0 = <3k cell count)</li>
  <li>RollStdev 1 week / 1 day: aggregated stddev verified water level of the previous 7 days or 1 day</li>
  <li>Rolling mean 1 week / 1 day: aggregated mean verified water level of the previous 7 days or 1 day</li>
  <li>Verified (ft): verified water level measurement</li>
  <li>ft_off_avg: difference between the average water level and the measured entry water level</li>
</ul>
