# Sleep-Disorders-Datasets

## [Apnea-ECG Database](https://physionet.org/content/apnea-ecg/1.0.0/)
Published: Feb. 10, 2000. Version: 1.0.0

The Apnea-ECG Database was designed to support the development of automated methods for detecting sleep apnea events, with a primary focus on ECG signals.

- 70 ECG records from 7 hours to 10 hours
- 16 bits per sample, least significant byte first in each pair, 100 samples per second, nominally 200 A/D units per millivolt
- Apnea annotations (derived by human experts on the basis of simultaneously recorded respiration and related signals), every minute indicating the presence or absence of apnea at that time
- Machine-generated QRS annotations (in which all beats regardless of type have been labeled normal) made using sqrs125. 
- Records a01 through a04, b01, and c01 through c03 are accompanied by additional signals: chest and abdominal respiratory effort signals obtained using inductance plethysmography (Resp C and Resp A), oronasal airflow measured using nasal thermistors (Resp, N), and oxygen saturation (SpO2).
- Subjects info (**LINK FILE**)

### Files

| File Type | Description                                                                         |
| ---       | ---                                                                                 |
| .dat      | Digitized Signals                                                                   | 
| .hea      | Text header files that specify the names and formats of the associated signal files |
| .apn      | Binary annotation files of apnea events                                             |
| .qrs      | Binary annotation files of the QRS complex                                          |
| .xws      | WAVE files for vizualising each record on Linux                                     |

### Records

| Name    | Description                                                             | Set          |
| ---     | ---                                                                     | ---          |
| a01-a20 | Apnea: 100 or more minutes with disordered breathing                    | Learning Set |
| b01-b05 | Boderline Apnea: Some apneas of uncertain importance (10 to 90 minutes) | Learning Set |
| c01-c10 | Control: Less than 5 min with disordered breathing                      | Learning Set |
| x01-x35 | No distinction made                                                     | Test Set     |

### Notes
- "In April 2013, Chiu-wen Wu reported that training set control records c05 and c06 come from the same original recording (c05 begins 80 seconds later than c06). The slightly different descriptions of these records in additional-information.txt suggest that c06 may have been a corrected version of c05.". [From Apnea-ECG Database site](https://physionet.org/content/apnea-ecg/1.0.0/)
- .qrs files are unaudited and contain errors.
- Several studies reported that the signals fro the database are raw signals, so artifact removal techiques were used to remove noise, such as noise from movement during sleep [(Li et al., 2024)](10.1109/TIM.2024.3440369), [(Krithika et al., 2024)](10.1109/ICIC3S61846.2024.106030499), [(Jiao et al., 2024)](10.1109/OJEMB.2024.3405666), [(Wei et al., 2024)](10.1109/IMCEC59810.2024.10575752).




## [CAP Sleep Database](https://physionet.org/content/capslpdb/1.0.0/)
Published: July 26, 2012. Version: 1.0.0

The Cyclic Alternating Pattern (CAP) is a periodic EEG activity that occursg during NREM sleep, characterized by two phase: A-phase (A1, A2 or A3) and B-phase). CAP is a marker of sleep instability and can be correlated with several sleep disorders. The CAP Sleep database provides a diverse set of recordings collected at the Sleep Disorders Center of the Ospedale Maggiore of Parma in Italy. The records include CAP annotations supporting the development and evaluation of automated CAP detection algorithms, as well as studies on the dynamics of CAP. Although the primary purpose of the CAP Sleep database is CAP analysis, the CAP sleep database could also be used for the development of sleep stage automatic detection algorithms and sleep disorders detecntion algorithms. However, for the latter the set would be really unbanlced.

- 108 polysomnographic records
- Records include multiple pre-filtered biosignals: at least 3 EEG channels (F3 or F4, C3 or C4 and O1 or O2, referred to A1 or A2) and EOG (2 channels), EMG of the submentalis muscle, bilateral anterior tibial EMG, respiration signals (airflow, abdominal and thoracic effort, and SaO2) and ECG.
- Some records may have additional EEG traces (Fp1-F3, F3-C3, C3-P3, P3-O1 and/or Fp2-F4, F4-C4, C4-P4, P4-O2)
- Sampling rate varies between and within signals
- Subject info [**Link**]

### Files
 
| File Type | Description                                                                            |
| ---       | ---                                                                                    |
| .edf      | Digitized Signals in European Data format                                              | 
| .txt      | Annotation files                                                                       |
| .st       | Annotation for PhysioBank ATM or other software that reads PhysioBank-compatible files |
| .m        | Matlab files for CAP scoring CAP parameters computation                                |
| .xlsx     | Spreadsheet file with gender and age information                                       |

### Records

| Name          | Description                     | 
| ---           | ---                             |
| n1-n16        | Controls (no neurological disorders and free of drugs affecting CNS |
| brux1-brux2   | Bruxism                         |
| ins1-ins9     | Insomnia                        |
| narco1-narco5 | Narcolepsy                      |
| nfle1-nfle40  | Nocturnal frontal lobe epilepsy |
| plm1-plm10	   | Periodic leg movements          |
| rbd1-rbd22    | REM behavior disorder           |
| sdb1-sdb4     | Sleep-disordered breathing      |


### Annotations

Sleep macrostructure was scored according to the Rechtschaffen & Kales rules, while the CAP was detected in agreement with Terzano’s reference atlas of rules.

| Type         | Description                                               |
| ---          | ---                                                       |
|Sleep stage   | W=wake, S1-S4=sleep stages, R=REM, MT=body movements      |
|Body position | Left, Right, Prone, or Supine                             |
|Time of day   | [hh:mm:ss]                                                |
|Event         | sleep stage (SLEEP-S0..S4, REM, MT), or a phase A of CAP) |
|Duration      | in seconds                                                |
|Location      | the signal(s) in which the event can be observed          |

### Notes
- Body position was not recorded in some subjects
- Not all subjects have all of the mentioned signals recorded
- A-phase annotations include distintion of waht subtype it is (A1, A2, A3)
- Though the signals are pre-filtered some studies still employed some kind of filtering [(Sheng-Hsiou et al. 2018)](https://www.sciencedirect.com/science/article/pii/S1053811918306888), [(Yan et al. 2019)](https://www.sciencedirect.com/science/article/pii/S1746809418302647), [(Sharma et al. 2023)](https://www.sciencedirect.com/science/article/pii/S0010482523007242#b36), [(Agarwal et al. 2024)](https://www.sciencedirect.com/science/article/pii/S1389945724004465).




## [St. Vincent's University Hospital / University College Dublin Sleep Apnea Database](https://physionet.org/content/apnea-ecg/1.0.0/)
Published: Oct. 9, 2007. Version: 1.0.0 (revised on 1 September 2011)

This database contains 25 full overnight polysomnograms with simultaneous three-channel Holter ECG, from adult subjects with suspected sleep-disordered breathing.

St. Vincent's University Hospital Sleep Disorders Clinic

- 25 polysomnography records (Jaeger-Toennies system) acompained by Three-channel holter ECGs (Reynolds Lifecard CF system)
- PSG records include EEG (C3-A2), EEG (C4-A1), left EOG, right EOG, submental EMG, ECG (modified lead V2), oro-nasal airflow (thermistor), ribcage movements, abdomen movements (uncalibrated strain gauges), oxygen saturation (finger pulse oximeter), snoring (tracheal microphone) and body position.
- Holter records include ECG (V5, CC5, V5R)

- [**Sampling frequency**]
- Subject info [**Link**]

### Files
 
| File Type | Description                                                                            |
| ---       | ---                                                                                    |
| .edf      | Digitized Holter Signals in European Data format                                       |
| .rec      | Digitized Polysonography Signals in European Data format                               | 
| .txt      | Annotation files                                                                       |
| .st       | Annotation for PhysioBank ATM or other software that reads PhysioBank-compatible files |
| .m        | Matlab files for CAP scoring CAP parameters computation                                |
| .xlsx     | Spreadsheet file with gender and age information                                       |

### Records

| Name          | Description                     | 
| ---           | ---                             |
| n1-n16        | Controls (no neurological disorders and free of drugs affecting CNS |
| brux1-brux2   | Bruxism                         |
| ins1-ins9     | Insomnia                        |
| narco1-narco5 | Narcolepsy                      |
| nfle1-nfle40  | Nocturnal frontal lobe epilepsy |
| plm1-plm10	   | Periodic leg movements          |
| rbd1-rbd22    | REM behavior disorder           |
| sdb1-sdb4     | Sleep-disordered breathing      |


### Annotations

Sleep stages were scored by an experienced sleep technologist according to the Rechtschaffen & Kales rules. Onset time and duration of respiratory events were annotated by the same sleep technologist.

| Type               | Description                                                       |
| ---                | ---                                                               |
| Sleep stage        | 0: wake, 1: REM, 2-5: sleep stages, 6: artifact, 7: indeterminate |
| Respiratory events | HYP: Hypopnea, C: Central, O: Obstructive, M: Mixed               |
| Duration           | Duration of respiratory event in seconds                          |
| Time of day        | [hh:mm:ss]                                                        |
| Snore              | Not present: -, Present: +                                        |
| Arousal            | Not present: -, Present: +                                        |
| PB/CS              | Periodic breathing/Cheynes-Stokes                                 |
| B/T                | Bradycardia/Tachycardia rare and change                           |


### Notes
-  The recording dates and times are not available
-  In record ucddb002, only two distinct ECG signals were recorded; the second ECG signal was also used as the third signal.


Subjects
Subjects were randomly selected over a 6-month period (September 02 to February 03) from patients referred to the Sleep Disorders Clinic at St Vincent's University Hospital, Dublin, for possible diagnosis of obstructive sleep apnea, central sleep apnea or primary snoring. Subjects had to be above 18 years of age, with no known cardiac disease, autonomic dysfunction, and not on medication known to interfere with heart rate. Twenty-five subjects (21M, 4F) were selected (age: 50 ± 10 years, range 28-68 years; BMI: 31.6 ± 4.0 kg/m², range 25.1-42.5 kg/m²; AHI: 24.1 ± 20.3, range 1.7-90.9). Details are shown in SubjectDetails.xls.)












