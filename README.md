# Netcat's ability to copy a file from one system to another.
Having Netcat either on a windows system (nc64) or linux (nc) you can transfer a file from one system to another.
## Overview: Doing a simple transfer of a txt file from a kali VM to a metasploitable VM over a network.

I have a text file located on my Kali VM called bobsfile.txt.

<img width="569" height="157" alt="1" src="https://github.com/user-attachments/assets/d188d0de-3e2d-4485-9a66-f346cd8f5a07" />

Here it is in nano

<img width="1598" height="713" alt="2" src="https://github.com/user-attachments/assets/97757327-dbd3-4b3e-9d7a-e5d17a70efc0" />


On the metasploitable VM I will need to know my IP address

<img width="757" height="167" alt="5" src="https://github.com/user-attachments/assets/79267abb-6857-4a0a-88f1-9f3d53afce53" />


Next we are going to set up netcat to listen and receive our file from our Kali machine via standard output re-direction.
We will accept the incoming bobfile.txt as inbox.txt

<img width="704" height="244" alt="4" src="https://github.com/user-attachments/assets/fa5afb8f-b68c-4c3d-a0ee-900e84f15016" />

Now back at our Kali system, we placed in our command:
This command tells netcat to take the data from bobsfile.txt and send it through the network using input redirection to the metasploitable
system.

<img width="386" height="181" alt="6" src="https://github.com/user-attachments/assets/91fa60e5-d7e4-47ab-a891-d8723318486f" />

The -w3 is a wait time of 3 seconds and then it terminates the connection.

<img width="445" height="211" alt="7" src="https://github.com/user-attachments/assets/fe9cf9d9-f587-492c-9acf-126788cb4c9d" />

When we go back to our metasploitable machine, we can see in the list content that inbox.txt is there. That is the bobsfile.txt
from the kali machine.

<img width="713" height="277" alt="8" src="https://github.com/user-attachments/assets/4e6198f2-d606-4e53-9981-d71aa0539074" />

let's display the inbox.txt contents using **cat** 

<img width="680" height="611" alt="9" src="https://github.com/user-attachments/assets/18c6630c-6737-4498-9820-a1aed7565413" />

<img width="827" height="597" alt="10" src="https://github.com/user-attachments/assets/9c6b2436-2802-45b3-9789-ddf39e6358bf" />


**In closing, We had our metasploitable system listen and receive a txt file called bobsfile.txt from our kali system as inbox.txt.**
