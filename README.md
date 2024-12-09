# Sleep-Disorders-Datasets

## Apnea-ECG Database

The data consist of 70 records, divided into a learning set of 35 records (a01 through a20, b01 through b05, and c01 through c10), and a test set of 35 records (x01 through x35). Recordings vary in length from slightly less than 7 hours to nearly 10 hours each. Each recording includes a continuous digitized ECG signal, a set of apnea annotations (derived by human experts on the basis of simultaneously recorded respiration and related signals), and a set of machine-generated QRS annotations (in which all beats regardless of type have been labeled normal). In addition, eight recordings (a01 through a04, b01, and c01 through c03) are accompanied by four additional signals (Resp C and Resp A, chest and abdominal respiratory effort signals obtained using inductance plethysmography; Resp N, oronasal airflow measured using nasal thermistors; and SpO2, oxygen saturation).

(16 bits per sample, least significant byte first in each pair, 100 samples per second, nominally 200 A/D units per millivolt)
.apn an annotation for each minute of each recording indicating the presence or absence of apnea at that time; these are available for the 35 learning set recordings only. 
The qrs files are machine-generated (binary) annotation files, made using sqrs125. Please note that the .qrs files are unaudited and contain errors. 

###Files

| File Type | Description                                                                         |
| ---       | ---                                                                                 |
| .dat      | Digitized Signals                                                                   | 
| .hea      | Text header files that specify the names and formats of the associated signal files |
| .apn      | Binary annotation files of apnea events                                             |
| .qrs      | Binary annotation files of the QRS complex                                          |
| .xws      | WAVE files for vizualising each record on Linux                                     |



Problems:
In April 2013, Chiu-wen Wu reported that training set control records c05 and c06 come from the same original recording (c05 begins 80 seconds later than c06). The slightly different descriptions of these records in additional-information.txt suggest that c06 may have been a corrected version of c05.

