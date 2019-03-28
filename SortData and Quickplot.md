# SortData and Quickplot

Geochemical researches often require great amount work of comparing data to those in literature. It is necessary and significant to find a quick way to create figures to show their geochemical variation. Because most scholars use Microsoft Excel® to process data, I design a VB program which incorporates the most common geochemical discrimination figures, trace element spider diagrams, Haker diagrams and etc. While a great deal of software could do this job, my program has two unique advantages: (1) Quickly sort element sequence (2) Automatically Group data. These two functions could significantly increase work efficiency.

The next part will show how to run this program.
Let’s roll

##Sort data
The sequence of the major and trace elements listed in tables is different from author to author, which cause much inconvenience when comparing data to literature. The smart VB program (SortData.xlam) is designed to solve this problem. For example, If we have two columns of sample data like CB15-1 and CB15-2 (Fig. 1), And we want the elements to be set as SiO2, TiO2, Al2O3, Fe2O3, FeO, MnO, MgO, CaO, Na2O, K2O, P2O5, Fe2O3T, FeOT, Li, Be, Sc, Ti, V, Cr, Mn, Co, Ni, Cu, Zn, Ga, Ge, As, F, B, Sn, Cs, Rb, Mo, Cd, Sr, Zr, Nb, Sb, Ba, W, Tl, Hf, Ta, Pb, Bi, Th, U, Y, La, Ce, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Tm, Yb, Lu, LOI. 

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%203_1.jpg?raw=true" width="400" height="1000" >

Fig. 1 The results of sorting

The first step open a new workbook and put the data needed to be sorted in ‘Sheet1’ (Please note the first column is the name of elements). Next, press “Alt+F11” to open VBAproject, select DataSort and press “Run” (Fig. 2a), and a window will come up as shown in Fig. 2b. Press ‘Check element’ button. 

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%203_2.jpg?raw=true" width="300" height="250" >

Fig. 2 (a) How to run SortData program (b) The interface of SortData

Then, it will check the element name column A in the ‘Sheet1’. If there is something wrong, for example, if ‘Al2O3’ was mistakenly written as ‘AL2O3’, it will be highlighted with yellow shade (Fig. 3). You should correct it and run the program again. Please note that ‘Al2O3’ does not need to be written as ‘Al2O3’. 

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%203_3.jpg?raw=true" width="300" height="300" >

Fig. 3 Highlighting incorrect elements

After making sure the name of elements is all correct, click ‘SortData’ button. The data will be sorted as we want (Fig. 1). You can see that the sequence of CaO and MgO has been changed and there are some elements like Ge, and As is blank because the original data do not have them.

## Group data and plot
Copy the sort data into a new workbook and Open the ‘Quickplot.xlam’. The table cell A1, B1, C1, D1 is ‘Group name’, ‘Longitude and latitude’, ‘Age (Ma)’, and ‘Rock type’, respectively. If you do not know the latter three, just leave them blank, but you need to know names for each group. For example, I divide the data into four groups: ‘OB’, ‘GB’, ‘HG’, and ‘GT’ by rock type. You just type the group name in the first column of your data (Fig. 4). 

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%203_4.jpg?raw=true" width="700" height="700" >

Fig. 4 The result of grouping data

Press “Alt+F11” to open VBAproject and select ‘Quickplot’ and run. a window will come up as shown in Fig. 5. Click ‘Group’. The data will be grouped quickly (Fig. 4). And then click ‘Fe-calibration’ calibrate Fe2O3 and FeO into FeOT. 

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%203_5.jpg?raw=true" width="700" height="230" >

Fig. 5 The interface of SortData of Quickplot

And then, you could click all other buttons to get other plots like TAS, A-type granite discrimination, Haker diagram, S-type granite source region discrimination, zircon saturation thermometer (ZTS), and trace element spider diagram and ect (Fig. 6). 

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%203_6a.jpg?raw=true" width="700" height="600" >
<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%203_6b.jpg?raw=true" width="700" height="600" >
<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%203_6c.jpg?raw=true" width="700" height="600" >

Fig. 6 Representative figures made by Quickplot