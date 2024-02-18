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
├── requirement.txt                               # File containing the list of Python packages the project uses
├── R                                             # 
│   ├── measurement.R                             # R script for measurement data preprocessing, including ACH calculation & thermal conductance cal & EPW weather file generation
│   ├── uncertainty.R                             # R script for measurement uncertainty analysis
│   ├── baseline_idfs.Rmd                         # R script for baseline EnergyPlus model development by incorporating different levels of information 
│   ├── model_accuracy_validation.R               # R script for validating the predictive accuracy of Models 1 to 6 against measured data
│   └── ECM_sim.R                                 # R script for ECM analysis using parametric simulations
|   └── model_evaluation.R                        # R script for model predictive performance evaluation and result visualization
├── data                                          # 
│   ├── csv                                       # Dataset summarizing papers reviewed
│   │   ├── sf6.csv                               # SF6 concentration measurements
│   │   ├── heat_flux.csv                         # Heat-flux sensor measurements
│   │   ├── pi_data.csv                           # Energy Management System data and logged data set during the experiment period
│   │   └── experiment_schedule.csv               # Experiment schedule
│   └── idf                                       # 
│       ├── epwfiles                              # EnergyPlus weather files
│       │   └── ...                               # 
│       ├── iddfiles                              # IDD files
│       │   └── ...                               # 
│       └── idffiles                              # Baseline IDFs
│           └── ...                               #                               
└── paper                                         # 
    ├── figures                                   # Figures used in the paper
    │   └── ...                                   #
    ├── tex                                       # LaTeX source document
    └── bib                                       # Bibliographic information file 
```

*Due to size limitations for data files on GitHub, please download the LULC data '1m_GridPoints_distTo_and_zones_3414.csv' from the provided external link*: <https://drive.google.com/file/d/1-8naDeGk_qNFP4aJ6ghtJGrHYwGkwMQi/view?usp=drive_link>

## Approach

This study performs occupancy prediction based on a minimum sensing strategy by using a comprehensive set of sensor data (i.e., indoor environmental and outdoor weather conditions, Wi-Fi connected devices, energy consumption data, HVAC operations, and time-related information) to identify the most crucial features through a proposed feature selection algorithm. Occupancy predictions were subsequently performed using different deep learning architectures, including Deep Neural Network (DNN), Long Short-Term Memory (LSTM), Bi-directional LSTM (Bi-LSTM), Gated Recurrent Unit (GRU), and Bi-directional GRU (Bi-GRU) in an office, library, and lecture room. Our findings highlighted that the proposed feature selection algorithm outperformed a popular feature selection algorithm to achieve a higher model performance with lower sensing requirements. Furthermore, empirical results showed that indoor $CO_2$ levels and Wi-Fi connected devices were crucial features for predicting occupancy across all space types. The best model performances were achieved using Bi-GRU for office, GRU for library, and Bi-GRU for lecture room.


## Licenses


