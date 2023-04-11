# Dataset- Handovers
Dataset of Human Human Handovers
![Handover_human_human_experimentation](https://user-images.githubusercontent.com/19911432/230441574-1e8edb41-a462-4c59-a0ca-970653c5f2cf.jpg)

A total of 13 participant pairs (26 participants involved). For each pair, they were assigned participant 1 and participant 2. The baton was transferred to and fro between them. The baton has 2 6D Force/Torque sensors on sides for recording the grip forces and one sensor in between for interaction force. The particpants wear motion capture suits (MoCap) and the experiment occured in a MoCap room. The upeer body movement and the baton pose is tracked.

The Experimentation done in sets of approximately 9 minutes each. We had three experimental settings:
1. Setting1- Normal baton transfer - 0.8 kg baton , Set 1 and Set 2
2. Setting2- Heavy baton transfer - 1.8 kg baton , Set 3 and Set 4
3. Setting3- Giver vision impairment with normal baton - 0.8 kg, Set 5 and Set 6

The data set is provided for each participant pair for each settting and corresponding set. Example: Pair1/Setting1/Set1

**Order** of sets in experimentation for:

**Pair 1 : Set1 Set3 Set5 Set2 Set4 Set6**
**Pair 2 : Set1 Set3 Set2 Set5 Set4 Set6**
**Pair 3 : Set1 Set5 Set2 Set3 Set6 Set4**
**Pair 4 : Set1 Set3 Set2 Set5 Set4 Set6**
**Pair 5 : Set1 Set3 Set5 Set2 Set6 Set4**

**Pair 6 : Set1 Set3 Set5 Set2 Set6 Set4**
**Pair 7 : Set1 Set3 Set2 Set5 Set4 Set6**
**Pair 8 : Set1 Set3 Set5 Set2 Set6 Set4**
**Pair 9 : Set1 Set5 Set2 Set3 Set6 Set4**
**Pair 10 : Set1 Set3 Set2 Set5 Set4 Set6**
**Pair 11 : Set1 Set3 Set5 Set2 Set6 Set4**
**Pair 12 : Set1 Set5 Set2 Set3 Set6 Set4**
**Pair 13 : Set1 Set3 Set5 Set2 Set6 Set4**

Each Set data has 2 zipped folders: 'handovers' and 'handovers_reverse'. The 'handovers' folder contains all recorded and segmented handovers as separate folders when participant 1 acts as giver and passed the baton to participant 2, who acted as taker. The 'handovers_reverse' contains all handovers when participant 2 acted as giver and participant 1 as taker. This is done for purely analytical purposes. 



Each handover folder has 30 .csv files, with 801 rows implying the saved duration (@120 Hz = 6.675 seconds) of the handover representing:
1. Wrench Taker - Fx,Fy,Fz,Tx,Ty,Tz (6 columns with title/header in first row)
2. Wrench Giver - Fx,Fy,Fz,Tx,Ty,Tz
3. Wrench Interaction- Fx,Fy,Fz,Tx,Ty,Tz
4. Baton pose -  x,y,z,q0,q1,q2,q3 (7 columns with title/header in first row)
5. 5-17. Giver upper body skeletal representation- pose of 13 individual frames
6. 18-30 Taker upper body skeletal representation- pose of 13 individual frames

Above can be seen in the handover_Sample folder provided which has data of a sample handover. The grip forces are given by -Fz from giver/taker wrench.


Please note the transformation in forces done for the interaction sensor for the reverse_handovers case, based on observed data from sensor:
1. Fx = -1*Fx_int_measured
2. Fy = -1*Fy_int_measured
3. Fz = -1*Fz_int_measured
4. Tx = -1*Tx_int_measured
5. Ty = -1*Ty_int_measured
6. Tz = -1*Tz_int_measured


The F/T HEX sensors from Onrobots : https://onrobot.com/en/products/hex-6-axis-force-torque-sensor
Datasheet: https://onrobot.com/sites/default/files/documents/Datasheet_HEX_QC_v1.3_EN.pdf


The MoCap setup from Motive: https://optitrack.com/
The setup used:
Software- MOTIVE 3.0
Cameras-
8x PrimeX13 Cameras (along the sides of the room)
4x PrimeX13W Wide-angle Cameras (in the corners of the room)
