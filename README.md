# Electrocardiogram

## DataSets

| S.No. | Name                                                        | #Records | Record Length | #Patients | #Leads | #Sampling Frequency |
|:------|:-----------------------------------------------------------:|---------:|--------------:|----------:| ------:| -------------------:|
| 1     | MIT-BIH Arrhythmia Database                                 | 48       | 30 min        | 47        | 2      | 
| 2     | MIT-BIH Noise Stress Database                               | 12       | 30 min        | N.A.      | 2      |
| 3     | MIT-BIH Atrial Fibrillation Database                        | 25       | 10 hr         | N.A.      | 2      |
| 4     | MIT-BIH Normal Sinus Rhythm Database                        | 18       | 24 hr         | 18        | 2      |
| 5     | MIT-BIH maligant ventricular Ectopy Database                | 22       | 30 min        | N.A.      | 2      |
| 6     | MIT-BIH Supraventricular arrhythmia Database                | 78       | 30 min        | N.A.      | 3      |
| 7     | St. Petersburg INCART 12-lead Arrhythmia Database           | 75       | 30 min        | 32        | 12     |
| 8     | Creighton University Ventricular Tachyarrhythmia Database   | 35       | 8.5 min       | N.A.      | 1      |
| 9     | Long-Term AF Database                                       | 75       | 24-25 hr      | N.A.      | 2      |
| 10    | Sudden Cardiac Death Holter Database                        | 23       | 24-48 hr      | 18        | 2-3    |
| 11    | Georgia 12-Lead ECG Challenge Database                      | 10344    | 5-10 sec      | N.A.      | 12     |
| 12    | China Physiological Signal Challenge 2018 (CPSC 2018)       | 6877     | 6-60 sec      | N.A.      | 12     |
| 13    | European ST-T Database                                      | 90       | 2 hr          | 79        | 2      |
| 14    | Apnea-ECG Database                                          | 70       | 7-10 hr       | N.A.      | 1      |
| 15    | PTB Diagnostic ECG Database                                 | 549      | 10 sec        | 290       | 12     |
| 16    | Normal Sinus Rhythm RR Interval Database                    | 54       | 24 hr         | 54        | N.A.   |

# Systematic Literature Review

1. [Ansari Y, Mourad O, Qaraqe K and Serpedin E (2023), Deep learning for ECG Arrhythmia detection and classification: an overview of progress for period 2017–2023. Front. Physiol. 14:1246746. doi: 10.3389/fphys.2023.1246746](https://www.frontiersin.org/journals/physiology/articles/10.3389/fphys.2023.1246746/full)
   
# Arrhythmia Beat Classification

  ## SOTA : 
  [Ye C, Coimbra MT, Vijaya Kumar BK. Arrhythmia detection and classification using morphological and dynamic features of ECG signals. Annu Int Conf IEEE Eng Med Biol Soc. 2010;2010:1918-21. doi: 10.1109/IEMBS.2010.5627645. PMID: 21097000.](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=5627645)
  
  ## Implementation :
  Find the implementation of above for MIT-BIH Arrhythmia Database and St. Petersberg INCART Database [here](https://github.com/SahilShahare/Beat-Classification-MIT-BIH) and [here]() respectively.
  


  ### MIT-BIH Arrhythmia Database

  ### Classes:

  | Name                                  | Annotation |
  |--------------------------------------:|-----------:|
  | Normal Beat                           | N          |
  | Left Bundle Branch Block Beat         | L          |
  | Right Bundle Branch Block Beat        | R          |
  | Atrial Premature Beat                 | A          |
  | Premature Ventricular Contraction     | V          |
  | Paced Beat                            | /          |
  | Aberrated Atrial Premature Beat       | a          |
  | Ventricular Flutter Wave              | !          |
  | Fusion of Ventricular and Normal Beat | F          |
  | Non-conducted P-wave (blocked APB)    | x          |
  | Nodal (junction) Escape Beat          | j          |
  | Fusion of Paced and Normal Beat       | f          |
  | Ventricular Escape Beat               | E          |
  | Nodal (junctional) Premature Beat     | J          |
  | Atrial Escape Beat                    | e          |

  ### Results
  #### Lead 1
  * Accuracy (Train): 0.9971
  * Accuracy (Test): 0.9847
  * Specificity and Sensitivity:
<div style="display: flex; justify-content: space-between; text-align: center;">
  <div style="margin-right: 10px;">
    <h4>Train</h4>
    <table border="1" style="border-collapse: collapse;">
      <tr>
        <th>Label</th>
    <th>Sensitivity</th>
    <th>Specificity</th>
      </tr>
      <tr>
        <td>!</td>
        <td>1.0</td>
        <td>1.0 </td>
      </tr>
      <tr>
        <td>/</td>
        <td>0.9996</td>
        <td>0.9998 </td>
      </tr>
      <tr>
        <td>A</td>
        <td>0.9823</td>
        <td> 0.9996 </td>
      </tr>
      <tr>
        <td>E</td>
        <td>1.0</td>
        <td> 1.0 </td>
      </tr>
      <tr>
        <td>F</td>
        <td>0.9726</td>
        <td> 1.0 </td>
      </tr>
      <tr>
        <td>J</td>
        <td>0.9756</td>
        <td>1.0 </td>
      </tr>
      <tr>
        <td>L</td>
        <td>0.9994</td>
        <td>0.9999 </td>
      </tr>
      <tr>
        <td>N</td>
        <td>0.9988</td>
        <td>0.9968</td>
      </tr>
      <tr>
        <td>R</td>
        <td>0.9997</td>
        <td> 1.0 </td>
      </tr>
      <tr>
        <td>V</td>
        <td>0.9961</td>
        <td> 1.0</td>
      </tr>
      <tr>
        <td>a</td>
        <td>0.9733</td>
        <td> 1.0</td>
      </tr>
      <tr>
        <td>e</td>
        <td>1.0</td>
        <td>1.0 </td>
      </tr>
      <tr>
        <td>f</td>
        <td>0.9857</td>
        <td>0.9998 </td>
      </tr>
      <tr>
        <td>j</td>
        <td>0.9649</td>
        <td>1.0 </td>
      </tr>
      <tr>
        <td>x</td>
        <td>1.0</td>
        <td>1.0 </td>
      </tr>
    </table>
  </div>

  <div style="margin-left: 10px;">
    <h4>Test</h4>
    <table border="1" style="border-collapse: collapse;">
      <tr>
        <th>Label</th>
    <th>Sensitivity</th>
    <th>Specificity</th>
      </tr>
      <tr>
        <td>!</td>
        <td>0.9524</td>
        <td>0.9998 </td>
      </tr>
      <tr>
        <td>/</td>
        <td>0.9981</td>
        <td>0.9996</td>
      </tr>
      <tr>
        <td>A</td>
        <td>0.9286</td>
        <td>0.9965</td>
      </tr>
      <tr>
        <td>E</td>
        <td>1.0</td>
        <td>1.0</td>
      </tr>
      <tr>
        <td>F</td>
        <td>0.8055</td>
        <td>0.9979</td>
      </tr>
      <tr>
        <td>J</td>
        <td>0.6667</td>
        <td>0.9996</td>
      </tr>
      <tr>
        <td>L</td>
        <td>0.9934</td>
        <td>0.9992</td>
      </tr>
      <tr>
        <td>N</td>
        <td>0.9875</td>
        <td>0.9872</td>
      </tr>
      <tr>
        <td>R</td>
        <td>0.9949</td>
        <td>0.9997</td>
      </tr>
      <tr>
        <td>V</td>
        <td>0.9687</td>
        <td>0.9964 </td>
      </tr>
      <tr>
        <td>a</td>
        <td>0.6267</td>
        <td>0.9997</td>
      </tr>
      <tr>
        <td>e</td>
        <td>0.375</td>
        <td>0.9999 </td>
      </tr>
      <tr>
        <td>f</td>
        <td>0.943</td>
        <td>0.9996</td>
      </tr>
      <tr>
        <td>j</td>
        <td>0.8261</td>
        <td>0.9995</td>
      </tr>
      <tr>
        <td>x</td>
        <td>0.8763</td>
        <td>0.9999</td>
      </tr>
    </table>
  </div>

</div>

* Confusion Matrix
<div style="display: flex; justify-content: space-around; align-items: center; text-align: center;">

  <div style="margin-right: 10px;">
    <h3>Train</h3>
    <img src="Resources/CM_MIT_Lead1_Train.png" alt="Image 1" style="width: 600px; height: auto;">
  </div>

  <div style="margin-left: 10px;">
    <h3>Test</h3>
    <img src="Resources/CM_MIT_Lead1_Test.png" alt="Image 2" style="width: 600px; height: auto;">
  </div>
    </div>

#### Lead 2
  * Accuracy (Train): 0.9937
  * Accuracy (Test): 0.9775
  * Specificity and Sensitivity:
<div style="display: flex; justify-content: space-between; text-align: center;">
  <div style="margin-right: 10px;">
    <h4>Train</h4>
    <table border="1" style="border-collapse: collapse;">
      <tr>
        <th>Label</th>
    <th>Sensitivity</th>
    <th>Specificity</th>
      </tr>
      <tr>
        <td>!</td>
        <td>1.0</td>
        <td>1.0 </td>
      </tr>
      <tr>
        <td>/</td>
        <td>0.9996</td>
        <td>1.0 </td>
      </tr>
      <tr>
        <td>A</td>
        <td>0.9666</td>
        <td> 0.9992 </td>
      </tr>
      <tr>
        <td>E</td>
        <td>1.0</td>
        <td> 1.0 </td>
      </tr>
      <tr>
        <td>F</td>
        <td>0.9526</td>
        <td> 1.0 </td>
      </tr>
      <tr>
        <td>J</td>
        <td>0.9512</td>
        <td>1.0 </td>
      </tr>
      <tr>
        <td>L</td>
        <td>0.9994</td>
        <td>1.0 </td>
      </tr>
      <tr>
        <td>N</td>
        <td>0.9963</td>
        <td>0.9939</td>
      </tr>
      <tr>
        <td>R</td>
        <td>1.0</td>
        <td> 0.9999 </td>
      </tr>
      <tr>
        <td>V</td>
        <td>0.9835</td>
        <td> 0.9991</td>
      </tr>
      <tr>
        <td>a</td>
        <td>0.9333</td>
        <td> 1.0</td>
      </tr>
      <tr>
        <td>e</td>
        <td>0.875</td>
        <td>1.0 </td>
      </tr>
      <tr>
        <td>f</td>
        <td>0.998</td>
        <td>0.9994 </td>
      </tr>
      <tr>
        <td>j</td>
        <td>0.9561</td>
        <td>0.9996 </td>
      </tr>
      <tr>
        <td>x</td>
        <td>1.0</td>
        <td>1.0 </td>
      </tr>
    </table>
  </div>

  <div style="margin-left: 10px;">
    <h4>Test</h4>
    <table border="1" style="border-collapse: collapse;">
      <tr>
        <th>Label</th>
    <th>Sensitivity</th>
    <th>Specificity</th>
      </tr>
      <tr>
        <td>!</td>
        <td>0.9683</td>
        <td>0.9997 </td>
      </tr>
      <tr>
        <td>/</td>
        <td>0.9988</td>
        <td>0.9988</td>
      </tr>
      <tr>
        <td>A</td>
        <td>0.9136</td>
        <td>0.9964</td>
      </tr>
      <tr>
        <td>E</td>
        <td>1.0</td>
        <td>1.0</td>
      </tr>
      <tr>
        <td>F</td>
        <td>0.803</td>
        <td>0.9985</td>
      </tr>
      <tr>
        <td>J</td>
        <td>0.7143</td>
        <td>0.9998</td>
      </tr>
      <tr>
        <td>L</td>
        <td>0.9942</td>
        <td>0.9986</td>
      </tr>
      <tr>
        <td>N</td>
        <td>0.9804</td>
        <td>0.9822</td>
      </tr>
      <tr>
        <td>R</td>
        <td>0.9945</td>
        <td>0.9999</td>
      </tr>
      <tr>
        <td>V</td>
        <td>0.9322</td>
        <td>0.9917 </td>
      </tr>
      <tr>
        <td>a</td>
        <td>0.6933</td>
        <td>0.9998</td>
      </tr>
      <tr>
        <td>e</td>
        <td>0.25</td>
        <td>0.9999 </td>
      </tr>
      <tr>
        <td>f</td>
        <td>0.9695</td>
        <td>0.9981</td>
      </tr>
      <tr>
        <td>j</td>
        <td>0.8</td>
        <td>0.9991</td>
      </tr>
      <tr>
        <td>x</td>
        <td>0.8969</td>
        <td>0.9999</td>
      </tr>
    </table>
  </div>

</div>

* Confusion Matrix
<div style="display: flex; justify-content: space-around; align-items: center; text-align: center;">

  <div style="margin-right: 10px;">
    <h3>Train</h3>
    <img src="Resources/CM_MIT_Lead2_Train.png" alt="Image 1" style="width: 600px; height: auto;">
  </div>

  <div style="margin-left: 10px;">
    <h3>Test</h3>
    <img src="Resources/CM_MIT_Lead2_Test.png" alt="Image 2" style="width: 600px; height: auto;">
  </div>

</div>