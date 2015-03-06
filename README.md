<b>Improved version of airodump-ng with ability to kick-off a stations from AP. To start attack on a particular AP just push the right arrow button, to stop attack select an AP, that is under attack and push left arrow button.</b><br><br>
What is better than in original airodump-ng?<br>
* show more statistics, packets/sec, etc...
* selection: if you have selected an AP (TAB button), and another APs will be found and inserted on top, your selection will not be moved. That is very annoying in original airodump-ng
* show client manufacturer (toggle with 'b' button). Dont forget to download OUI file, just run scripts/airodump-ng-oui-update
* toggle client statistics with 'g' button, sniffed packets: (EAPOL/AssocReq/AssocResp/ReAssocReq/ReAssocResp/ProbeRequest/ProbeResp/Disass/Auth/Deauth). Very usefull to see how many times a client tries to reconnect.<br><br>
git clone https://github.com/maroviher/airodump_mod.git<br>
git checkout origin/kick_off<br>
git checkout -b kick_off origin/kick_off<br>
make<br>
make install
