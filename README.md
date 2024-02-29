

<p align="center">
    <h4 align="center"><a href="https://library.imaging.org/ei/articles/36/17/AVM-115">📑 Article</a>  | <a href="https://drive.google.com/drive/folders/1JPb64bGV88ymZkJrUBaKQg12tToZVF7T?usp=sharing">📂 Dataset</a> | <a href="https://docs.google.com/presentation/d/1R7yt0BJVVkZIXfyz3MIcuNJkGIw8Z_Vk/edit#slide=id.p1">🎙️Talk</a>    </h4> 
</p>

## BEVSeg2TP: Surround View Camera Bird’s-Eye-View Based Joint Vehicle Segmentation and Ego Vehicle Trajectory Prediction




Abstrct: Trajectory prediction is, naturally, a key task for vehicle autonomy. While the number of traffic rules is limited, the combinations and uncertainties associated with each agent’s behaviour in real-world scenarios are nearly impossible to encode. Consequently, there is a growing interest in learning-based trajectory prediction. The proposed method in this paper predicts trajectories by considering perception and trajectory prediction as a unified system. In considering them as unified tasks, we show that there is the potential to improve the performance of perception. To achieve these goals, we present BEVSeg2TP - a surround-view camera bird’s-eye-view-based joint vehicle segmentation and ego vehicle trajectory prediction system for autonomous vehicles. The proposed system uses a network trained on multiple camera views. The images are transformed using several deep learning techniques to perform semantic segmentation of objects, including other vehicles, in the scene. The segmentation outputs are fused across the camera views to obtain a comprehensive representation of the surrounding vehicles from the bird’s-eye-view perspective. The system further predicts the future trajectory of the ego vehicle using a spatiotemporal probabilistic network (STPN) to optimize trajectory prediction. This network leverages information from encoder-decoder transformers and joint vehicle segmentation. The predicted trajectories are projected back to the ego vehicle’s bird’s-eye-view perspective to provide a holistic understanding of the surrounding traffic dynamics, thus achieving safe and effective driving for vehicle autonomy. The present study suggests that transformer-based models that use cross-attention information can improve the accuracy of trajectory prediction for autonomous driving perception systems. Our proposed method outperforms existing state-of-the-art approaches on the publicly available nuScenes dataset.

## Our Overview 📑
Our Overview: Segment anything model extracts bounding box info. GNN processes the graph for spatial feature relations, predicting ego vehicle trajectory with LSTM layers.


<img src="https://github.com/sharmasushil/BEVSeg2TP/assets/70905483/4ef70f3e-4440-49ca-801e-207aeccedb4e" width ="850">


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

