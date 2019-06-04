In this Jupyter Notebook, I tried to replicate findings of the following paper

https://pdfs.semanticscholar.org/7465/5a89427878ee237b103e657a1651bbf3d497.pdf


Dataset was provided at the following URL by authors of the paper 

https://github.com/barisbozkurt/MASTmelody_dataset


Description of steps in Python Notebook
1. The voice frequency data and piano frequency data were matched and Dynamic Time Warp 
was run on them to find distance (deviation) between voice and piano frequencies. 15000 
such data points were collected.

2. This data was stored in .csv file called "distance.csv'.

3. Paralelly, another .csv file was made that stored output data about grades (pass or fail)
given to the particular performance in 'distance.csv'. This file was called 'result.csv'.

Both these files are available on GitHub. This is done to avoid generating 15000 samples everytime.
15000 sammples take about 24 hours to make because DTW is a slow process.

4. Code for Random Forrest Classification model was downloaded from 
https://stackabuse.com/classification-in-python-with-scikit-learn-and-pandas/
When 'distance' and 'result' was fed into this model, a mean prediction accuracy of 0.69 was acheived. 

