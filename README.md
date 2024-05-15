# One-bit DoA estimation

 We explore an application of deep unrolling in the direction of arrival (DoA) estimation problem when  coarse quantization is applied to the measurements.
We present a  compressed sensing formulation  for DoA estimation from one-bit data in which estimating  target DoAs  requires recovering  a sparse signal from a limited number of severely quantized linear measurements. In particular, we exploit covariance recovery from one-bit dither samples. To recover the covariance of transmitted signal, the learned iterative shrinkage and thresholding algorithm (LISTA) is employed fed by one-bit data. We  demonstrate that the upper bound of estimation performance is governed by the recovery error of the transmitted signal covariance matrix.
Through numerical experiments, we demonstrate the proposed LISTA-based algorithm's capability in estimating target locations.
![Screenshot 2024-05-15 134005](https://github.com/TaraEsmaeilbeig/one_bit_DoA_estimation/assets/154453606/e201d42a-e8f1-47c6-8bfc-0f40263caba9)

## Experimental result

We used a uniform linear array with $d=\lambda/2$ spacing and $M=\{8,16\}$ antennas equipped with one-bit ADCs. In all of our experiments, the DoA interval is set to $\Delta \theta=1^{\circ}$, with $K=2$ and $K=3$ targets are assumed to be in random locations in the interval $[-60^{\circ},60^{\circ}]$. 




|![Screenshot 2024-05-15 134635](https://github.com/TaraEsmaeilbeig/one_bit_DoA_estimation/assets/154453606/65879b8c-b2c3-45af-9e95-e6a6e52d7fde)<br>$K=3$|![Screenshot 2024-05-15 134339](https://github.com/TaraEsmaeilbeig/one_bit_DoA_estimation/assets/154453606/82157b81-582c-42a5-ab27-c7d1b012798b)<br>$K=2$|
|:-:|:-:|
