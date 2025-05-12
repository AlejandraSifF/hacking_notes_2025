#### Description

A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/bdda31c79c31975a5fe5402777bc87794655172e5d5bb2b569f1970df8efda34/myNetworkTraffic.pcap) and try to get the flag.

#### Consejos:
1.  Filter your packets to narrow down your search.
2. Attacks were done in timely manner.
3. Time is essential
   
## Solución 

```
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_af160980}
```

#### Usando Wireshark  y cyberchef:
![[Pasted image 20250512154003.png]]

#### Usando termianl de linux `tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame -dme -e tcp.segment_data | sort -k4 | awk '{print $6}' | xxd -p -r | base64`:

```
yoli@Yoli:~/Fundamentos_Seguridad/Tarea_3-Forensic/9-Ph4nt0m_1ntrud3r$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4"
    3   0.005156  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=12
    5   0.003740  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=12
    7   0.003276  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=12
   10   0.005398  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Out-Of-Order] [Illegal Segments]
   14   0.004931  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Retransmission] 20 → 80 [SYN] Seq=0 Win=8192 Len=12
   16   0.005617  192.168.0.2 → 192.168.1.2  TCP 44 [TCP Out-Of-Order] 20 → 80 [SYN] Seq=0 Win=8192 Len=4
   22   0.003511  192.168.0.2 → 192.168.1.2  TCP 52 [TCP Retransmission] 20 yoli@Yoyoli@Yolyoli@Yoli:~yoli@Yoli:~/yoli@Yoli:~/Fundamentos_Seguridad/Tarea_3-Forensic/9-Ph4nt0m_1ntrud3r$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" - T fielda -e frame.time
tshark: Display filters were specified both with "-Y" and with additional command-line arguments.
yoli@Yoli:~/Fundamentos_Seguridad/Tarea_3-Forensic/9-Ph4nt0m_1ntrud3r$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" - T fields -e frame.time
tshark: Display filters were specified both with "-Y" and with additional command-line arguments.
yoli@Yoli:~/Fundamentos_Seguridad/Tarea_3-Forensic/9-Ph4nt0m_1ntrud3r$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time
Mar  5, 2025 21:32:24.616727000 CST
Mar  5, 2025 21:32:24.615311000 CST
Mar  5, 2025 21:32:24.614847000 CST
Mar  5, 2025 21:32:24.616969000 CST
Mar  5, 2025 21:32:24.616502000 CST
Mar  5, 2025 21:32:24.617188000 CST
Mar  5, 2025 21:32:24.615082000 CST
yoli@Yoli:~/Fundamentos_Seguridad/Tarea_3-Forensic/9-Ph4nt0m_1ntrud3r$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time -e tcp.segment_data
Mar  5, 2025 21:32:24.616727000 CST     596d68664e484a6659513d3d
Mar  5, 2025 21:32:24.615311000 CST     626e52666447673064413d3d
Mar  5, 2025 21:32:24.614847000 CST     63476c6a62304e5552673d3d
Mar  5, 2025 21:32:24.616969000 CST     5a6a45324d446b344d413d3d
Mar  5, 2025 21:32:24.616502000 CST     587a4d3063336c6664413d3d
Mar  5, 2025 21:32:24.617188000 CST     66513d3d
Mar  5, 2025 21:32:24.615082000 CST     657a46305833633063773d3d
yoli@Yoli:~/Fundamentos_Seguridad/Tarea_3-Forensic/9-Ph4nt0m_1ntrud3r$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time -e tcp.segment_data | sort -k4
Mar  5, 2025 21:32:24.614847000 CST     63476c6a62304e5552673d3d
Mar  5, 2025 21:32:24.615082000 CST     657a46305833633063773d3d
Mar  5, 2025 21:32:24.615311000 CST     626e52666447673064413d3d
Mar  5, 2025 21:32:24.616502000 CST     587a4d3063336c6664413d3d
Mar  5, 2025 21:32:24.616727000 CST     596d68664e484a6659513d3d
Mar  5, 2025 21:32:24.616969000 CST     5a6a45324d446b344d413d3d
Mar  5, 2025 21:32:24.617188000 CST     66513d3d
yoli@Yoli:~/Fundamentos_Seguridad/Tarea_3-Forensic/9-Ph4nt0m_1ntrud3r$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time -e tcp.segment_data | sort -k4 | awk '{print $6}'
63476c6a62304e5552673d3d
657a46305833633063773d3d
626e52666447673064413d3d
587a4d3063336c6664413d3d
596d68664e484a6659513d3d
5a6a45324d446b344d413d3d
66513d3d
yoli@Yoli:~/Fundamentos_Seguridad/Tarea_3-Forensic/9-Ph4nt0m_1ntrud3r$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time -e tcp.segment_data | sort -k4 | awk '{print $6}' | xxd -p -r
cGljb0NURg==ezF0X3c0cw==bnRfdGg0dA==XzM0c3lfdA==YmhfNHJfYQ==ZjE2MDk4MA==fQ==yoli@Yoli:~/Fundamentos_Seguridad/Tarea_3-Forensic/9-Ph4nt0m_1ntrud3r$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame -dme -e tcp.segment_data | sort -k4 | awk '{print $6}' | xxd -p -r | base64
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_af160980}yoli@Yoli:~/Fundamentos_Seguridad/Tarea_3-Forensic/9-Ph4nt0m_1ntrud3r$ 
```
