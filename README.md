# quantum-random-number-generator
----------------------------------
---------  Introduction  ---------
----------------------------------
The aim of this function is to provide real random numbers for sensitive applications, 
which cannot accept the pseudorandomness of Matlab's "randperm(N, K)"  

----------------------------------
---------  Description-  ---------
----------------------------------
This function returns a row vector with "n" REAL RANDOM NUMBERS with values between [1-"n"] and NO REPETITION.  
These random numbers are generated in real time (Internet connection is needed) from the Australian National University's Quantum Random Numbers Server.  
The returned numbers can be "uint8" (0 to 255) or "uint16" (0 to 65,535) type of integers

----------------------------------
---------  Elapsed time  ---------
----------------------------------
The function needs a random time to retrieve the asked array of numbers. As an illustration, using a computer with 6 cores, these are the obtained results for different scenarios:  
########## Executed command ########## || ########## Elapsed time (s) ##########  
>> quantumRandomGenerator( 1, 'uint8')                     0.73  
>> quantumRandomGenerator( 50, 'uint8')                    0.73  
>> quantumRandomGenerator( 100, 'uint8')                   0.73  
>> quantumRandomGenerator( 150, 'uint8')                   0.73  
>> quantumRandomGenerator( 200, 'uint8')                   0.73  
>> quantumRandomGenerator( 200, 'uint16')                 35.95  
>> quantumRandomGenerator( 852, 'uint16')                 57.03  
>> quantumRandomGenerator(4216, 'uint16')                 53.22  
