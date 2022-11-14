# Hydraulic-EoL-Testing
Multivariate Time Series Data usable for Time Series Segmentation and Time Series Classification. Each sample represents the multi-phased End-of-Line-Testing cycle of one hydraulic pump (evolution of 9 sensors). For confidentality reasons, the data were normalized (standard-score) and the sensor names anonymized.

Folder Structure:
<pre>
Data/
  Generation/                  Corresponding Generation. We have data from 2 generations (Generation A, Generation B)
    control type/              Coresponding pump control type. We have 3 different control types (Direct Control (DC), Proportional Control (PC), Speed-based Control (SC) )
      version/                 Coresponding version of specific control type. Only relevant for Generation A DC-pumps, where we have 3 version (V35, V36, V38)
        zip-file:              zip file containing all samples of the specific version. One Sample has the following name format:
                               [Generation]+"_"+[Control Type]+[Version]+"_"+[ID]+".csv"<br />
</pre>:                                    
                                    
 
                                    
Each sample contains a time-series with 11 channels (data collected at 100 Hz frequency):
1. Time-Index (in seconds)
2. Values of Sensors 1-9 (standard-score normalized, no units for confidentality reasons)
3. State Label (integer-encoded, meaning not further specified for confidentality reasons)

<pre>
The dataset was published in the context of one of our works:
Gaugel, S.; Reichert, M.: PrecTime: A Deep Learning Architecture for Exact Time Series Segmentation and its Application to Hydraulic End-Of-Line Testing, 2022
The subset referenced in the paper is found in the following path: Data/Generation A/DC
</pre>

# License 
The dataset created for the research located in the directory data are licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC-BY-4.0) .



