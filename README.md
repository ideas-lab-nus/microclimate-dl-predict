# Microclimate spatio-temporal prediction using deep learning and land use data
This repository contains the research compendium of our latest work, "Microclimate spatio-temporal prediction using deep learning and land use data." This study proposes a novel approach to predict microclimate: the Geo-LSTM-Kriging model, which is applicable for fine-scale microclimate prediction within a few hundred meters around weather stations. 

The compendium includes all the data and code needed to reproduce the analysis. More details can be found in our paper:

> xxx, xxx, xxx, xxx and xxx, (2024).
> *Microclimate spatio-temporal prediction using deep learning and land use data*.
> *Building and Environment*. <https://doi.org/xxx/xxx>

## Citation

If you are interested in using this code in your research, please cite our paper:
```
@article{2024microclimate,
  title={Microclimate spatio-temporal prediction using deep learning and land use data},
  author={xxx},
  year={2024},
  note={In Revision}
}
```

## Repository Structure

```
./
├── python                                        # 
│   ├── requirement.txt                           # File containing the list of Python packages the project uses
│   ├── Model_train.ipynb                         # Python notebook for constructing and training the models used in study
│   ├── Model_evaluation_and_plot.ipynb           # Python notebook for validating the predictive error of models and plot the validation results
│   └── trainednw                                 # Folder to save trained network parameters
│       └── ...                                   #
├── data                                          # 
│   ├──GridPoints_TreesAndStreets_3414.csv        # LULC data of trees and streets
│   ├──WSPoints_TreesAndStreets_3414.csv          # LULC data of weather stations
│   ├──RH0719.csv                                 # RH data of weather stations in 2019/07
│   ├──RH0819.csv                                 # RH data of weather stations in 2019/08
│   ├──Tem0719.csv                                # Temperature data of weather stations in 2019/07
│   ├──Tem0819.csv                                # Temperature data of weather stations in 2019/08
│   ├──sr0719.csv                                 # Solar radiation data of weather stations in 2019/07
│   └──ws0719.csv                                 # Wind speed data of weather stations in 2019/07 
├── src                                           # sources used in README.md
└── paper                                         # 
    ├── figures                                   # Figures used in the paper
    │   └── ...                                   #
    ├── main.tex                                  # LaTeX source document
    └── cas-refs.bib                              # Bibliographic information file 
```

*Due to size limitations for data files on GitHub, please download the LULC data '1m_GridPoints_distTo_and_zones_3414.csv' from the provided external link*: <https://drive.google.com/file/d/1-8naDeGk_qNFP4aJ6ghtJGrHYwGkwMQi/view?usp=drive_link>

## Approach

This study performs occupancy prediction based on a minimum sensing strategy by using a comprehensive set of sensor data (i.e., indoor environmental and outdoor weather conditions, Wi-Fi connected devices, energy consumption data, HVAC operations, and time-related information) to identify the most crucial features through a proposed feature selection algorithm. Occupancy predictions were subsequently performed using different deep learning architectures, including Deep Neural Network (DNN), Long Short-Term Memory (LSTM), Bi-directional LSTM (Bi-LSTM), Gated Recurrent Unit (GRU), and Bi-directional GRU (Bi-GRU) in an office, library, and lecture room. Our findings highlighted that the proposed feature selection algorithm outperformed a popular feature selection algorithm to achieve a higher model performance with lower sensing requirements. Furthermore, empirical results showed that indoor $CO_2$ levels and Wi-Fi connected devices were crucial features for predicting occupancy across all space types. The best model performances were achieved using Bi-GRU for office, GRU for library, and Bi-GRU for lecture room.


## Licenses


