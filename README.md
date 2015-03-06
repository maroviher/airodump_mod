<b>Improved version of airodump-ng with ability to kick-off a stations from AP. To start attack on a particular AP, select it (TAB and arrow up/down) and then push the right arrow button, to stop an attack select an AP, that is currently under attack, and push left arrow button. You can attack only WPA2/WPA APs. If the encryption of AP changes on-fly to WEP or OPEN (admin has changed it), than <b>airodump_mod</b> will immediately stop an attack until the encryption will be changed to WPA2/WPA again.</b><br><br>
What is better than in original airodump-ng?<br>
* show more statistics: packets/sec, bytes sniffed, currently sniff rate bytes/sec, beacons sniffed, packets sniffed
* selection: if you have selected an AP (TAB button), and another APs will be found and inserted on top, your selection will not be moved. That is very annoying in original airodump-ng
* show client manufacturer (toggle with 'b' button). Dont forget to download OUI file, just run scripts/airodump-ng-oui-update
* toggle client statistics with 'g' button, sniffed packets: (EAPOL/AssocReq/AssocResp/ReAssocReq/ReAssocResp/ProbeRequest/ProbeResp/Disass/Auth/Deauth). Very usefull to see how many times a client tries to reconnect.<br><br>
<b>Installation steps</b>
git clone https://github.com/maroviher/airodump_mod.git<br>
cd airodump_mod/<br>
make uninstall #uninstall currently installed aircrack suite, if any
git checkout origin/kick_off<br>
git checkout -b kick_off origin/kick_off<br>
libnl=false make -j4<br>
libnl=false make install<br>
scripts/airodump-ng-oui-update #download MAC manufacturer database<br>
make install
