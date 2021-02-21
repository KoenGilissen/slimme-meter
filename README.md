# slimme-meter
https://www.raspberrypi.org/forums/viewtopic.php?t=21025 </br>
https://www.raspberrypi.org/forums/viewtopic.php?f=36&t=12335 </br>
https://www.reddit.com/r/raspberry_pi/comments/2ut4vb/built_a_nodejs_service_to_allow_the_pi_to_turn/ </br>
https://github.com/jasbur/RaspiWiFi </br>
https://googlecreativelab.github.io/coder/ </br>
https://github.com/sabhiram/raspberry-wifi-conf </br>
https://github.com/RaspAP/raspap-webgui </br>

Stap 1: activeer slimme meter via fluvius
https://www.fluvius.be/nl/thema/meters-en-meterstanden/activeer-desactiveer-je-gebruikerspoorten

Stap 2: connect device

Stap 3: connect to wifi


Ontwikkeling:
1) headless image met wifi portal config </br>
https://github.com/jasbur/RaspiWiFi  <<-- Image needed for headless wifi config </br>
 a) raspi-config to enable SSH GPIO Serial etc... </br>

2) installatie Grafana </br>
a) find latest package for raspberry pi zero: https://dl.bintray.com/fg2it/deb-rpi-1b/main/g/ </br>

sudo apt-get install adduser libfontconfig </br>
curl -L https://dl.bintray.com/fg2it/deb-rpi-1b/main/g/grafana_5.1.4_armhf.deb -o /tmp/grafana_5.1.4_armhf.deb </br>
sudo dpkg -i /tmp/grafana_5.1.4_armhf.deb </br>

sudo systemctl daemon-reload </br>
sudo systemctl enable grafana-server && sudo systemctl start grafana-server </br>

3) Installatie influxdb </br>
curl -sL https://repos.influxdata.com/influxdb.key | sudo apt-key add - </br>
source /etc/os-release </br>
sudo apt-get update && sudo apt-get install influxdb</br>
sudo systemctl start influxdb</br>





