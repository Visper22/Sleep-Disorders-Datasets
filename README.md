# Sleep-Disorders-Datasets

## [Apnea-ECG Database](https://physionet.org/content/apnea-ecg/1.0.0/)
Published: Feb. 10, 2000. Version: 1.0.0

The Apnea-ECG Database was design to support the development of automated methods for detecting sleep apnea events, emphasizing the use of ECG signals. So it has been many employed in various studies for the detection of sleep apnea events [(Fatimah et al. 2020)](https://doi.org/10.1016/j.bspc.2020.102005), [(Mashrur et al. 2021)](https://doi.org/10.1016/j.compbiomed.2021.104532), [(Yang et al. 2022)](https://doi.org/10.1016/j.compbiomed.2021.105124), [(Wei et al., 2024)](https://doi.org/10.1109/IMCEC59810.2024.10575752), [(Li et al., 2024)](https://doi.org/10.1109/TIM.2024.3440369) [(Hou et al. 2025)](https://doi.org/10.1016/j.cmpb.2024.108558) but also, for subject-level sleep apnea classification [(Jiao et al., 2024)](https://doi.org/10.1109/OJEMB.2024.3405666).

- 70 ECG records from 7 hours to 10 hours
- 16 bits per sample, least significant byte first in each pair, 100 samples per second, nominally 200 A/D units per millivolt
- Records a01 through a04, b01, and c01 through c03 are accompanied by additional signals: chest and abdominal respiratory effort signals obtained using inductance plethysmography (Resp C and Resp A), oronasal airflow measured using nasal thermistors (Resp N), and oxygen saturation (SpO2).
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
- Though the signals are pre-filtered some studies still employed some kind of filtering [(Sheng-Hsiou et al. 2018)](https://www.sciencedirect.com/science/article/pii/S1053811918306888), [(Yan et al. 2019)](https://www.sciencedirect.com/science/article/pii/S1746809418302647), [(Sharma et al. 2023)](https://www.sciencedirect.com/science/article/pii/S0010482523007242#b36), [(Agarwal et al. 2024)](https://www.sciencedirect.com/science/article/pii/S1389945724004465).
- Not clear about ECG lead positioning
- Channel names are inconsistent




## [St. Vincent's University Hospital / University College Dublin Sleep Apnea Database](https://physionet.org/content/apnea-ecg/1.0.0/)
Published: Oct. 9, 2007. Version: 1.0.0 (revised on 1 September 2011)

The database contains overnight polysomnograms and simultaneous three-channel Holter ECG recordings from adults with suspected sleep-disordered breathing, collected at St. Vincent's University Hospital Sleep Disorders Clinic. It can be used for multiple porposes, such as sleep stage classification and sleep apnea event detection. Studies have been made on sleep/wake classification [(Geng et al 2022)](https://doi.org/10.1016/j.bspc.2021.103132) and sleep stage classification [(Abdulla et al. 2023)](https://doi.org/10.1016/j.ijmedinf.2023.105001). For sleep apnea events detection some studies detect sleep apnea events,  regardless of type [(Fatimah et al. 2020)](https://doi.org/10.1016/j.bspc.2020.102005), [(Cai et al. 2025)](https://doi.org/10.1016/j.bspc.2024.106993), while others focus on specific events detection, such as obstructive sleep apnea event detection [(Taghizadegan et al. 2021)](https://doi.org/10.1016/j.mehy.2021.110659), and multiple sleep apnea events detection (Hypopnea, Central, Obstructive,Mixed) [(Arnab et al. 2022)](https://doi.org/10.1109/TENSYMP54529.2022.9864566).

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
Published: Aug. 3, 1999. Version: 1.0.0

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
- Several studies reported employing some type of filtering to removw artifacts [(Taghizadegan et al. 2021)](https://doi.org/10.1016/j.mehy.2021.110659), [Rankawat & Dubey 2017)](https://doi.org/10.1016/j.bspc.2016.12.004), [(Belakhdar et al. 2018)](https://doi.org/10.1016/j.micpro.2018.02.004)



## [Sleep-EDF Database Expanded](https://physionet.org/content/sleep-edfx/1.0.0/)
Published: Oct. 24, 2013. Version: 1.0.0

The sleep-edf database contains 197 whole-night PolySomnoGraphic sleep recordings, containing EEG, EOG, chin EMG, and event markers. Some records also contain respiration and body temperature.  The data comes from two studies: Sleep Cassette Study and Data (SC) and Sleep Telemetry Study and Data (ST).

Sleep Cassette Study and Data
The 153 SC* files (SC = Sleep Cassette) were obtained in a 1987-1991 study of age effects on sleep in healthy Caucasians aged 25-101, without any sleep-related medication [2]. Two PSGs of about 20 hours each were recorded during two subsequent day-night periods at the subjects homes. Subjects continued their normal activities but wore a modified Walkman-like cassette-tape recorder. 
74 subjects

Sleep Telemetry Study and Data
The 44 ST* files (ST = Sleep Telemetry) were obtained in a 1994 study of temazepam effects on sleep in 22 Caucasian males and females without other medication. Subjects had mild difficulty falling asleep but were otherwise healthy. The PSGs of about 9 hours were recorded in the hospital during two nights, one of which was after temazepam intake, and the other of which was after placebo intake. Subjects wore a miniature telemetry system with very good signal quality described in [8]. 
22 subjects

- 197 PSG records from 2 studies:
- 12 bits per sample, 250 samples per second
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
- Files are named in the form */*7**ssN**J0-PSG.edf where ss is the subject number, and N is the night.
- Several studies reported employing some type of filtering to removw artifacts [(Taghizadegan et al. 2021)](https://doi.org/10.1016/j.mehy.2021.110659), [Rankawat & Dubey 2017)](https://doi.org/10.1016/j.bspc.2016.12.004), [(Belakhdar et al. 2018)](https://doi.org/10.1016/j.micpro.2018.02.004)




















## [Sleep Heart Health Study (SHHS)](https://biolincc.nhlbi.nih.gov/studies/shhs/)
Published: Oct. 9, 2007. Version: 1.0.0 (revised on 1 September 2011)

To determine the cardiovascular and other consequences of sleep-disordered breathing and to test whether sleep-disordered breathing is associated with an increased risk of coronary heart disease, stroke, all-cause mortality and hypertension by examining subjects from well-characterized and established epidemiologic cohorts. The Sleep Heart Health Study added in-home polysomnography to the data collected in each of the parent studies at a baseline SHHS exam and a follow-up approximately 4 years later.

SHHS Visit 1 (November 1995 - January 1998) (N=5798)
-  5804 Polysomonography records (SHHS-1)
-  Follow-up polysomnogram (SHHS-2) was obtained for 3295 of the participants
-  Polysomonography records include EEG (C3/A2 and C4/A1), EOG (right and left), EMG (bipolar submental), ECG (bipolar lead), Respiratory signals (abbdominal and thoracix effort, and airflow), Heart rate (derived from ECG), pO2, Body position, ambient light 
- Sampling frequency: EEG, ECG (SHHS-1) and EMG - 125 Hz; EOG - 50 Hz; ECG (SHHS-2) - 250 Hz, airflow, THOR and ABDO - 10 Hz; Heart rate, Spo2 - 1 Hz
- Each participant in the parent studies was completed a questionaire covering usual sleep pattern, snoring, and sleepiness.



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
-  No paper on the db




Sleep-EDF Sleep stages classification [(Abdulla et al. 2023)](https://www.sciencedirect.com/science/article/pii/S1386505623000187)














