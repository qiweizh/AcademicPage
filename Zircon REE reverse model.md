# Zircon REE reverse model
## 1. Overview of Zircon_in-situ
Zircon_in-situ is a program that calculates the percentage of co-precipitation minerals (x) with zircon whose trace element composition variation is caused by co-precipitation minerals’ crystallization in a closed system. Modeling of crystallization in Zircon_in-situ is based on the in-situ fractionation formula (Hanson and Langmuir 1978) and nonnegative least squares method (Lawson and Hanson 1974). This program runs in the MATLAB®2012a or higher vision. This program could be download in the supplemtary files in my paper on [Chemical Geology].(https://www.sciencedirect.com/science/article/abs/pii/S0009254118303814)

## 2. Input file
Zircon_in-situ contains three input files (.csv): (1) Parameter file. The parameters include the range of remaining melt (F) and its calculation step, and the range of mean fraction of the mixture of liquids returned from the solidification zone (f) and its calculation step. (2) Zircon trace element composition file. It includes initial and terminal zircon composition and normative zircon composition. (3) Partition coefficients file.

###2.1	Parameter file
A typical parameter file is shown in the Fig.S1. It displays the initial and terminal point and calculation step of (F) and (f).

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%20S1.png?raw=true" width="400" height="110" >

Figure S1 Parameter file 

###2.2	Zircon trace element composition file
The zircon trace element composition file consists of a 5\times (m+1) matrix (Fig. S2), where m is the number of trace elements involved in calculation. The first row is the names of elements. The second row is the initial composition of zircon, and the third row is the terminal composition of zircon. The fourth row is normative zircon composition. The purpose of setting normative zircon composition is to normalize the trace element composition of samples to standout the compositional variation among samples.

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%20S2.png?raw=true" width="700" height="90" >

Fig. S2 Zircon trace element composition file

###2.3	Partition coefficients file

The partition coefficients file consists of a (n+1)\times(m+1) matrix, where m is the number of trace element and n is the number of minerals involved calculation. In the matrix, the first row is the name of each trace element. And the first column is the name of each mineral. Note that the partition coefficients of zircon must be put in the second row. (Fig. S3).

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%20S3.png?raw=true" width="700" height="140" >

Fig. S3 Partition coefficients file

##3. How to run Zircon_in-situ
After preparing all input files for running, open the MATLAB®, make sure the main program (Zircon_in_situ.m) and the three input files should be put in the same work path. Then select the Zircon_in_situ.m file and click right mouth button to run (Fig. S4).

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%20S4.png?raw=true" width="400" height="400" >

Fig. S4 Operation interface of Zircon_in_situ

##4. Output file
After running the program, the results are shown in a figure and a Table in .txt format file.
### 4.1	Result figure 1
Figure 1 shows the result of optimal mineral assemblage. It contains 3 subfigures. The left figure shows the initial and terminal composition of zircon and the calculated zircon composition after crystallization. The middle figure shows the residue for each element. The third figure shows the contribution rate for every mineral on each element.

<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%20S5.png?raw=true" width="700" height="350" >

Fig. S5 Result figure 2. 

### 4.2	Result table
The result table contains: (1) the sum of residue (2) optimal value of F, f and x. (3) Calculated terminal accessory mineral composition; (4) residue for each element (5) The bulk partition coefficients for each element (6) contribution matrix.


<img src="https://github.com/qiweizh/Qiweizh.github.io/blob/master/img/Fig.%20S6.png?raw=true" width="700" height="500" >

Fig. S6 Result table