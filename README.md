# Li-ion-Battery-Digital-Twin-and-Discharge-Capacity-Prediction
This repo is the project on Simulating the Digital Twin of a Li-ion Battery's discharge capacity.

This repo is the project on Simulating the Digital Twin of a Li-ion Battery's discharge capacity. The project was inspired heavily from Javier Marin's article and code (cited). The project involves using the NASA Aging Batteries Datasets for experimental data, an empirical model of the degradation of Battery capacity over its lifetime and training a neural network to fit this data. 

Empirical model formula:
  
$$L = 1 - (1 - L')\exp^{f_{d}}$$

where $f_d$ is the degradation per unit time per cycle for Battery with Lifetime $L$ and initial battery lifetime $L'$. $f_d$ depends on the charge-discharge cycle time $t_i$, battery temperature $T_c$, cycle index $i$ and the empirical constant $k$ in the following way:

$$f_{d} = k\frac{i T_c}{t_i}$$

This neural network was then combined with the available Experimental Data to achieve our aim of forming a Digital Twin of the Li-ion battery.
Predictions were made and results were compared between the Digital Twin and the physical model. The discharge capacity up to a further approximately 330 cycles were predicted for a total of 500 charge-discharge cycles. As a conclusion, we see a decline in the battery capacity over its lifetime of 500 charge-discharge cycles.

Source:
https://towardsdatascience.com/how-to-build-a-digital-twin-b31058fd5d3e
https://data.nasa.gov/dataset/Li-ion-Battery-Aging-Datasets/uj5r-zjdb
