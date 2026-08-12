# Takeaways From the Intro to DFIR room in TryHackMe:

link to the room: https://tryhackme.com/room/introductoryroomdfirmodule

DFIR: Digital Forensics & Incident Response

# Digital Forensics = 

- Finding evidence of attacker activity and differentiating between false alarms and actual incidents. 
- Consists of Identification and scoping . (Identification : understanding the type of attack and /or threat , Scoping : Examining the impact of the attack and its attack radius)

# Incident Response =

Containment of the attack, reducing damage/breach and Eradication of attacker and the attacker's persistence mechanisms and malware/ harmful files.


# In DFIR:

- Evidence / artifacts obtained must be preserved carefully. The copy of the evidence is first write-protected and then another copy of this write-protected evidence is made and THIS COPY is analysed.
- ANY person unrelated to the investigation should not have the data/ evidence. chain of custody is preserved in this way. (CoC means the lifecycle of the evidence in the case until it is presented at the court).
- Try to preserve data which lives in highly volatile storage device (e.g. RAM chips) sooner than the data in SSD or HDD. ( highly volatile data must be preserved first, this is called as order of Volatility).
- A proper chronological sheet of the events in the attack must be prepared based on the evidence gathered. (this is called timeline creation).


# The Hands-On:

The room also gave a hands-on site in which :

- I identified a malicious alert and collected evidence regarding the alert in the logs, ultimately arranging them chronologically.
- the SIEM as given in the site alerted abt a malicious alert , so upon investigating within the SIEM it was found that an external IP (202.22.241.34) (this was the source IP) tried to login to a private network's IP (192.168.1.150) . The Syslog showed evidence of a potential SSH Bruteforce attack (initially in the SIEM SSH connection attempt by the source to the destination was observed.)
- The compromised device then executed the malicious file downloaded from the source IP.

#  Some DFIR Tools mentioned:

Eric Zimmermann's too, redline, KAPE, Autopsy, Volatility, Velociraptor

# The Incident Response Process:

 Orgs such as NIST and  SANS have published processes & handbooks to guide on how to perform a successful Incident Response process. Both of them are almost similar. Thus the overall Incident Response Process can be summarized into the acronym PICERL.

 
<img width="1530" height="118" alt="image" src="https://github.com/user-attachments/assets/d0aacb93-600f-4789-af23-9495f3b1dd38" />




