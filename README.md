# Dataset
Dataset of Human Human Handovers

A total of 13 participant pairs (26 participants involved). For each pair, they were assigned participant 1 and participant 2. Experimentation done in sets of approximately 9 minutes each. We had three experimental settings:
1. Setting1- Normal baton transfer - 0.8 kg baton , Set 1 and Set 2
2. Setting2- Heavy baton transfer - 1.8 kg baton , Set 3 and Set 4
3. Setting3- Giver vision impairment with normal baton - 0.8 kg, Set 5 and Set 6

The data set is provided for each participant pair for each settting and corresponding set. Example: Pair1/Setting1/Set1

Each Set data has 2 zipped folders: 'handovers' and 'handovers_reverse'. The 'handovers' folder contains all recorded and segmented handovers as separate folders when participant 1 acts as giver and passed the baton to participant 2, who acted as taker. The 'handovers_reverse' contains all handovers when participant 2 acted as giver and participant 1 as taker. This is done for purely analytical purposes. 

Each handover folder has 30 .csv files, with 801 rows implying the saved duration (@120 Hz = 6.675 seconds) of the handover representing:
1. Wrench Taker - Fx,Fy,Fz,Tx,Ty,Tz (6 columns with title/header in first row)
2. Wrench Giver - Fx,Fy,Fz,Tx,Ty,Tz
3. Wrench Interaction- Fx,Fy,Fz,Tx,Ty,Tz
4. Baton pose -  x,y,z,q0,q1,q2,q3 (7 columns with title/header in first row)
5-17. Giver upper body skeletal representation- pose of 13 individual frames
18-30 Taker upper body skeletal representation- pose of 13 individual frames




Please note the transformation in forces done for the interaction sensor for the reverse_handvoers case, based on observed data from sensor:
1. F_x = -1*F_x_int_measured
2. F_y = -1*F_y_int_measured
3. F_z = F_z_int_measured

The F/T sensors from Onrobots
