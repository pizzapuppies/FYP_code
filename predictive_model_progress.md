For the predictive models:
I tried inputing raw data from the csv

test 1 : [freq,  real,  im]
this model got an average of 70% on 10 runs

test 2 : [real,  im]
This model got an average of 60% on 10 runs

** Some times the models got 100% it happened about 3 times in 10 run for both tests 

I tried to use impedance.py to extract reynolds circuit to help the model learn, but the library doesn't let the code just read the parameters for some reason.
It can print them but the code can't read them because a custom circuit object is "unsubsciptable"

So I'm gonna use impedance.py to find the circuit and then predict what the idealized results should have looked like and train the model on the idealized reynolads circ.

Test 3 : [predicted real, predicted imag] * 
This model got an average of 40% on 10 runs

*The predictions are suspect, when compared to the real data the delta is not neglegable. If their is any learnable difference then the impedence lib could be just mudding up the data  


**


$ another thing to explore is the config of the CNN i tried adding layers and moving their order around. It showed little to no difference, at least neglegable differance considering that the randomization on rerun is huge rangeing from 20% accuracy to 100 % 

