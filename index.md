### Hand-tremor frequency estimation in videos

This dataset was created as part of a larger study on developing patient-friendly techniques for objective quantification of motor (dys)function in patients with neurological disorders. 

This work was supported by the Netherlands Organisation for Scientific Research (NWO) [Technology in Motion research programme, project 628.004.001]. 

The funding party played no role in the study design, in the collection, analysis and interpretation of
data, or in the decision to submit the dataset or related manuscripts for publication.

________________

The dataset documentation can be found [here](https://github.com/SilviaLauraPintea/hand-tremor/TIM-Tremor.pdf).

For each patient recording we provide a directory following the naming convention: 
*T0xx [Left/Right]*, where T0xx denotes a given recording number, and Left/Right indicates the mirrored arm on which the accelerometers were positioned. 

Within each patient directory, a set of subdirectories are found, containing the recordings for the set of tasks performed for that patient. 
Within each recording directory for every task, we store:

```markdown
1. The RGB video segment: *kinect.avi*.
  - Sampling rate: 30 frames/second.
  - Size: 1920 px × 1080 px.
  
2. The corresponding Kinect depth recording, encoded as a grayscale video: *kinect_depth.avi*.
  - Sampling rate: 30 frames/second.
  - Size: 512 px x 424 px.
  (The transformation from the stored depth image values to mm can be performed by applying the scaling: 4000 / 255.)

3. The Kinect depth recording spatially aligned with the RGB video, also encoded as a grayscale video: *kinect_map.avi*.
  - Sampling rate: 30 frames/second.
  - Size: 1920 px × 1080 px.
  
4. The corresponding accelerometer recordings obtained from the two sensors used: *kinect_accelerometer.tsv*
  - Sampling rate: 1000 samples /second.
  - 9-column recording, in “tab-separated” format: (1) sensor-1 x, (2) sensor-1 y, (3) sensor-1 z, (4) ignore, (5) sensor-2 x, (6) sensor-2 y, (7) sensor-2 z, (8) ignore, (9) ignore.
  Columns 4 and 8 of the accelerometer recordings should be ignored, because there was no input on these channels. Column 9 should also be ignored, it contains a digital value that was not used (and therefore not properly set/meaningful).
```

We provide a labeling file: *[TIM-tremor-labeling.csv](https://github.com/SilviaLauraPintea/hand-tremor/TIM-tremor-labeling.csv)*, containing for every patient recording the following information, in “comma-separated” format:

```markdown
  1. The arm, as displayed in the video, on which the accelerometers are positioned.
  2. Tremor rating ranging from 0 to 10 of the left arm of the patient.
  3. Tremor rating ranging from 0 to 10 of the right arm of the patient.
  4. Five classes diagnosis: 0 - No convincing tremor, 1 - Parkinsonian tremor, 2 - Essential tremor, 3 - Dystonic tremor, 4 - Functional tremor, and 5 - Other (note: multiple labels can be present in one recording).
```
### Obtaining the data

1. Download, fill out, and sign the agreement [form](https://github.com/SilviaLauraPintea/hand-tremor/agreement_form.pdf).
*Note:* The person signing the agreement must hold a permanent position at an academic institution.

2. Using the institutional e-mail address, please send an e-mail to *P.J.M.van_Schaik-Bank [at] lumc.nl*, including the purpose of usage of the *TIM-Tremor* dataset, and the signed agreement form.

3. Once your request is processed, you will receive the download information via your institutional e-mail address.

### Citation

If you use this dataset please make sure to cite:

- S.L. Pintea, J. Zheng, X. Li, P.J.M. Bank, J.J. van Hilten, J.C. van Gemert. *“Hand-tremor frequency estimation in videos”*. European Conference on Computer Vision Workshop on Observing and Understanding Hands in Action (2018).
- P.J.M. Bank, S.L. Pintea, P.W. (Elma) Ouwehand, J. Zheng, J.C. van Gemert, J.J. van Hilten. *"Technology in Motion Tremor Dataset: TIM-Tremor"* (2018). 



