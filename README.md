# Hydraulic-EoL-Testing
Multivariate Time Series Data usable for Time Series Segmentation and Time Series Classification. Each sample represents the multi-phased End-of-Line-Testing cycle of one hydraulic pump (evolution of 9 sensors). For confidentality reasons, the data were normalized (standard-score) and the sensor names anonymized.

The dataset was published in the context of one of our research articles:
<pre>
Gaugel, S.; Reichert, M.: PrecTime: A Deep Learning Architecture for Precise Time Series Segmentation in Industrial Manufacturing Operations, 2023
</pre>
<br/>
<br/>

<b>Folder Structure:</b>
<pre>
Data/
  Generation/                  Corresponding Generation. We have data from 2 generations (Generation A, Generation B)
    control type/              Coresponding pump control type. We have 3 different control types (Direct Control (DC), Proportional Control (PC), Speed-based Control (SC) )
      version/                 Coresponding version of specific control type. Only relevant for Generation A DC-pumps, where we have 3 version (V35, V36, V38)
        zip-file:              zip file containing all samples of the specific version. One Sample has the following name format:
                               "Pump_"+[Generation]+"_"+[Control Type]+[Version]+"_"+[ID]+".csv"<br />
</pre>                                    
                                     
Each sample contains a time-series with 11 channels (data collected at 100 Hz frequency):
1. Time-Index (in seconds)
2. Values of Sensors 1-9 (standard-score normalized, no units for confidentality reasons)
3. State Label (integer-encoded, meaning not further specified for confidentality reasons)

# Publications 
### Publication 1: "PrecTime: A Deep Learning Architecture for Precise Time Series Segmentation in Industrial Manufacturing Operations" (2023)
Authors: Gaugel, S.; Reichert, M. <br/>
The subset referenced in the paper is found in the following path: <br/>
<pre>
V35: Data/Generation A/DC/V35
V36: Data/Generation A/DC/V36
V38: Data/Generation A/DC/V38
</pre>
Preprint found at
https://www.academia.edu/96528691/PrecTime_A_Deep_Learning_Architecture_for_Precise_Time_Series_Segmentation_in_Industrial_Manufacturing_Operations


### Publication 2: "Industrial Transfer Learning for Multivariate Time Series Segmentation: A study on the example of hydraulic pump testing cycles" (2023)
Authors: Gaugel, S.; Reichert, M. <br/>
The subsets referenced in the paper are found in the following paths: <br/>
<pre>
DC-V35: Data/Generation A/DC/V35
DC-V36: Data/Generation A/DC/V36
DC-V38: Data/Generation A/DC/V38
SC: Data/Generation A/SC/V12
PC: Data/Generation A/PC/V23
</pre>

### Publication 3: "Supervised Time Series Segmentation as Enabler of Multi-Phased Time Series Classification: A Study on Hydraulic End-of-Line Testing" (2023)
Authors: Gaugel, S.; Wu, B.; Anand, A.; Reichert, M.<br/>
The subset referenced in the paper is found in the following paths: <br/>
<pre>
Generation B: Data/Generation B/DC/V03
</pre>


# License 
The dataset created for the research located in the directory data are licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC-BY-4.0) .



