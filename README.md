# Netcat's ability to copy a file from one system to another.
Having Netcat either on a windows system (nc64) or linux (nc) you can transfer a file from one system to another.
## Overview: Doing a simple transfer of a txt file from a kali VM to a Metasotable VM over a network.

I have a text file located on my Kali VM called Bobsfile.txt.

<img width="569" height="157" alt="1" src="https://github.com/user-attachments/assets/d188d0de-3e2d-4485-9a66-f346cd8f5a07" />

Here it is a nano

<img width="1598" height="713" alt="2" src="https://github.com/user-attachments/assets/97757327-dbd3-4b3e-9d7a-e5d17a70efc0" />


On the metasploitable VM I will need to know my IP address

<img width="757" height="167" alt="5" src="https://github.com/user-attachments/assets/79267abb-6857-4a0a-88f1-9f3d53afce53" />


Next we are going to set up netcat to listen and receive our file from our Kali machine via standard output re-direction.
We will accept the incoming txt file as inbox.txt

<img width="704" height="244" alt="4" src="https://github.com/user-attachments/assets/fa5afb8f-b68c-4c3d-a0ee-900e84f15016" />
