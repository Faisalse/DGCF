<!DOCTYPE html>
<html>
<head>

</head>
<body>
<h2>Intent Aware Recommender Systems</h2>

<h2>Installation guide</h2>  

<h5>Using Anaconda</h5>
  <ul>
    <li>Download Anaconda from <a href="https://www.anaconda.com/">https://www.anaconda.com/</a> and install it</li>
    <li>Clone the GitHub repository by using this link: <code>https://github.com/Faisalse/Intent_Aware_Recomm_Systems.git</code></li>
    <li>Open the Anaconda command prompt</li>
    <li>Move into the <b>DGCF</b> directory</li>
    <li>Run this command to create virtual environment: <code>conda create --name DGCF_env python=3.7</code></li>
    <li>Run this command to activate the virtual environment: <code>conda activate Intent_Aware_Recomm_Systems</code></li>
    <li>Run this command to install the required libraries for CPU: <code>pip install -r requirements_cpu.txt</code>. However, if you have support of CUDA-capable GPUs, 
        then run this command to install the required libraries to run the experiments on GPU: <code>pip install -r requirements_gpu.txt</code></li>
  </ul>
</p>
<h3>Note:</h3>
<p align="justify">STAMP and DGCF were designed by using the older versions of the TensorFlow  and Python. Therefore, we provide seperate settings to run the experiments for these models.</p>
<ul>
<li>Python=3.7.16</li>
<li>TensorFlow=1.14.0</li>
</ul>


<h2>Follow these steps to reproduce the results for Intent Aware and Non-Intent Aware Recommender Systems</h2>


<h5>DGCF and baseline models</h5>
<ul>

<li>Run this command to reproduce the experiments for the DGCF on the Yelp2018 dataset: <code>python run_experiments_for_DGCF_algorithm.py --dataset yelp2018</code>  </li>

<li>Run this command to reproduce the experiments for the baseline models on the Yelp2018 dataset: <code>python run_experiments_DGCF_baseline_algorithms.py --dataset yelp2018</code>  </li>

<li>Run this command to reproduce the experiments for the DGCF on the Gowalla dataset: <code>python run_experiments_for_DGCF_algorithm.py --dataset gowalla</code>  </li>

<li>Run this command to reproduce the experiments for the baseline models on the Gowalla dataset: <code>python run_experiments_DGCF_baseline_algorithms.py --dataset gowalla</code>  </li>

<li>Run this command to reproduce the experiments for the DGCF on the Amazon-book dataset: <code>python run_experiments_for_DGCF_algorithm.py --dataset amazonbook</code>  </li>

<li>Run this command to reproduce the experiments for the baseline models on the Amazon-book dataset: <code>python run_experiments_DGCF_baseline_algorithms.py --dataset amazonbook</code>  </li>




</body>
</html>  

