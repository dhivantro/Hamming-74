# AWGN Noise Channel Concept

## Formula visualizer
![awgn formulas](https://user-images.githubusercontent.com/61950429/140474902-27ca61ce-756e-4211-8769-81ff26f6d4c8.png)

## Coding steps
#### 1. Calculate code rate, R
    R= number of user bits,K / number of transmitted bits,N

#### 2. Calculate SNR (in dB)
    SNR is a variable in this research.
    So, users can specify any SNR values (snr_db) of their choice
    
#### 3. Calculate noise variance (sigma squared)
    variance = 1 / (code rate * 10^(snr_db/10)) 
    
#### 4. Calculate noise (sigma)
    noise = sqrt(variance) * randn(size of input signal)
    randn returns a random variable of mean 0 and variance 1
    
#### 5. Apply additive
    output[i] = input[i] + noise
    
#### 6. Hard-decision decoding 
    
    The float noise will be added to the input signal.
    If output[i]>0,  then output[i] = 1
    Else,                 output[i] = 0;
    
    *Note:
    In step 5, if SNR is very high, the noise will be 0.000000
    So, output [i] = input [i]
    Hence, with higher snr, the ber values will be low because there'll 
    be less bit errors.
    
