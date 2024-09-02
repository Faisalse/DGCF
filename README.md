<!DOCTYPE html>
<html>
<head>

</head>
<body>
<h2>Intent Aware Recommender Systems</h2>

<h2>Installation guide</h2>  
<p>This is how the framework can be downloaded and configured to run the experiments</p>
<h5>Using Docker</h5>
<ul>
  <li>Download and install Docker from <a href="https://www.docker.com/">https://www.docker.com/</a></li>
  <li>Run the following command to "pull Docker Image" from Docker Hub: <code>docker pull shefai/intent_aware_recomm_systems</code>
  <li>Clone the GitHub repository by using the link: <code>https://github.com/Faisalse/Intent_Aware_Recomm_Systems.git</code>
  <li>Move into the <b>Intent_Aware_Recomm_Systems</b> directory</li>
  
  <li>Run the command to mount the current directory <i>Intent_Aware_Recomm_Systems</i> to the docker container named as <i>intent_aware_recomm_systems_container</i>: <code>docker run --name intent_aware_recomm_systems_container  -it -v "$(pwd):/Intent_Aware_Recomm_Systems" -it shefai/intent_aware_recomm_systems</code>. If you have the support of CUDA-capable GPUs then run the following command to attach GPUs with the container: <code>docker run --name intent_aware_recomm_systems_container  -it --gpus all -v "$(pwd):/SessionRecGraphFusion" -it shefai/intent_aware_recomm_systems</code></li> 
<li>If you are already inside the runing container then run the command to navigate to the mounted directory <i>Intent_Aware_Recomm_Systems</i>: <code>cd /Intent_Aware_Recomm_Systems</code> otherwise starts the "intent_aware_recomm_systems_container"</li>
<li>Finally, follow the given instructions to run the experiments for each model </li>
</ul>  
<h5>Using Anaconda</h5>
  <ul>
    <li>Download Anaconda from <a href="https://www.anaconda.com/">https://www.anaconda.com/</a> and install it</li>
    <li>Clone the GitHub repository by using this link: <code>https://github.com/Faisalse/Intent_Aware_Recomm_Systems.git</code></li>
    <li>Open the Anaconda command prompt</li>
    <li>Move into the <b>Intent_Aware_Recomm_Systems</b> directory</li>
    <li>Run this command to create virtual environment: <code>conda create --name Intent_Aware_Recomm_Systems python=3.8</code></li>
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
<h5>TAGNN and baseline models</h5>
<ul>
<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Yoochoose</a> dataset, unzip it and put the “yoochoose-clicks.dat” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the TAGNN and baseline models on the shorter version of the Yoochoose dataset: <code>python run_experiments_TAGNN_And_baseline_models.py --dataset yoochoose1_64</code></li>
  
<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Diginetica</a> dataset, unzip it and put the “train-item-views.csv” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the TAGNN and baseline models on the Diginetica dataset: <code>python run_experiments_TAGNN_And_baseline_models.py --dataset diginetica</code></li> 
</ul>

<h5>GCE_GNN and baseline models</h5>
<ul>
<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Diginetica</a> dataset, unzip it and put the “train-item-views.csv” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the GCE_GNN and baseline models on the Diginetica dataset: <code>python run_experiments_GCE_GNN_And_baseline_models.py --dataset diginetica</code></li> 

<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Nowplaying</a> dataset, unzip it and put the “nowplaying.csv” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the GCE_GNN and baseline models on the Nowplaying dataset: <code>python run_experiments_GCE_GNN_And_baseline_models.py --dataset nowplaying</code></li> 

<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Tmall</a> dataset, unzip it and put the “dataset15.csv” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the GCE_GNN and baseline models on the Tmall dataset: <code>python run_experiments_GCE_GNN_And_baseline_models.py --dataset tmall</code></li> 
</ul>

<h5>DIDN and baseline models</h5>
<ul>

<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Yoochoose</a> dataset, unzip it and put the “yoochoose-clicks.dat” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the DIDN and baseline models on the shorter version of the Yoochoose dataset: <code>python run_experiments_for_DIDN_baseline_models.py --dataset yoochoose1_64</code> and run the following command to create the experiments for the larger version of the Yoochoose dataset <code>python run_experiments_for_DIDN_baseline_models.py --dataset yoochoose1_4</code>  </li>
  
<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Diginetica</a> dataset, unzip it and put the “train-item-views.csv” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the DIDN and baseline models on the Diginetica dataset: <code>python run_experiments_for_DIDN_baseline_models.py --dataset diginetica</code></li> 

</ul>

<h5>NARM and baseline models</h5>
<ul>

<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Yoochoose</a> dataset, unzip it and put the “yoochoose-clicks.dat” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the NARM and baseline models on the shorter version of the Yoochoose dataset: <code>python run_experiments_for_NARM_And_baseline_models.py --dataset yoochoose1_64</code> and run the following command to create the experiments for the larger version of the Yoochoose dataset <code>python run_experiments_for_NARM_And_baseline_models.py --dataset yoochoose1_4</code>  </li>
  
<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Diginetica</a> dataset, unzip it and put the “train-item-views.csv” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the NARM and baseline models on the Diginetica dataset: <code>python run_experiments_for_NARM_And_baseline_models.py --dataset diginetica</code></li> 

</ul>

<h5>HIDE and baseline models</h5>
<ul>

<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Tmall</a> dataset, unzip it and put the “dataset15.csv” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the HIDE and baseline models on the Tmall dataset: <code>python run_experiments_HIDE_And_baseline_models.py --dataset Tmall</code></li> 
<li>Run this command to reproduce the experiments for the HIDE model with original train-test splits and without any modification in the code: <code>python run_experiments_for_HIDE_withoutAnyChanges.py --dataset Tmall</code></li>
</ul>

<h5>KIGN and baseline models</h5>
<ul>
<li>Run this command to reproduce the experiments for the KGIN and baseline models on the lastFm dataset: <code>python run_experiments_for_KGIN_baselines_algorithms.py --dataset lastFm</code>  </li>

<li>Run this command to reproduce the experiments for the KGIN and baseline models on the alibabaFashion dataset: <code>python run_experiments_for_KGIN_baselines_algorithms.py --dataset alibabaFashion</code>  </li>
<li>Run this command to reproduce the experiments for the KGIN and baseline models on the amazonBook dataset: <code>python run_experiments_for_KGIN_baselines_algorithms.py --dataset amazonBook</code>  </li>
</ul>

<h5>IDSNR and baseline models</h5>
<ul>
<li>Run this command to reproduce the experiments for the IDS4NR_NCF and baseline models on the MovieLens dataset: <code>python run_experiments_IDS4NR_baselines_algorithms.py --dataset MovieLens --model NCF</code>  </li>

<li>Run this command to reproduce the experiments for the IDS4NR_NCF and baseline models on the Beauty dataset: <code>python run_experiments_IDS4NR_baselines_algorithms.py --dataset Beauty --model NCF</code>  </li>

<li>Run this command to reproduce the experiments for the IDS4NR_NCF and baseline models on the Music dataset: <code>python run_experiments_IDS4NR_baselines_algorithms.py --dataset Music --model NCF</code>  </li>

<li>Run this command to reproduce the experiments for the IDS4NR_LFM and baseline models on the MovieLens dataset: <code>python run_experiments_IDS4NR_baselines_algorithms.py --dataset MovieLens --model LFM</code>  </li>

<li>Run this command to reproduce the experiments for the IDS4NR_LFM and baseline models on the Beauty dataset: <code>python run_experiments_IDS4NR_baselines_algorithms.py --dataset Beauty --model LFM</code>  </li>

<li>Run this command to reproduce the experiments for the IDS4NR_LFM and baseline models on the Music dataset: <code>python run_experiments_IDS4NR_baselines_algorithms.py --dataset Music --model LFM</code>  </li>
</ul>
<h5>STAMP and baseline models</h5>
<ul>
<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Yoochoose</a> dataset, unzip it and put the “yoochoose-clicks.dat” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the STAMP and baseline models on the shorter version of the Yoochoose dataset: <code>python run_experiments_STAMP_And_baseline_models.py -m stamp_rsc -d rsc15_64 -n</code> and run the following command to create the experiments for the larger version of the Yoochoose dataset <code>python run_experiments_STAMP_And_baseline_models.py -m stamp_rsc -d rsc15_4 -n</code>  </li>
<li>Download <a href="https://www.dropbox.com/sh/n281js5mgsvao6s/AADQbYxSFVPCun5DfwtsSxeda?dl=0" target="_blank">Diginetica</a> dataset, unzip it and put the “train-item-views.csv” file into the “data” directory/folder. </li>
<li>Run this command to reproduce the experiments for the STAMP and baseline models on the Diginetica dataset: <code>python run_experiments_STAMP_And_baseline_models.py -m stamp_cikm -d digi -n</code></li> 
</ul>

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

