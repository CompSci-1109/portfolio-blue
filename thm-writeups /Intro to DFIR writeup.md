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

The room also gave a hands-on site in which 




