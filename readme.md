<h1> Baton Rouge Flooding </h1>

<img src="images/precip_hist_smooth.png" width="800">
<h4> Figure 1: Histogram of Baton Rouge August rainfall totals. </h4>
<br>
<img src="images/temp_precip2.png" width="800">
<h4> Figure 2: Scatter plots of North hemisphere surface temperature and Baton Rouge rainfall totals for August. </h4>

<h5> Temperature data from NASA and rainfall data from NOAA. </h5>

I’m a little late in posting this one because August is now a distant memory, but I found the discussion around the flooding in Baton Rouge both fascinating and terrifying. I recently learned that there is a schism in the federal government right now where the majority of congress denies climate change while many agencies such as FEMA, NASA, and the military both believe in and study the phenomenon. Some of these organizations avoid the term ‘climate change’  for fear of potential political repercussions. Others, like NASA, have fearlessly posted evidence of this climate change.

Figure 1 is a histogram of August rainfall totals in Baton Rouge over the last 126 years. The data point to the fair right is the rainfall for August 2016 and it sticks out like a sore thumb. Figure 2 contains a plot of Western surface temperature and Baton Rouge August rainfall over time. The temperature plot is alarming because it means both more water evaporating into the air from the water and air that hold greater masses of water. It’s not a stretch to say that physics suggest that 'excessive’ rainfall events will probably become more and more common in the coming years.

<img src="images/logos/nasa.png" width="120"> <img src="images/logos/noaa.png" width="120"> <img src="images/logos/python.png" width="120"> <img src="images/logos/matplotlib.png" width="120"> <img src="images/logos/jupyter.png" width="120"> <img src="images/logos/linux.png" width="120">
<br>
<h1> Fitting Distributions to WHO Mortality by Age Data </h1>

<img src="images/all_dist.png" width="800">
<h4> Figure 1: All distributions in SciPy stats fitted to WHO mortality by age data for the United States. </h4>
<br>
<img src="images/best_fit.png" width="800">
<h4> Figure 2: Best fitting distribution with paramaters. </h4>

<h5> All probability distributions from SciPy Stats were fit to World Health Organization global mortality data for the United States.  Images are in the images folder and Python code can be found in the Jupyter Notebook in the src folder. </h5>

Death is a fascinating topic because it’s the one thing all human beings will share, but we never talk about it. I recently came across World Health Organization data on age and cause of death for over 600,000,000 people over the last several years.

I thought it would be interesting to study the distribution of age of death. In statistics, distributions are used to describe how frequently a particular value appears. Even if you have never studied statistics, you are already familiar with the idea of a bell curve. This shape occurs so commonly that it’s referred to as a normal distribution.

There are many distributions of varying shapes used in statistics. Several of these distributions are used to describe failure rates of machines over time as parts wear out. I suspected that these distributions might also be applicable to the human body because we are machines that wear out. As it turns out, these distributions do a terrible job of describing human mortality rates. One plausible explanation for this difference is that unlike machines, the human body has an amazing ability to heal itself. As we lose this ability we die at higher and higher rates.

Out of the nearly 100 distributions I fit to the data (Figure 1), it was the log gamma distribution that best matched (Figures 2). This is a pretty exotic distribution, but it appears that lifetime modeling and the medical field are two of its primary uses.

<img src="images/logos/who.png" width="120"> <img src="images/logos/python.png" width="120"> <img src="images/logos/matplotlib.png" width="120"> <img src="images/logos/scipy.png" width="120"> <img src="images/logos/jupyter.png" width="120"> <img src="images/logos/linux.png" width="120">
<br>
<h1> Gephi Visualizations of Presidential Candidate Facebook Like Networks </h1>

<img src="images/clinton2.png" width="800">

<h4> Figure 1: Gephi visualization of the like network for Hillary Clinton's Facebook page. </h4>
<br>
<img src="images/trump2.png" width="800">
<h4> Figure 2: Gephi visualization of the like network for Donald Trump's Facebook page. </h4>

<h5> Gephi network visualizations of Facebook pages liked by people who liked Hillary Clinton's and Donald Trump's Facebook pages. </h5>

I present to you my first attempts at network visualization. I used an app name NetVizz to scrape information from the Facebook pages of Donald Trump and Hillary Clinton about what other pages are liked by people who like the pages of Trump and Clinton. The graphs were created with a piece of software named Gephi.

These figures reveal very curious trends I won’t attempt to explain, but please feel free to share your interpretations. Figure 1 (Clinton’s graph) is curiously dominated by Wellesley College pages with a large portion being dedicated to Democratic party pages. The lobes seem to be largely unconnected. Figure 2 (Trump’s plot) on the other hand, is a bizarre salad of TV entertainment and luxury brands. Strangely, Glamour, Vera Wang, Stewart Weddings, and BRIDES are in the network of this loud misogynist as well.

<img src="images/logos/facebook.png" width="120"> <img src="images/logos/gephi.png" width="120"> <img src="images/logos/win10.png" width="120">
<br>

<h1> Seattle 911 Plots </h1>

<img src="images/seattle_911_hexlog.png" width="800">
<h4> Figure 1: Logarithmic heat map of Seattle 911 calls. </h4>
<br>
<img src="images/seattle_911_hex.png" width="800">
<h4> Figure 2: Heat map of Seattle 911 calls. </h4>
<br>
<img src="images/seattle_911a.png" width="800">
<h4> Figure 3: Plot of 550,000 Seattle 911 calls by location. </h4>
<br>
<h5> Plots of public [Seattle 911](https://data.seattle.gov/Public-Safety/Seattle-Police-Department-911-Incident-Response/3k2p-39jp/data) data in the images folder.  Python code can be found in the Jupyter Notebook in the src folder. </h5>

I’ve revisited the Seattle 911 data to create these heatmaps (or hexbin 3D histograms if you prefer). The colors represent the number of 911 calls placed from within that hex.

Notice that Figure 2 is nearly entirely black with a single bright yellow cell near the center. The number of 911 calls placed from that cell is so much higher than any other cell, that it threw off the entire color scale. To reveal more definition, I created Figure 1 using a logarithmic scale. For those unfamiliar with logarithms, I applied some math to partially flatten the scale and capture more detail (https://en.wikipedia.org/wiki/Logarithmic_scale).

The mysterious yellow cell captured my curiosity so I examined it more closely. It is located where Downtown runs into Pioneer Square near the King County Courthouse. I had the biased assumption that high numbers of 911 calls would be associated with high crime rates, but the data revealed something entirely different. About three fourths of the calls were medically related, presumably due to the high concentration of people with limited resources, mental health issues, and addiction. Most of the remaining quarter were things like responses to automated fire alarms, bark fires, and a surprising number of elevator rescues. As it turns out, only a tiny portion of the calls were related to crime. The world is apparently safer and sadder than I imagined.

Figure 3 is a plot of the latitude and longitude for 550,000 calls placed to 911 in the city of Seattle. The shape of Seattle is quite clear because unsurprisingly, not a lot of 911 calls come from the bodies of water. The bridges however appear to hot spots presumably due to car accidents. Some places stand out for being devoid of calls such as the Zoo and the Port. Others, like downtown and good old Aurora are noticeably active. The striations that are visible in some of the residential areas are presumably the result of the algorithms are used anonymize the location by adding uncertainty. I plan to revisit this data with heat mapping.

<img src="images/logos/seattle.png" width="120"> <img src="images/logos/python.png" width="120"> <img src="images/logos/matplotlib.png" width="120"> <img src="images/logos/jupyter.png" width="120"> <img src="images/logos/linux.png" width="120">
<br>
