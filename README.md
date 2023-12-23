# Millisecond qXRR data pipeline and Neural Network analysis 

This GitHub repository showcases a comprehensive data pipeline for extracting X-ray reflectivity (XRR) signals from a rotating sample, along with the implementation of a Feedforward Neural Network for the analysis of XRR data collected during a spin-coating procedure.   

### Data pipeline

The data pipeline presented in this repository is designed to extract X-ray reflectivity signals from a rotating sample. The raw data is acquired from a 2D pixel detector (Eiger2 X 1M), and all necessary normalizations are seamlessly integrated into the script ('Gold/reader.ipynb'). These normalizations include footprint correction from the rotating sample, absorber normalization, and residence dwell time normalization along the curved shape of the beam on the detector. The provided example data demonstrates the process during the rotation of a gold-coated silicon wafer. A sample holder with a wedge-shaped design, featuring a stepness of 1 degree, is affixed atop the spin coater.   

### NN for spin-coated films

For the analysis of data obtained from spin-coating experiments, we leverage mlreflect (Greco et al., 2022), a Feedforward Neural Network algorithm. This approach is chosen for its convenience and speed compared to advanced genetic algorithms, particularly when dealing with a large dataset of 10,000 curves generated during the spin-coating procedure.

The notebook 'ml_reflect.ipynb' encompasses the generation of training data, training of the Neural Network, and fitting of the entire spin-coating run (located in the "data" folder).

The notebook 'ml_single.ipynb' focuses on the analysis of a spin-coating run (also in the "data" folder) within a shorter time scale. It reveals the exponential decay of thickness at the beginning of the spin-coating procedure.

If you have any questions or suggestions, please don't hesitate to reach out.

