<!DOCTYPE html>
<html>
<head>

</head>
<body>
<h2>Installation guide</h2>  

<h5>Using Anaconda</h5>
  <ul>
    <li>Download Anaconda from <a href="https://www.anaconda.com/">https://www.anaconda.com/</a> and install it</li>
    <li>Clone the GitHub repository by using this link: <code>https://github.com/Faisalse/DGCF.git</code></li>
    <li>Open the Anaconda command prompt</li>
    <li>Move into the <b>DGCF</b> directory</li>
    <li>Run this command to create virtual environment: <code>conda create --name DGCF_env python=3.6</code></li>
    <li>Run this command to activate the virtual environment: <code>conda activate DGCF_env</code></li>
    <li>Run this command to install the required libraries for CPU: <code>pip install -r requirements.txt</code></li>
  </ul>
</p>

<h3>Follow these steps to reproduce the results for DGCF and baseline models</h3>

<ul>
<li>Run this command to reproduce the experiments for the DGCF on the Yelp2018 dataset: <code>python run_experiments_for_DGCF_algorithm.py --dataset yelp2018</code>  </li>

<li>Run this command to reproduce the experiments for the baseline models on the Yelp2018 dataset: <code>python run_experiments_DGCF_baseline_algorithms.py --dataset yelp2018</code>  </li>

<li>Run this command to reproduce the experiments for the DGCF on the Gowalla dataset: <code>python run_experiments_for_DGCF_algorithm.py --dataset gowalla</code>  </li>

<li>Run this command to reproduce the experiments for the baseline models on the Gowalla dataset: <code>python run_experiments_DGCF_baseline_algorithms.py --dataset gowalla</code>  </li>

<li>Run this command to reproduce the experiments for the DGCF on the Amazon-book dataset: <code>python run_experiments_for_DGCF_algorithm.py --dataset amazonbook</code>  </li>

<li>Run this command to reproduce the experiments for the baseline models on the Amazon-book dataset: <code>python run_experiments_DGCF_baseline_algorithms.py --dataset amazonbook</code>  </li>




</body>
</html>  

