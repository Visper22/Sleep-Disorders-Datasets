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

### File Format

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

### Notes:
- "In April 2013, Chiu-wen Wu reported that training set control records c05 and c06 come from the same original recording (c05 begins 80 seconds later than c06). The slightly different descriptions of these records in additional-information.txt suggest that c06 may have been a corrected version of c05.". [From Apnea-ECG Database site](https://physionet.org/content/apnea-ecg/1.0.0/)
- .qrs files are unaudited and contain errors.
- Several studies reported that the signals fro the database are raw signals, so artifact removal techiques were used to remove noise, such as noise from movement during sleep [(Li et al., 2024)](10.1109/TIM.2024.3440369), [(Krithika et al., 2024)](10.1109/ICIC3S61846.2024.106030499), [(Jiao et al., 2024)](10.1109/OJEMB.2024.3405666), [(Wei et al., 2024)](10.1109/IMCEC59810.2024.10575752).




## [CAP Sleep Database]([https://physionet.org/content/apnea-ecg/1.0.0/](https://physionet.org/content/capslpdb/1.0.0/))
Published: July 26, 2012. Version: 1.0.0

The Cyclic Alternating Pattern (CAP) is a periodic EEG activity occurring during NREM sleep. It is characterized by cyclic sequences of cerebral activation (phase A) followed by periods of deactivation (phase B) which separate two successive phase A periods with an interval <1 min. Phase A periods are subdivided into three subtypes. Despite being a physiological phenomenon, CAP is also a marker of sleep instability and can be correlated with several sleep-related pathologies. In fact, on one hand CAP can reflect a reaction of the sleeping brain to any endogenous or exogenous disturbance; on the other hand, the A phase of CAP has been interpreted as a kind of gate through which pathological events more easily occur [3].

This database is intended to provide a useful number of carefully annotated examples of CAP in a representative variety of pathophysiologic contexts, for development and evaluation of automated CAP analyzers, as well as to support basic studies of the dynamics of CAP.

Several efforts have been made to develop a reliable automatic CAP-scoring algorithm [11]. Most of these methods rely on the extraction of spectral features from the EEG and on the application of machine-learning algorithms. Although all these methods achieve good results, none of them is yet applied to clinical practice since they either require some amount of clinician intervention or do not achieve a sufficient accuracy in the classification to support the clinical diagnosis. Some recordings from this database have been used for studies on features related to CAP phase A [12-16] and for training automatic CAP detection algorithms [17].
  

- 108 polysomnographic recordings registered at the Sleep Disorders Center of the Ospedale Maggiore of Parma, Italy.
- Records include least 3 EEG channels (F3 or F4, C3 or C4 and O1 or O2, referred to A1 or A2), EOG (2 channels), EMG of the submentalis muscle, bilateral anterior tibial EMG, respiration signals (airflow, abdominal and thoracic effort and SaO2) and ECG.
- Additional traces include EEG bipolar traces, according to the 10-20 international system (Fp1-F3, F3-C3, C3-P3, P3-O1 and/or Fp2-F4, F4-C4, C4-P4, P4-O2).
- The 16 healthy subjects included in the study did not present any neurological disorders and were free of drugs affecting the central nervous system.
- Subject info

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
| n1-n16        | Controls                        |
| brux1-brux2   | Bruxism                         |
| ins1-ins9     | Insomnia                        |
| narco1-narco5 | Narcolepsy                      |
| nfle1-nfle40  | Nocturnal frontal lobe epilepsy |
| plm1-plm10	  | Periodic leg movements          |
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

### Notes:
- Body position was not recorded in some subjects
- Not all subjects have all of the mentioned signals recorded







