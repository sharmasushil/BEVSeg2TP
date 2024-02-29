## BEVSeg2TP: Surround View Camera Bird’s-Eye-View Based Joint Vehicle Segmentation and Ego Vehicle Trajectory Prediction

# Code will release soon 

☞ To delve deeper into our findings and gain a more comprehensive understanding of our results, we invite you to explore the additional insights presented in our video.  
You can access the video by following this link: 🎬 https://youtu.be/FNBMEUbM3r8

<p align="center">
    <h4 align="center"><a href="https://library.imaging.org/ei/articles/36/17/AVM-115">📑 Article</a>  | <a href="https://drive.google.com/drive/folders/1JPb64bGV88ymZkJrUBaKQg12tToZVF7T?usp=sharing">📂 Dataset</a> | <a href="https://docs.google.com/presentation/d/1R7yt0BJVVkZIXfyz3MIcuNJkGIw8Z_Vk/edit#slide=id.p1">🎙️Talk</a>    </h4> 
</p>

# Optimizing Ego Vehicle Trajectory Prediction: The Graph Enhancement Approach 🚗

Abstract:Predicting the trajectory of an ego vehicle is a critical component of autonomous driving systems. Current state-of-the-art methods typically rely on Deep Neural Networks (DNNs) and sequential models to process front-view images for future trajectory prediction. However, these approaches often struggle with perspective issues affecting object features in the scene. To address this, we advocate for the use of Bird’s Eye View (BEV) perspectives, which offer unique advantages in capturing spatial relationships and object homogeneity. In our work, we leverage Graph Neural Networks (GNNs) and positional encoding to represent objects in a BEV, achieving competitive performance compared to traditional DNN-based methods. While the BEV-based approach loses some detailed information inherent to front-view images, we balance this by enriching the BEV data by representing it as a graph where relationships between the objects in a scene are captured effectively.

## Our Overview 📑
Our Overview: Segment anything model extracts bounding box info. GNN processes the graph for spatial feature relations, predicting ego vehicle trajectory with LSTM layers.

<img src="https://github.com/sharmasushil/Optimizing-Ego-Vehicle-Trajectory-Prediction-The-Graph-Enhancement-Approach/assets/70905483/ad96c3e6-42d0-4553-8aea-fbcfac442e37" width ="650">


## Our proposed architecture ⛓️
Semantic segmentation derives bounding box coordinates and mask details from a BEV, this information is then utilized by a DNN to inform a KNN, which establishes connections between the boxes to create a graph. A GNN, enhanced with positional encoding, captures spatial features, while LSTM layers integrate temporal dynamics for the prediction of the ego vehicle’s trajectory.

<img src="https://github.com/sharmasushil/Optimizing-Ego-Vehicle-Trajectory-Prediction-The-Graph-Enhancement-Approach/assets/70905483/140fda00-482d-448f-bc57-663990356165" width = "650">

## CARLA Results Visualization 📈

Qualitative results: Left depicts a random frame from the Carla simulation, and the middle illustrates the GNN graph structure
with nodes and edges. On the right, the predicted trajectory of the ego vehicle is plotted over a 5-step horizon, where the starting step is
marked in blue, and the predicted trajectory is represented in red.


<img src="https://github.com/sharmasushil/Optimizing-Ego-Vehicle-Trajectory-Prediction-The-Graph-Enhancement-Approach/assets/70905483/b97c4dc1-cfe0-400d-a285-cc26e894ab6b" width ="650">

## Citation 👇🏻
If you use this dataset in your research or work, we kindly request that you cite the following paper:

```BibTeX
@inproceedings{sharma2024,
      title={Optimizing Ego Vehicle Trajectory Prediction: The Graph Enhancement Approach}, 
      author={Sushil Sharma, Aryan Singh, Ganesh Sistu, Mark Halton, Ciarán Eising},
      year={2024},
      booktitle={Electronic Imaging,2024,pp 115-1 - 115-6,https://doi.org/10.2352/EI.2024.36.17.AVM-115,
      San Francisco, California, USA}
}
```

