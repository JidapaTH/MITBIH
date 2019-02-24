# MITBIH

This project goal is to detect Premeture Ventricular Contraction (PVC) alarm from EKG signal.

A study conducted in 2014 (Drew and al.,  2014) during one month in UCSF’s Intensive Care Units revealed that heart arrhythmias accounted for half of the 2 million alarms, and that Premature Ventricular Contraction (PVC) represented 80% of heart arrhythmia alarms. In other words, one of every three alarms triggered in an ICU is for a PVC. Because of their prominence, building a better classifier of PVCs would have a larger impact on the alarm fatigue phenomenon.

Current patient monitoring devices can detect PVCs because of their unique characteristics. In a normal electrocardiogram, heartbeats are usually decomposed into 3 phases, each corresponding to a specific electrical polarization of the heart’s muscles that include: the P wave, QRS wave and T wave. These 3 phases are shown in Figure 1 as shown below :


<p align="center"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/SinusRhythmLabels.svg/280px-SinusRhythmLabels.svg.png"  width="40%" height="40%" ></p>
<p align="center">Figure 1: Regular heartbeat with P wave, QRS wave and T wave</p>



<p align="center"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/PVC10.JPG/300px-PVC10.JPG"  width="50%" height="50%" ></p>
<p align="center">Figure 2: PVC </p>

A PVC can be identified using the following symptoms:
- An early R-wave
- A wide QRS complex
- Absence of P-wave
- A Discordant T-wave
- A Compensatory Pause
 

PVCs are not only prominent and detectable, they are suspected to have negative effects on health. Even though they are not actionable, which means there is no means to stop them or cure them, a recent study (Lin and al., 2017) showed that PVCs are “associated with a higher incidence of all-cause mortality, cardiovascular hospitalization, all-cause hospitalization, and new-onset heart failure which was independent of other clinical risk factors”. For all these reasons, PVC is the primary subject of study for our team.

### Preprocessing

Use package biosppy to detect peak. 
<p align="center"> <img src="https://github.com/JidapaTH/MITBIH/blob/master/rpeak.png"  width="50%" height="50%" ></p>


To reduce noise wavelet transform have been used according to a result from Hari's paper (Hari et al, 2018). 
<p align="center"> <img src="https://github.com/JidapaTH/MITBIH/blob/master/wavelet.png"  width="50%" height="50%" ></p>


The wandering baseline is removed by moving average smoothing.
<p align="center"> <img src="https://github.com/JidapaTH/MITBIH/blob/master/rebase.png"  width="50%" height="50%" ></p>


#### Reference

Drew BJ, Harris P, Zègre-Hemsey JK, Mammone T, Schindler D, Salas-Boni R, et al. (2014) Insights into the Problem of Alarm Fatigue with Physiologic Monitor Devices: A Comprehensive Observational Study of Consecutive Intensive Care Unit Patients. PLoS ONE 9(10): e110274. https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0110274  

Hari Mohan Rai, Kalyan Chatterjee, A unique feature extraction using MRDWT for automatic classification of abnormal heartbeat from ECG big data with Multilayered Probabilistic Neural Network classifier, Applied Soft Computing, Volume 72, 2018, Pages 596-608, ISSN 1568-4946, https://doi.org/10.1016/j.asoc.2018.04.005. (http://www.sciencedirect.com/science/article/pii/S156849461830190X)

Lin CY, Chang SL, Lin YJ, et al. An observational study on the effect of premature ventricular complex burden on long-term outcome. Medicine (Baltimore). 2017;96(1):e5476.

Biosppy package
https://biosppy.readthedocs.io/en/stable/biosppy.signals.html#biosppy-signals-ecg

