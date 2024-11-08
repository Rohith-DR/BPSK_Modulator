# BPSK_Modulator
A CMOS Direct-Digital BPSK Modulator
This project simulates the BPSK Modulator circuit to determine its performance characterisitics pre-layout.

# Note: The circuit does not meet the actual requirement, and the design still requires modification as it is not completed as per the requirement. but still i am uploading this circuit till where i was able to complete. if possible cosider it. I have learnt a lot by this hackathon thanks a lot.

## about the BPSK Modulator

Direct-digital modulation is gaining traction for its potential cost-effectiveness and performance benefits, particularly in mobile communications. BPSK modulation is widely used in systems like CDMA 2000, GPS, and RFID. Standard methods of BPSK modulation include reflection-type topologies, Gilbert-cell mixers , and ring-mixers. Many modulators rely on passive transmission-line couplers, which require high carrier frequencies to achieve on-chip scalability; however, this is challenging in CMOS due to silicon's low resistivity, which causes significant transmission losses at high frequencies. An alternative approach uses an active balun to produce a 180° phase shift, making it better suited to CMOS applications.

## Block Diagram of the BPSK Modulator

 <p align="center">
  <img width="800" height="500" src="/Images/block_diagram.png">
</p>




## Circuit Diagram of the BPSK Modulator

 <p align="center">
  <img width="800" height="500" src="/Images/bpsk_circuit.png">
</p>



## Bandgap Performance Parameters 

| Parameter| Description| Min | Type | Max | Unit | Condition |
| :---:  | :-: | :-: | :-: | :---:  | :-: | :-: |
|Technology| 0.18 µm CMOS Process |
|RL|Load resistance at Vbgp terminal | 10|||Kohm|VDD=5V, T=27C|
|Vout|Output voltage|0.5634|0.6345|0.6923|V|VDD=2.7V to VDD=5V, T=27C|
|TC_vout|Temperature Coefficient||26.2663||ppm/C|T=-40 to 125C, VDD=5V|
|Tstart|Start up time||10||us|Vdd=5v, T=27C|
|VDD|Supply Voltage||5||V|T=-40C to 125C|
|IDD|Supply Current||2.5747||mA|EN=1|



## Pre-Layout Performance Characteristics

###  Vout v/s VDD [ 3V - 5V]


 <p align="center">
  <img width="800" height="500" src="/Images/vout_vs_vdd.png">
</p>

###  carrier signal


 <p align="center">
  <img width="800" height="500" src="/Images/input.png">
</p>

###  modulated signal 


 <p align="center">
  <img width="800" height="500" src="/Images/modulated_bpsk.png">
</p>


## Tools used are eSim/ngspice 

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

exit from the Ngspice Shell by typing:
```
ngspice 1 ->  exit
```

### Pre-Layout Simulation

To clone the Repository and download the Netlist files for Simulation, enter the following commands in your terminal.

```
$  sudo apt install -y git
$  git clone https://github.com/Rohith-DR/BPSK_Modulator
$  cd BPSK_Modulato/Simulation/Ngspice_Simulation/Final_Simulation/PreLayout
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
- Sumanto Kar.
- NIT Jamshedpur.
- VSD(Vlsi System Design).
- Global Academy of Technology

## Contact Information

- Rohith DR, Undergraduate Student, Global Academy of Technology rohith200317@gmail.com
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com
