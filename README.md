# SRECG 1.0
Abstract: A combination of cloud-based deep learning (DL) algorithms with portable/wearable (P/W) devices has been developed as a smart heath care system to support automatic cardiac arrhythmias (CAs) classification using electrocardiography (ECG). However, long-term and continuous ECG monitoring is challenging because of limitations of batteries and transmission bandwidth of P/W devices while incorporated with consumer electronics (CE). A feasible approach to address this challenge is to decrease sampling rates. However, low sampling rates lead to low-resolution signals that hinder the CAs classification performance. In this study, we propose a DL-based ECG signal super-resolution framework (called SRECG) to enhance low-resolution ECG signals by jointly considering the accuracies when applied to the DL-based high-resolution multiclass classifier (HMC) of CAs. In our experiments, we downsampled the ECG signals from the CPSC2018 dataset and evaluated their HMC accuracies with and without the SRECG. Experimental results show that SRECG can well improve the HMC accuracies as compared to traditional interpolation methods. Moreover, approximately half of the CAs classification accuracies of HMC were maintained within the enhanced ECG signals by SRECG. The promising results confirm that SRECG can be suitably used to enhance low-resolution ECG signals from P/W devices with CE to improve their cloud-based HMC performances.

Authors: Tsai-Min Chen (1 and 2), Yuan-Hong Tsai (3 and 4), Huan-Hsin Tseng (2), Kai-Chun Liu (2), Jhih-Yu Chen (5), Chih-Han Huang (6), Guo-Yuan Li (3 and 4), Chun-Yen Shen (1 and 7), Yu Tsao (1 and 2) ((1) Graduate Program of Data Science, National Taiwan University and Academia Sinica, Taipei, Taiwan, (2) Research Center for Information Technology Innovation, Academia Sinica, Taipei, Taiwan, (3) Program of Taiwan AI Academy, Taiwan Artificial Intelligence Academy Foundation, New Taipei, Taiwan, (4) Technology Development Center, Artificial Intelligence Foundation, New Taipei, Taiwan, (5) Graduate Institute of Biomedical Electronics and Bioinformatics, National Taiwan University, Taipei, Taiwan, (6) Institute of Biomedical Sciences, Academia Sinica, Taipei, Taiwan, (7) Department of Mathematics, National Taiwan University, Taipei, Taiwan)

training, validation, and testing code: SRECG.ipynb

testing analysis folder: comparison

reference papers: 
1. https://ieeexplore.ieee.org/document/10018428/
2. https://arxiv.org/abs/2012.03803/
3. https://doi.org/10.1016/j.isci.2020.100886
