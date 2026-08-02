# DC-Position-Control-System
## Aim:
To control the position of motor having the following specifications using MATLAB.<br>
(J)     moment of inertia of the rotor =    0.02 kg.m^2<br>
(b)     motor viscous friction constant =    0.002 N.m.s<br>
(Ktf)    motor torque constant   =           1.5 N.m/Amp<br>
(Ra)    armature resistance  =              2 Ohm<br>
(La)     armature inductance  =              0.5 H<br>
(Kb)      back emf constant = 0.5<br>
## Apparatus Required:
Computer with MATLAB software
## Theory: 
The speed of a DC motor is directly proportional to armature voltage and inversely proportional to flux. In field controlled DC motor the armature voltage is kept constant and the speed is varied by varying the flux of the machine. Since flux is directly proportional to field current, the flux is varied by varying field current.

The speed control system is an electro-mechanical control system. The electrical system consists of armature and field circuit but for analysis purpose, only field circuit is considered because the armature is excited by a constant voltage. The mechanical system consists of the rotating part of the motor and the load connected to the shaft of the motor. The field controlled DC motor speed control system is shown in the below figure. For this field controlled DC motor we shall find transfer function.
<img width="722" height="237" alt="image" src="https://github.com/user-attachments/assets/6f34d378-76ea-4467-b6dc-c859960cf55d" />

Let Rf = Field resistance Lf = Field inductance if = Field current Vf= Field voltage T = Torque developed by motor Ktf = Torque constant J = Moment of inertia of rotor and load The equivalent circuit of field is shown in the below figure. image
<img width="322" height="303" alt="image" src="https://github.com/user-attachments/assets/c83661f0-4ccf-4d95-9da9-fead65ac35ef" />

By Kirchoff ‘s voltage law, we can write image The torque of DC motor is proportional to product of flux and armature current. Since armature current is constant in this system, the torque is proportional to flux alone, but flux is proportional to field current. T ∝ if

                                                   Torque , T = Ktf if        

The mechanical system of the motor is shown in the below figure. image
<img width="407" height="100" alt="image" src="https://github.com/user-attachments/assets/aa5d8070-f75e-427e-a54e-1958abda0ac0" />

The differential equation governing the mechanical system of the motor is given by, image 
<img width="263" height="92" alt="image" src="https://github.com/user-attachments/assets/f1ea6b30-1514-4c6b-a43c-34db0319748e" />

On taking Laplace transform of the above equations with zero initial condition we get, image
<img width="632" height="197" alt="image" src="https://github.com/user-attachments/assets/5570bb73-f4fa-42f0-b8f5-aefda4643496" />

Equating equations (2) & (3) we get,
<img width="917" height="182" alt="image" src="https://github.com/user-attachments/assets/d0bc2875-a9ea-4e79-9ea2-df836bdf4434" />

The equation (1) can be written as
<img width="646" height="75" alt="image" src="https://github.com/user-attachments/assets/1e9cbd81-b005-4262-abd8-fa82ee6cb15b" />
<img width="303" height="137" alt="image" src="https://github.com/user-attachments/assets/6a6a4ca3-e2b1-4b58-9e6d-a767c72b9948" />


## Procedure:
1.	Open MATLAB software
2.	Open a new script file.
3.	Type the program.
4.	Save and Execute the program.
5.	Analyse the output in open loop and closed loop.

## Program
kt=0.0274 Rf=4 Lf=2.75E-6 J=3.2284E-6 B=3.5077E-6 s=tf('s') ol_sys=kt/((Rf+Lfs)(Jss+B*s)) subplot(2,1,1) step(ol_sys) title('open loop response') cl_sys=feedback(ol_sys,1) subplot(2,1,2) step(cl_sys) title('closed loop response')

## Output
<img width="1686" height="960" alt="image" src="https://github.com/user-attachments/assets/62dfd7f3-3259-4df7-bfb2-a79850df5449" />

## Result
Thus, the position of dc motor is controlled using MATLAB. 
