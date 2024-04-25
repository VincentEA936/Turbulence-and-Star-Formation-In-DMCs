# Turbulence-and-Star-Formation-In-DMCs

## Background:

This project explores the relationship between turbulence and high-mass star formation in dense molecular clouds (DMCs) by measuring the turbulence of molecular transitions found in denser clumps of gas. The earliest evolutionary stages of high-mass star formation are poorly understood due to these stars being deeply embedded in dense, optically thick regions of molecular clouds where observations are difficult. However, radio and infrared molecular line surveys can be used to penetrate these regions and obtain unique information about the gas kinematics, temperature, and gas density for different elements. One example of these surveys is the Radio-Ammonia Mid-Plane Survey (RAMPS), a molecular line survey using the Green Bank Telescope (GBT) of 13 different lines and transitions found in the Northern Mid-Galactic Plane. The major target of RAMPS was measuring the first five metastable transitions of Ammonia (NH3(1,1)), which are very useful for accurately measuring the gas temperature and optical depth by using the main-to-satellite line ratio. In addition, NH3(1,1) has been used as a molecular tracer for identifying denser clumps of gas, since it is typically only abundant in very cold (<100 K), dense regions and rarely found outside of these gas clumps.

## Methods:

By identifying denser gas clumps in these regions and measuring the turbulence and gas density, we can get a better understanding on how turbulence is connected with star formation. Star formation is essentially a battle between gravity collapsing inwards and gas pressure pushing outwards; therefore, we would expect that regions of low gas turbulence will have denser clumps aiding star formation. The first step was implementing K-Means clustering, an unsupervised machine learning algorithm used for spatially clustering data into unique clumps. Although this method is quite simple, it provides interpretable results that can be easily visualized in a scatterplot. One issue with K-Means clustering is that the number of clumps, K, needs to be entered - which can pose an issue with clustering data, especially when different initializations represent different features of the data. This was resolved by iteratively performing K-Means Clustering for each region in the data and measuring the silhouette score, a quality metric that determines how well the within-clump separation of data points represents the data. This metric is ranked from [-1,1] where 1 is perfect clustering and -1 is bad clustering (the max score was typically on the order of 0.7-0.8 and none of the scores measured were negative. 

With the clumps identified, we could then measure the average turbulence and density of each clump and plot the data in a scatterplot to see what turbulence value corresponds to the most gas clumps. These dense clumps are the earliest indicators of early star formation, and thus a critical stage in the evolution of molecular clouds into star-forming regions.

