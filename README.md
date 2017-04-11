# Project 10 - Honeypot

Time spent: **2** hours spent in total

> Objective: Setup a honeypot and provide a working demonstration of its features.

### Required: Overview & Setup

- [x] A basic writeup (250-500 words) on the `README.md` desribing the overall approach, resources/tools used, findings

     I first attempted to create a honeypot using vagrand, but I kept receiving an error that the key algorithm setting was incorrect so I attempted to find another way of setting up a honeypot. The tool that I used to set up the honey pot was pentbox, which is a ruby application that can help with a number of different things. Some of the things that pentbox gives you are Cryptogrophay ools, Ip Grabbers, and geolocation using IP, but most importantly it allowed me to create a honeypot. After setting up the honeypot on port 8080, I attempted to connect to and enter the computer through port 8080, which resulted in the honey pot alerting me to a possible intrusion. The honey pot also saves a log of intrusions in a log file. This would be considered an example of a low-interaction honeypot because it doesn't allow the user to connect to a webserver. Instead, it will just pick up information about any user that attempts to connect to the honeypot.

- [x] A specific, reproducible honeypot setup, ideally automated. There are several possibilities for this:
	- A Vagrantfile or Dockerfile which provisions the honeypot as a VM or container
	- A bash script that installs and configures the honeypot for a specific OS
	- Alternatively, **detailed** notes added to the `README.md` regarding the setup, requirements, features, etc.

### Required: Demonstration

- [x] A basic writeup of the attack (what offensive tools were used, what specifically was detected by the honeypot)

	The attack did not really require any offensive tools. The only thing I needed to do was to try to access the webpage and the honeypot would inform me of an attempted intrusion. The honeypot was created using pentbox1.8.

- [x] An example of the data captured by the honeypot (example: IDS logs including IP, request paths, alerts triggered)
	
	The honeypot tells you that an intrusion was detected and the ip from, which it was attempted. It lets you know the type of request, GET or POST, as well as what connection type was used, the cache control, how the attack was conducted, the time that it happened, and much more useful information that can be seen in the screen-cap.

- [x] A screen-cap of the attack being conducted
    
	<img src='http://i.imgur.com/fA23pdP.png' title='Honeypot Attack' width='' alt='Honeypot Attack' />


### Optional: Features
- Honeypot
	- [ ] HTTPS enabled (self-signed SSL cert)
	- [ ] A web application with both authenticated and unauthenticated footprint
	- [ ] Database back-end
	- [ ] Custom exploits (example: intentionally added SQLI vulnerabilities)
	- [ ] Custom traps (example: modified version of known vulnerability to prevent full exploitation)
	- [ ] Custom IDS alert (example: email sent when footprinting detected)
	- [ ] Custom incident response (example: IDS alert triggers added firewall rule to block an IP)
- Demonstration
	- [ ] Additional attack demos/writeups
	- [ ] Captured malicious payload
	- [ ] Enhanced logging of exploit post-exploit activity (example: attacker-initiated commands captured and logged)
