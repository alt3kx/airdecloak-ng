# Airdecloak-ng
My Aircrack-ng contribution with Thomas d'Otreppe

# Description
Airdecloak-ng is a tool that removes wep cloaking from a pcap file. Some WIPS (actually one) actively “prevent” cracking a WEP key by inserting chaff (fake wep frames) in the air to fool aircrack-ng. In some rare cases, cloaking fails and the key can be recovered without removing this chaff. In the cases where the key cannot be recovered, use this tool to filter out chaff.

The program works by reading the input file and selecting packets from a specific network. Each selected packet is put into a list and classified (default status is “unknown”). Filters are then applied (in the order specified by the user) on this list. They will change the status of the packets (unknown, uncloaked, potentially cloaked or cloaked). The order of the filters is really important since each filter will base its analysis amongst other things on the status of the packets and different orders will give different results.

Important requirement: The pcap file needs to have all packets (including beacons and all other “useless” packets) for the analysis (and if possible, prism/radiotap headers).

# Official Project and Credits
https://www.aircrack-ng.org/doku.php?id=airdecloak-ng

# Author 
Thomas d'Otreppe <tdotreppe@aircrack-ng.org>

# Contributor 
Alex Hernandez aka <em><a href="https://twitter.com/_alt3kx_" rel="nofollow">(@\_alt3kx\_)</a></em>
