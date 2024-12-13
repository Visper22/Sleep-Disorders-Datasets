# Sleep-Disorders-Datasets

| Dataset/Database | Signals | Signal Properties | Annotations | Population | Applications |
| --- | --- | --- | --- | --- | --- |
| [Apnea-ECG Database](##[Apnea-ECG Database](https://physionet.org/content/apnea-ecg/1.0.0/)) | Signals | Signal Properties | Annotations | Population | Applications |
| Dataset/Database | Signals | Signal Properties | Annotations | Population | Applications |
| Dataset/Database | Signals | Signal Properties | Annotations | Population | Applications |
| Dataset/Database | Signals | Signal Properties | Annotations | Population | Applications |
| Dataset/Database | Signals | Signal Properties | Annotations | Population | Applications |
| Dataset/Database | Signals | Signal Properties | Annotations | Population | Applications |
| Dataset/Database | Signals | Signal Properties | Annotations | Population | Applications |
| Dataset/Database | Signals | Signal Properties | Annotations | Population | Applications |
| Dataset/Database | Signals | Signal Properties | Annotations | Population | Applications |


## [Apnea-ECG Database](https://physionet.org/content/apnea-ecg/1.0.0/)
*Published: Feb. 10, 2000. Version: 1.0.0*

The Apnea-ECG Datababe was design to support the development of automated methods for detecting sleep apnea events, emphasizing the use of ECG signals. So, it has been many employed in various studies for the detection of sleep apnea events [(Fatimah et al. 2020)](https://doi.org/10.1016/j.bspc.2020.102005), [(Mashrur et al. 2021)](https://doi.org/10.1016/j.compbiomed.2021.104532), [(Yang et al. 2022)](https://doi.org/10.1016/j.compbiomed.2021.105124), [(Wei et al., 2024)](https://doi.org/10.1109/IMCEC59810.2024.10575752), [(Li et al., 2024)](https://doi.org/10.1109/TIM.2024.3440369) [(Hou et al. 2025)](https://doi.org/10.1016/j.cmpb.2024.108558) but also, for subject-level sleep apnea classification [(Jiao et al., 2024)](https://doi.org/10.1109/OJEMB.2024.3405666).

- 70 ECG records from 7 hours to 10 hours
- 16 bits per sample, least significant byte first in each pair, 100 samples per second, nominally 200 A/D units per millivolt
- Records a01 through a04, b01, and c01 through c03 are accompanied by additional signals: chest and abdominal respiratory effort signals obtained using inductance plethysmography (Resp C and Resp A), oronasal airflow measured using nasal thermistors (Resp N), and oxygen saturation (SpO2).

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

### Annotations

Apnea annotations (derived by human experts on the basis of simultaneously recorded respiration and related signals), every minute. Machine-generated QRS annotations (in which all beats regardless of type have been labeled normal) made using sqrs125.

| Type          | Description                                               |
| ---           | ---                                                       |
| Apnea Event   | N: Normal, A: Apnea                                       |
| Qrs complex   | N: R-peak                                                 |

### Notes
- "In April 2013, Chiu-wen Wu reported that training set control records c05 and c06 come from the same original recording (c05 begins 80 seconds later than c06). c06 may have been a corrected version of c05.". [From Apnea-ECG DB site](https://physionet.org/content/apnea-ecg/1.0.0/)
- .qrs files are unaudited and contain errors. [From Apnea-ECG DB site](https://physionet.org/content/apnea-ecg/1.0.0/)
- Some ECG recordings (a10, a12, a19, b05, c01, c04, c07, c09, and x17) are reversed [(Yang et al. 2022)](https://doi.org/10.1016/j.compbiomed.2021.105124).
- Several studies reported that the signals from the database are raw signals, so artifact removal techiques were used to remove noise, such as noise from movement during sleep [(Li et al., 2024)](https://doi.org/10.1109/TIM.2024.3440369), [(Jiao et al., 2024)](https://doi.org/10.1109/OJEMB.2024.3405666), [(Wei et al., 2024)](https://doi.org/10.1109/IMCEC59810.2024.10575752), [(Mashrur et al. 2021)](https://doi.org/10.1016/j.compbiomed.2021.104532).
- [(Travieso et al.)](https://doi.org/10.1016/j.neucom.2013.04.048) evaluated the quality of the ECG signals following pre-defined characteristics and "after discarding the affected segments, the recordings are reduced to a 54.76% of its duration in the worst case and 89.09% in the best case, per patient. The mean extracted length of the database recordings is 76.94%.". They employ this process of discarding the noisy or low quality segments instead of applying typical filtering techniques.




## [CAP Sleep Database](https://physionet.org/content/capslpdb/1.0.0/)
*Published: July 26, 2012. Version: 1.0.0*

The Cyclic Alternating Pattern (CAP) is a periodic EEG activity that occursg during NREM sleep, characterized by two phase: A-phase (A1, A2 or A3) and B-phase). CAP is a marker of sleep instability and can be correlated with several sleep disorders. The CAP Sleep database provides a diverse set of recordings collected at the Sleep Disorders Center of the Ospedale Maggiore of Parma in Italy. The records include CAP annotations supporting the development and evaluation of automated CAP detection algorithms, as well as studies on the dynamics of CAP. Although the primary purpose of the CAP Sleep database is for CAP automatic detection [(Sharma et al. 2023)](https://doi.org/10.1016/j.compbiomed.2023.107259), [(Agarwal et al. 2024)](https://doi.org/10.1016/j.sleep.2024.09.025), the CAP sleep database has also been used for the development of sleep stage automatic scoring algorithms [(Yan et al. 2019)](https://doi.org/10.1016/j.bspc.2018.10.001), [(Zhao et al. 2024)](https://doi.org/10.1016/j.bspc.2023.105615) and sleep disorders automatic classification algorithms [(Sharma et al. 2024)](http://dx.doi.org/10.1007/s10489-024-05284-6). However, for the latter the set would be really unbanlanced.

- 108 polysomnographic records
- Records include multiple pre-filtered biosignals: at least 3 EEG channels (F3 or F4, C3 or C4 and O1 or O2, referred to A1 or A2) and EOG (2 channels), EMG of the submentalis muscle, bilateral anterior tibial EMG, respiration signals (airflow, abdominal and thoracic effort, and SaO2) and ECG.
- Some records may have additional EEG traces (Fp1-F3, F3-C3, C3-P3, P3-O1 and/or Fp2-F4, F4-C4, C4-P4, P4-O2)
- Sampling rate varies between and within signals

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
| n1-n16        | Controls (no neurological disorders and free of drugs affecting CNS) |
| brux1-brux2   | Bruxism                         |
| ins1-ins9     | Insomnia                        |
| narco1-narco5 | Narcolepsy                      |
| nfle1-nfle40  | Nocturnal frontal lobe epilepsy |
| plm1-plm10	   | Periodic leg movements          |
| rbd1-rbd22    | REM behavior disorder           |
| sdb1-sdb4     | Sleep-disordered breathing      |


### Annotations

Sleep macrostructure was scored according to the Rechtschaffen & Kales rules, while the CAP was detected in agreement with Terzano’s reference atlas of rules.

| Type          | Description                                               |
| ---           | ---                                                       |
| Sleep stage   | W: wake, S1-S4: sleep stages, R: REM, MT: body movements  |
| Body position | Left, Right, Prone, or Supine                             |
| Time of day   | [hh:mm:ss]                                                |
| Event         | sleep stage (SLEEP-S0..S4, REM, MT), or a phase A of CAP) |
| Duration      | in seconds                                                |
| Location      | the signal(s) in which the event can be observed          |

### Notes
- Body position was not recorded in some subjects
- Not all subjects have all of the mentioned signals recorded
- A-phase annotations include distintion of waht subtype it is (A1, A2, A3)
- Though the signals are pre-filtered some studies still employed some kind of filtering [(Sheng-Hsu et al. 2018)](https://doi.org/10.1016/j.neuroimage.2018.08.001), [(Yan et al. 2019)](https://doi.org/10.1016/j.bspc.2018.10.001), [(Sharma et al. 2023)](https://doi.org/10.1016/j.compbiomed.2023.107259), [(Agarwal et al. 2024)](https://doi.org/10.1016/j.sleep.2024.09.025).
- Not clear about ECG lead positioning
- Channel names are inconsistent




## [St. Vincent's University Hospital / University College Dublin Sleep Apnea Database](https://physionet.org/content/ucddb/1.0.0/)
*Published: Oct. 9, 2007. Version: 1.0.0 (revised on 1 September 2011)*

The database contains overnight polysomnograms and simultaneous three-channel Holter ECG recordings from adults with suspected sleep-disordered breathing, collected at St. Vincent's University Hospital Sleep Disorders Clinic from September 2002 to February 2003. It can be used for multiple porposes, such as sleep stage classification and sleep apnea event detection. Studies have been made on sleep/wake classification [(Geng et al 2022)](https://doi.org/10.1016/j.bspc.2021.103132) and sleep stage classification [(Abdulla et al. 2023)](https://doi.org/10.1016/j.ijmedinf.2023.105001). For sleep apnea events detection some studies detect sleep apnea events,  regardless of type [(Fatimah et al. 2020)](https://doi.org/10.1016/j.bspc.2020.102005), [(Cai et al. 2025)](https://doi.org/10.1016/j.bspc.2024.106993), while others focus on specific events detection, such as obstructive sleep apnea event detection [(Taghizadegan et al. 2021)](https://doi.org/10.1016/j.mehy.2021.110659), and multiple sleep apnea events detection (Hypopnea, Central, Obstructive,Mixed) [(Arnab et al. 2022)](https://doi.org/10.1109/TENSYMP54529.2022.9864566).

- 25 polysomnography records (Jaeger-Toennies system) acompained by Three-channel holter ECGs (Reynolds Lifecard CF system)
- PSG records include EEG (C3-A2), EEG (C4-A1), left EOG, right EOG, submental EMG, ECG (modified lead V2), oro-nasal airflow (thermistor), ribcage movements, abdomen movements (uncalibrated strain gauges), oxygen saturation (finger pulse oximeter), snoring (tracheal microphone) and body position.
- Holter records include ECG (V5, CC5, V5R)
- Sampling frequency: SpO2 - 8 Hz; EEGs and ECGs - 128 Hz, EOG and EMG - 64 Hz a sample rate [**Sampling frequency**]
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

### Subjects

Subjects with no known cardiac disease, autonomic dysfunction, and not on medication known to interfere with heart rate. They were randomly selected over a 6-month period (September 2002 to February 2003) from patients referred to the Sleep Disorders Clinic at St Vincent's University Hospital, Dublin, for possible diagnosis of obstructive sleep apnea, central sleep apnea or primary snoring. 

| Characteristic | Description                       |
| ---            | ---                               |
| Age            | 50 ± 10 years; 28-68 years        |
| BMI            | 31.6 ± 4.0 kg/m²; 25.1-42.5 kg/m² |
| AHI            | 24.1 ± 20.3; 1.7-90.9             |
| Gender         | 21M, 4F                           |

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
-  In record ucddb002, only two distinct ECG signals were recorded; the second ECG signal was also used as the third signal
-  [(Geng et el.)](https://www.sciencedirect.com/science/article/pii/S1746809421007291) discarded poor ECG quality signals though they do not mention which. Additionally, the methods for R-peak detection was chosen specifically for signals with poor quality.
-  Several studies used filtering to remove artifacts [(Taghizadegan et al. 2021)](https://www.sciencedirect.com/science/article/pii/S030698772100178X#b0050), [(Hou et al. 2025)](https://www.sciencedirect.com/science/article/pii/S0169260724005510), [(Mashrur et al. 2021)](https://www.sciencedirect.com/science/article/pii/S0010482521003267).




## [MIT-BIH Polysomnographic Database](https://physionet.org/content/slpdb/1.0.0/)
*Published: Aug. 3, 1999. Version: 1.0.0*

The MIT-BIH Polysomnographic Database is contains over 80 hours of polysomnographic records, collected from patients at the Boston's Beth Israel Hospital Sleep Laboratory for chronic obstructive sleep apnea syndrome (OSA) evaluation and to test the effects of CPAP (continuous positive airway pressure). Records vary beatween four-, six-, and seven-channel record and include automatic (with corrections) beat annotations on the ECG and sleep stages and apnea events annotations each 30 s. This database was disignd for researchers studying clinical physiology or non-linear dynamics during sleep apnea, engineers developing algorithms for PSG data analysis, and students learning about sleep physiology. In literature it has been used for detectionn and classification tasks, including general apnea event detection [(Fatimah et al. 2020)](https://www.sciencedirect.com/science/article/pii/S1746809420301610), OSA event analysis [(Taghizadegan et al. 2021)](https://doi.org/10.1016/j.mehy.2021.110659), sleep stage classification [(Isa et al. 2012)](https://doi.org/10.1016/j.proeng.2012.07.259), [(Otomo et al. 2019)](https://doi.org/10.1016/j.procs.2019.08.173), drowsiness detection in sleep stage 1 [(Belakhdar et al. 2018)](https://doi.org/10.1016/j.micpro.2018.02.004), and heart rate estimation  [Rankawat & Dubey 2017)](https://doi.org/10.1016/j.bspc.2016.12.004).

- 18 PSG records from 16 subjects
- 12 bits per sample, 250 samples per second
- All recordings include an ECG signal, an invasive blood pressure signal (measured using a catheter), an EEG signal (C4-A1, O2-A1 or C3-O1), and a respiration signal (airflow or abdominal orchest effort)
- The six- and seven-channel recordings also include a respiratory effort signal derived by inductance plethysmography; some include an EOG signal and an EMG signal (chin), and the remainder include a cardiac stroke volume signa and Spo2 signal (earlobe).
- Subjects info (**LINK FILE**)

### Files

| File Type | Description                                                                         |
| ---       | ---                                                                                 |
| .dat      | Digitized Signals                                                                   | 
| .hea      | Text header files that specify the names and formats of the associated signal files |
| .ecg      | Automatic R-peak (heartbeat) annotations                                            |
| .st       | Sleep stages and Apnea annotations                                                  |
| .xws      | WAVE files for vizualising each record on Linux                                     |

### Subjects

| Characteristic | Description                       |
| ---            | ---                               |
| Age            | mean 43 years; 32-56 years        |
| Weight         | mean 119 kg; 89-152 kg     |
| Gender         | 16M                               |

### Annotations

| Type               | Description                                                         |
| ---                | ---                                                                 |
| Sleep stage        | W: wake, 1-4: sleep stages 1-4, R: REM |
| Respiratory events | H:	Hypopnea,	HA:	Hypopnea with arousal,	OA:	Obstructive apnea,	X:	Obstructive apnea with arousal,	CA:	Central apnea,	CAA:	Central apnea with arousal |
| Body movements     | L:	Leg movements,	LA:	Leg movements with arousal,	MT:	Movement time 
| Other              | A: Unspecified arousal                                              |

### Notes
- slp41 and slp 45 records do not have apnea annotations
- Records slp01a and slp01b are segments of one subject's polysomnogram, separated by a gap of about one hour; records slp02a and slp02b are segments of another subject's polysomnogram, separated by a ten-minute gap.
- Several studies reported employing some type of filtering to removw artifacts [(Taghizadegan et al. 2021)](https://doi.org/10.1016/j.mehy.2021.110659), [Rankawat & Dubey 2017)](https://doi.org/10.1016/j.bspc.2016.12.004), [(Belakhdar et al. 2018)](https://doi.org/10.1016/j.micpro.2018.02.004).



## [Sleep-EDF Database Expanded](https://physionet.org/content/sleep-edfx/1.0.0/)
*Published: Oct. 24, 2013. Version: 1.0.0* **VER**


The Sleep-EDF database comprises 197 whole-night polysomnographic (PSG) sleep recordings originating from two studies: the Sleep Cassette Study and Data (SC) and the Sleep Telemetry Study and Data (ST). The SC dataset includes 153 records collected from 1987 to 1991 for a study on age effects on sleep in healthy Caucasians, without sleep-related medication. Subjects wore a modified Walkman-like cassette recorder to collect two PSGs of about 20 hours each over two consecutive day-night periods at home while maintaining normal activities. The ST dataset includes 44 files collected in 1994 for study on temazepam effects on sleep in caucasians with mild difficulty falling asleep but otherwise healthy. Two records of 9h were collected for each patient using a miniature telemetry system, one following temazepam intake and the other after placebo intake. In literature this data base has been mostly used for sleep stage scoring [(He et al. 2022)](https://doi.org/10.1016/j.compbiomed.2022.106044), [(Abdulla et al. 2023)](https://www.sciencedirect.com/science/article/pii/S1386505623000187), [(Li. et al. 2023)](https://doi.org/10.1016/j.compbiomed.2023.107477), [(Zhao et al. 2024)](https://doi.org/10.1016/j.bspc.2023.105615)

- 197 PSG records from 2 studies: 153 20h long records from 74 subjects (SC) and 44 9h long records from 22 subjects (ST)
- 12 bits per sample
- All records contain EEG (from Fpz-Cz and Pz-Oz electrode locations) signals, EOG (horizontal) signals, and submental chin EMG signal.
- The SC records often also contain oro-nasal respiration and rectal body temperature.
- SC frequency: EOG and EEG - 100 Hz. The submental-EMG, Oro-nasal airflow, rectal body temperature - 1Hz.
- ST frequency: EOG, EMG and EEG - 100 Hz, and the event marker at 1 Hz.

### Files

| File Type     | Description                                            |
| ---           | ---                                                    |
| PSG.edf       | Digitized Signals in European data format              | 
| Hypnogram.edf | Sleep satges annotations file in European Data Format  |
| .xls          | Subject information                                    |


### Subjects

| Characteristic | SC                                | ST                         |
| ---            | ---                               | ---                        |
| Age            | mean 59 years; 25-101 years       | mean 40 years; 18-79 years |
| Gender         | 34M/40F                           | 7M/15F                     |

### Annotations

Hypnograms were manually scored by trained technicians (identified by the eighth letter of the hypnogram filename) according to the 1968 R & Kales rules, but based on Fpz-Cz/Pz-Oz EEGs instead of C4-A1/C3-A2 EEGs.

| Type               | Description                                                             |
| ---                | ---                                                                     |
| Sleep stage        | W: wake, 1-4: sleep stages 1-4, R: REM, M: Movement time, ?: not scored |


### Notes
- SC: The first nights of subjects 36 and 52, and the second night of subject 13, were lost due to a failing cassette or laserdisk.
- SC: The submental-EMG signal was electronically highpass filtered, rectified and low-pass filtered
- Files are named in the form \*\*7**ssN**J0-PSG.edf where ss is the subject number, and N is the night.
- Several studies reported employing some type of filtering to removw artifacts [(Ghimatgar et al. 2019)](https://doi.org/10.1016/j.jneumeth.2019.108320), [Hamouda et al. 2024)](https://doi.org/10.1016/j.bspc.2024.106184), [(Fei et al. 2024)](https://doi.org/10.1016/j.compbiomed.2024.108300)



## [ISRUC-Sleep Dataset](https://sleeptight.isr.uc.pt/)
*Published: 2016. Version: unknown*

The ISRUC-Sleep dataset is contains 126 PSG records from both healthy and sleep disorders subject collected by the Sleep Medicine Centre of the Hospital of Coimbra University (CHUC) between 2009 and 2013. The dataset is divided into 3 subgroups and was designed to support various research objectives, including biomedical signal processing, the development of new automated sleep stage classification (ASSC) methods, and studies in sleep physiology. Subgroup_1 (SG1) contains data from 100 subjects with evidence of sleep disorders (some under sleep medication), each undergoing one recording session. Subgroup_2 (SG2) contains data from 8 subjects with evidence of sleep disorders (some under sleep medication), each undergoing two recording sessions on different dates, making it suitable for studies on changes in PSG signals over time. Subgroup_3 (SG3) contains data from 10 healthy control subjects, each undergoing one recording session, which is useful for comparing healthy individuals with patients suffering from sleep disorders. In literature this data base has been mostly used for sleep stage scoring [(Khalighi et al. 2013)](https://doi.org/10.1016/j.eswa.2013.06.023), [(Ghimatgar et al. 2019)](https://doi.org/10.1016/j.jneumeth.2019.108320), [(Moctezuma et al. 2023)](https://doi.org/10.1016/j.ifacol.2023.10.1458), however it has also been used for sleep apnea event detection [(Rehman et al. 2025)](https://doi.org/10.1016/j.engappai.2024.109534).

- 126 polysomnography records: 100 from 100 subjects (SG_1), 16 from 8 subjects (SG_2) and 10 from 10 subjects (SG_3).
- PSG records include EEG (F3-A2, C3-A2, O1-A2, F4-A1, C4-A1, and O2-A1), EOG (LOC-A2 and ROC-A1), EMG (chin: X1, righ leg: X3, left leg: X4), ECG (X2), snore (X5), airflow (X6 and DC3), Abdominal effort (X7 and X8), SaO2, Body Position (DC8).
- Sampling frequency: EOG, EEG, EMG, ECG, Snore - 200 Hz, Airflow (X6), SaO2 - 12.5 Hz, Airflow (DC3), Abdominal effort, Body Position - 25 Hz; 
- Some signlas are pre-filtered: EOG, EEG - Butterworth band of 0.3–35 Hz and a 50 Hz notch filter; EMG, Snore - Butterworth band of 10–70 Hz and a 50 Hz notch filter; ECG - notch filter 50 Hz.

### Files
 
| File Type | Description                                                                                    |
| ---       | ---                                                                                            |
| .rec      | Digitized Polysonography Signals in European Data format                                       | 
| .mat      | Digitized Polysonography Signals in MATLAB format                                              |
| .text     | Hypnogram Annotation files                                                                     |
| .xlsx     | Events and sleep stanging (same as hypnogram, different format), and subject information files |

### Subjects

SG1 and SG2 consists of subjects with evidence of sleep disorders that could be under medication, but all were capable of breathing unaided, while SG3 consists of a control group with healthy subjects.

| Characteristic | Subgroup_1                 | Subgroup_2                | Subgroup3                  |
| ---            | ---                        | ---                       | ---                        |
| Age            | 51 ± 16 years; 20–85 years | 46.87 ± 18.7; 26-79 years | 40 ± 10 years; 30–58 years | 
| Gender         | 55M, 45F                   | 6M, 2F                    | 9M, 1F                     |

### Annotations

Sleep stages were scored in AASM Standard by two different sleep experts.

| Type               | Description                                                                                                 |
| ---                | ---                                                                                                         |
| Sleep stage        | W: wake, N1, N2, N3, R: REM                                                                                 |
| Respiratory events | CH: Central Hypopnea, C: Central Apnea, OH: Obstructive Hypopnea, OA: Obstructive Apnea, MH: Mixed Hypopnea |
| HR                 | Heart rate                                                                                                  |
| Lights             | L out: Lights turned off, L on: Lights turned on                                                            |
| SaO2               | oxigen saturation in percentage                                                                             |
| Movement           | LM: Leg Movement, MP: Movement Periodic, PLM: Periodic Leg Movement                                         |


### Notes
-  No info on ECG lead placement
-  Since annotations were made by to different experts, not all may agree. So, some studies, when devoloping systems for stage scoring, ignore the stages in which there's no agreement [(Moctezuma et al. 2023)](https://doi.org/10.1016/j.ifacol.2023.10.1458).
-  Even though the signals are pre-filtered, several studies used filtering to remove artifacts [(Khalighi et al. 2013)](https://doi.org/10.1016/j.eswa.2013.06.023), [(Ghimatgar et al. 2019)](https://doi.org/10.1016/j.jneumeth.2019.108320).


## [Sleep Heart Health Study (SHHS)](https://biolincc.nhlbi.nih.gov/studies/shhs/)
*Published: Unknown (revised on October 2, 2024)*

This data base was designed to investigate the relationship between sleep disordered breathing and cardiovascular disease, stroke, all-cause mortality, and hypertension. The Sleep Heart Health Study (SHHS) contains subjects from well-characterized and established epidemiologic cohorts: The Hagerstown and Minneapolis/St. Paul sites of the Atherosclerosis Risk in Communities Study (ARIC), The Hagerstown, Sacramento and Pittsburgh sites of the Cardiovascular Health Study (CHS), The Framingham Offspring Cohort, The Strong Heart Study (SHS) sites in South Dakota, Oklahoma, and Arizona, The New York Hypertension Cohorts, The Tucson Epidemiologic Study of Airways Obstructive Diseases and the Health and Environment Study. The study incorporated in-home polysomnography into the data collected from each parent study during a baseline SHHS exam and a follow-up approximately 4 years later. In the literature, SHHS data has been widely used for sleep stage scoring studies [(Li. et al. 2023)](https://doi.org/10.1016/j.compbiomed.2023.107477), [(Zhao et al. 2024)](https://doi.org/10.1016/j.bspc.2023.105615), and correlation analyses, including the relationship between subjective sleep quality and objective measures of sleep [(Kaplan et al. 2017)](https://doi.org/10.1016/j.sleep.2017.03.004), the predictive role of sleep hypoxemia in mortality in patients with sleep apnea [(Khouzani et al. 2024)](https://doi.org/10.1016/j.chpulm.2024.100087), and the study of heart rate variability during sleep onset in patients with insomnia [(Fan et al. 2023)](https://doi.org/10.1016/j.sleep.2023.06.005).

-  5804 PSG subjects (SHHS-1) with a follow-up polysomnogram (SHHS-2) for 3295 of the participants
-  Polysomonography records include EEG (C3/A2 and C4/A1), EOG (right and left), EMG (bipolar submental), ECG (bipolar lead), abbdominal and thoracix effort, airflow, Heart rate (derived from ECG), SpO2, Body position, ambient light 
- Sampling frequency: EEG, ECG (SHHS-1) and EMG - 125 Hz; EOG - 50 Hz; ECG (SHHS-2) - 250 Hz, airflow, THOR and ABDO - 10 Hz; Heart rate, Spo2 - 1 Hz
- Each participant in the parent studies was completed a questionaire covering usual sleep pattern, snoring, and sleepiness.

### Files
 
| File Type | Description                                                                            |
| ---       | ---                                                                                    |
| .edf      | Digitized Polysonography Signals in European Data format                                       |
| .hea      | Text header files that specify the formats of the associated signal files as well as subject info                             | 
| .hyp      | Sleep stages annotation files                                                                       |
| .arous    | Arousal events annotation files |
| .resp     | Respiratory events annotation files                                |
| .oart     | Oximeter artifacts annotation files                                       |
| .comp     | all annotations from the hypn, arou, resp, and oart files                                       |

### Subjects

| Characteristic | Description                |
| ---            | ---                        |
| Age            | 63.1 years; 39–90 years    |
| Gender         | 2765M, 3039F               |

### Annotations
Sleep stages was scored using the Rechtschaffen and Kales (R&K) guidelines. Addicionally, there are annotations for respiratory and arousal events, and oximiter artifacts.

### Data by request
Data can be resqueted [here](https://biolincc.nhlbi.nih.gov/login/?next=/requests/type/shhs/):
- Must have BioLINCC account
- Must fill a request form

### Notes
- A study reported that 101 records had poor quality or where incomplete [(Kaplan et al. 20127)](https://doi.org/10.1016/j.sleep.2017.03.004)


## [NCH Sleep DataBank](https://sleepdata.org/datasets/nchsdb)
*Published: February 2021. (revised on July 2022)*

This database was created by Nationwide Children's Hospital (NCH) and Carnegie Mellon University (CMU) to accelerate research on pediatric sleep and its connection to health. It contains 3,984 pediatric PSG records from 3,673 unique patients collected in the real-world clinical setting at NCH in Columbus, Ohio, USA between 2017 and 2019, along with the patients' longitudinal clinical data. The NCH Sleep DataBank was designed to study many problems related to pediatric sleep, including: Automatic sleep stage classification, especially algorithms that combine modalities beyond EEG or ECG, Automatic real-time sleep disorder (e.g. apnea) detection, diagnosis prediction, identifying patient subgroups that could affect their symptoms or best courses of treatment, and treatment (e.g. medications and procedures) efficacy analysis. Studies using this database have addressed diverse applications, such as sleep stage scoring [(Lee et al. 2023)](https://doi.org/10.1007/s13534-023-00288-6), obstructive sleep apnea diagnosis [(Wang et al. 2025)](https://doi.org/10.1007/s40747-024-01648-0), prevalence and influencing factors of sleep disorders among preschool children [(Gao et al. 2023)](https://doi.org/10.1186/s13052-023-01477-w), and mapping neurodevelopment using sleep-based features in pediatric populations [(Kozhemiako et al. 2024)](https://doi.org/10.1016/j.nicl.2023.103552).


- 3,984 polysomnography records from 3,673 subjects with a mean of 10.5h
- PSG records include EEG, EMG (chin and leg EMG), EOG, ECG, airflow, thoracic and abdominal effort, SpO2, bood CO2.
- Almost half (1,972) of the files have 26 channels, a quarter (1,012) have 29, a fifth (820) have 25, and the rest have 28, 24, 40, 27, 9, or 56 channels.
- Sampling frequency: 3,204 records in 256 Hz, 581 in 400 Hz, and 199 in 512 Hz.


### Files
 
| File Type | Description                                                                                       |
| ---       | ---                                                                                               |
| .edf      | Digitized Polysonography Signals in European Data format                                          |
| .annot    | Annotations on WFDB-format                                                                        | 
| .tsv      | Annotations on Tab-Separated Value (TSV) format                                                   |
| .csv      | Information files on demographic, diagnosis, medication, procedure, etc ...                       |  

### Subjects

| Characteristic | Description                                                                                |
| ---            | ---                                                                                        | 
| Age            | Most <10                                                                                   | 
| Gender         | 2068M, 1604F, 1 Unknown                                                                    |
| Race           | 2433 White, 738 Black or African American, 277 Multiple races, 93 Asian, 132 Other/Unknown |
| Ethnicity      | 186 Hispanic or Latino, 3,446 Not Hispanic or Latino, and 41 Unknown                       |

### Annotations

Sleep stages were scored in AASM Standard.

| Type               | Description                                                                                                 |
| ---                | ---                                                                                                         |
| Sleep stage        | W: wake, N1, N2, N3, R: REM                                                                                 |
| Respiratory events | Obstructive Hypopnea, Obstructive Apnea, Hypopnea, Central Apnea, and Mixed Apnea                           |
| Lights             | Lights on, Lights off                                                                                       |
| Movement           | Limb Movement, Move                                                                                         |
| Body Position      | Left, Right, Supine, Prone, Upright                                                                                                                   |
| Sleep Stage?       | Typically occurs after “Lights On”, and physiological data acquired during that time can usually be ignored, as it indicates that the study has ended |
| Others             | Oxygen Desaturation, Oximeter Event, EEG Arousal, Gain/Filter Change                                                                                  |

### Data by request
Data can be resqueted [here](https://sleepdata.org/datasets/nchsdb):
- Must have NSRR account
- Must fill a request form
- For non-comercial use



## [Sleep Disorder Research Centre](https://data.mendeley.com/datasets/3hx58k232n/4)
*Published: 25 September 2017. Version 4.*

The data from this database were originally collected for a research project entitled “Sleep EEG spectral analysis in psycho-physiological insomnia and normal sleep subjects.” This article describes data from patients referred to the Sleep Disorders Research Center (SDRC). This database includes PSG data from subjects with psycho-physiological insomnia as well as normal sleepers. In literature, this dataset has been employed on two types of applications: insomnia detection [(Sharma et al. 2024)](http://dx.doi.org/10.1007/s10489-024-05284-6), [(Kumar et al. 2024)](http://dx.doi.org/10.1109/TLA.2024.10431420), and sleep stage classification [(Moradi et al. 2020)](http://dx.doi.org/10.1159/000511306).

- 22 8h PSG records, 11 with insomnia and 11 without
- PSG based on the American Academy of Sleep Medicine guidelines
- EEG (C4-A1, C3-A2, F3, F4, C3, C4, A1, A2, O1, O2, F3-A2, F4A-1, O1-A2, O2-A1), EOG ((EOG1, EOG2, EOG1-A1, EOG2-A1, EOG1-A2, EOG2-A2) and 3 EMG (EMG, EMG1, EMG2).
- Sample frequency: 256 Hz
- Filtering: EEG - band pass between 0.1 Hz and 35Hz
- Includes power spectral features of each band (δ, θ, α, β) in segment of 30 s for each channel and nonlinear analysis parameters.
- The polysomnography room was cleaned from artefacts like auditory and visual noises.

### Files

| File Type     | Description                                            |
| ---           | ---                                                    |
| .edf       | Digitized Signals in European data format              | 
| Hypnogram.edf | Sleep satges annotations file in European Data Format  |
| Arousal.txt   | Arousal annotations                                    |
| REM.txt   | REM events annotations                                    |
|  Sleep Profile Reliability.txt   | Reliability of the sleep profile   |
|  Sleep Profile.txt   | Sleep stage annotations                        |
|  Spindle K.txt   | Spindle and K complex annotations                                    |

### Subjects

| Characteristic | SC                                | 
| ---            | ---                               | 
| Age            | 43.2 ± 14.2 years; 18-63 years |
| Gender         | 8M/14F                           | 


### Annotations

Sleep stages were scored according to R & Kales rules. There are also annotations of arousal, spindles and K-complexes. 

| Type               | Description                                                             |
| ---                | ---                                                                     |
| Sleep stage        |  Stage 4, Stage 3, Stage 2, Stage 1, Rem, Wake, Movement  |


### Notes
- EEG was recorded using Ag/AgCl electrodes, as per the International 10–20 System of Electrode Placement
- Mention of filtering of the EEG by the equipment but no mention about EMG and ECG












