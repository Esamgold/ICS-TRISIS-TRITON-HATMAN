# ICS-TRISIS-TRITON-HATMAN
This repository contains original samples and decompiled sources of malware attacking commonly used in Industrial Control Systems (ICS) Triconex Safety Instrumented System (SIS) controllers. For more information scroll to "Learn More".
SIS  controller applications!
Emergency shutdown (ESD)
Turbine control (TMC)
Boiler management System (BMS)
Offshore fire & gas protection (F&G)
Nuclear
Any critical process
![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/e1b555c1-85b6-468e-b196-02dbaefd9fad)

![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/e4c3fd7d-8f3e-4a00-81c4-c8a4388f6934)

What is Safety Integrity Level (SIL)?![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/1e13afb8-d739-4821-b045-89c45edc8a56)
The internationally recognized safety standards fall into different buckets, which can be an issue. ISA 84 and IEC 61508/61511 are the safety standards. 
![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/3f6f612f-8adc-4ffc-8747-1f58e1ca40d4)
![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/7b4f1960-e900-441c-a235-28d1743e70ff)
![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/3faf8a7d-f8d9-4521-b0dd-2066fc01874a)

Triton![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/1915c0cd-6e36-46fa-b28e-5d16b8e97ca5)

TRITON is one of the few publicly known examples of malware targeting Industrial Control Systems (ICS), after Stuxnet, Havex, Blackenergy2 and Industroyer, and the first publicly known example of malware targeting industrial safety controllers specifically.

TRITON does not leverage any 0-days but instead reprograms the target safety controllers via the TriStation protocol ) which lacks authentication.

As the TriStation protocol is proprietary and undocumented this means the attacker had to reverse engineer it, possibly through a combination of using similarities with the documented Triconex System Access Application (TSAA) protocol.

By default, Ethernet communications for TSAA take place over UDP port 1500 while those for TriStation take place over UDP port 1502.

The Triconex controllers have a physical four-position key switch which can be set to either RUN - PROGRAM - STOP or REMOTE.
![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/72f7dbec-9342-482c-b4aa-f3bf383d1668)
![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/2fe53535-6c32-4024-9190-63e4bfcc1eda)

TRITON Framework![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/eb45e766-5c5c-4774-9cf9-c4922735ee4d)

TRITON Framework - The framework is written in Python and consists of the following components:TS_cnames.py: TsHi.py: TsBase.py: - TsLow.py:

The payload used in the incident can be thought of as a four-stage shellcode.-- Stage 1: Argument-Setter (PresetStatusField)--Stage 2: Implant Installer (inject.bin)--Stage 3: Backdoor Implant (imain.bin)--Stage 4: Missing OT Payload

![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/f3a249df-9038-41f0-8c40-d381ec20ff85)
![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/5e09ff29-e323-4859-a1b7-0831dd4f0939)

Affected Files by TRITON![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/a12c4a9d-e973-48d4-940c-bf64e03bce10)

![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/c28f451c-09b1-4afb-a512-58d12b5fae1a)

![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/99c3ac01-175f-421e-b649-2326359c7e5a)

TRITON Framework![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/a137b43a-6bae-43b1-902c-391b9c1df982)

![image](https://github.com/Esamgold/ICS-TRISIS-TRITON-HATMAN/assets/76063102/8a366077-df0e-4293-ab76-f82bddcdffb9)

Learn more
Technical Analysis:
https://www.dragos.com/wp-content/uploads/TRISIS-01.pdf 
https://www.youtube.com/watch?v=f09E75bWvkk 
https://www.slideshare.net/DragosInc/hunting-for-xenotime-and-the-next-big-thing 
https://www.mandiant.com/resources/blog/triton-attribution-russian-government-owned-lab-most-likely-built-tools 
https://github.com/NozomiNetworks/tricotools 
https://www.bsi.bund.de/DE/Themen/Industrie_KRITIS/ICS/Tools/RAPSN_SETS/RAPSN_SETS_node.html
