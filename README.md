

# BPSK Modulation Design 
This project simulates the designed BPSK Modulation circuit to determine its performance characterisitics pre-layout. 

# Note: This circuit does not work as expected, as of now it is just a simulation of the circuit that i build in esim. It works partially, but still i am uploading this for the sake of hackathon. If possible consider it for evaluation. thanks a lot i have learnt a lot form this hackathon.

## BPSK Modulation

Direct-digital modulation is gaining traction for its potential 
cost-effectiveness and performance benefits, particularly in 
mobile communications. BPSK modulation is widely used in 
systems like CDMA 2000, GPS, and RFID. Standard methods of 
BPSK modulation include reflection-type topologies , Gilbert
cell mixers , and ring-mixers . Many modulators rely on 
passive transmission-line couplers, which require high carrier 
frequencies to achieve on-chip scalability; however, this is 
challenging in CMOS due to silicon's low resistivity, which 
causes significant transmission losses at high frequencies. An 
alternative approach uses an active balun to produce a 180° 
phase shift, making it better suited to CMOS applications.


## Block Diagram of the BPSK Modulation

 <p align="center">
  <img width="800" height="500" src="/Images/block_diagram.png">
</p>




## Circuit Diagram of the BPSK Modulation

 <p align="center">
  <img width="800" height="500" src="/Images/bpsk_circuit.png">
</p>



## BPSK Modulation Performance Parameters 

| Parameter| Description| Min | Type | Max | Unit | Condition |
| :---:  | :-: | :-: | :-: | :---:  | :-: | :-: |
|Technology| 0.18 µm CMOS Process |
|RL|Load resistance at Vbgp terminal | 10|||kohm|VDD=5V, T=27C|
|Vout|Output voltage|0.5634|0.6345|0.6923|V|VDD=2.7V to VDD=5V, T=27C|
|TC_vout|Temperature Coefficient||26.2663||T=-40 to 125C, VDD=5V|
|Tstart|Start up time||10||us|Vdd=5v, T=27C|
|VDD|Supply Voltage||5||V|T=-40C to 125C|
|IDD|Supply Current||2.5747||mA|EN=1|

## Pre-Layout Performance Characteristics

###  Vout v/s VDD [ 3V - 5V]


 <p align="center">
  <img width="800" height="500" src="/Images/vout_vs_vdd.png">
</p>

###  message signal


 <p align="center">
  <img width="800" height="500" src="/Images/input.png">
</p>

###  carrier signal


 <p align="center">
  <img width="800" height="500" src="/Images/input.png">
</p>

###  modulation output


 <p align="center">
  <img width="800" height="500" src="/Images/modulated_bpsk.png">
</p>



## Tools used are eSim and ngspice

### Installing Ngspice

#### For Ubuntu

Open your terminal and type the following to install Ngspice
```
$  sudo apt-get install -y ngspice
```

## Running the Simulation


To enter the Ngspice Shell, open the terminal & type:
```
$ ngspice
```
To simulate a netlist, type:
```
ngspice 1 ->  source <filename>.cir
```

You can exit from the Ngspice Shell by typing:
```
ngspice 1 ->  exit
```
### Pre-Layout Simulation

To clone the Repository and download the Netlist files for Simulation, enter the following commands in your terminal.

```
$  sudo apt install -y git
$  git clone https://github.com/Rohith-DR/BPSK_Modulator
$  cd BPSK_Modulator/Simulation/Ngspice_Simulation/Final_Simulation/PreLayout
```




### To obtain the output


Run the netlist file using the following command.
```
$  ngspice bpsk.cir
```

## Contributors 

- **Rohith DR** 
- **Kunal Ghosh** 
- **Sumanto Kar** 



## Acknowledgments


- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
- NIT Jamshedpur
- VSD(VLSI System Design)
- Global academy of technology

## Contact Informaion

- Rohith DR, Undergraduate Student, Global academy of technology, rohith200317@gmail.com
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com


