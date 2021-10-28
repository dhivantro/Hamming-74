# AWGN Noise Channel Concept

(This concept method was derived from MATLAB's AWGN sourcecode)

#### 1. Calculate signal power 
    Can make it a constant (Eg: sigp=1;)

#### 2. Calculate SNR
    snr = 10 ^ (signal power/10)
    
#### 3. Calculate noise power
    noise power = signal power/snr
    
#### 4. Calculate noise
    noise = sqrt(noisepower) * randn(size of input signal)
    
#### 5. Apply additive calculation 
    output = noise+input
