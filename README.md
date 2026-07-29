# Access-Point
I used two access point and dhcp relay to give wireless devices Ip addresses
I wanted to created two different Lan networks and supply wireless devices with Ip addresses via DHCP and wireless access points.
Devices:
Layer 3 switch 
Two access points
Four wireless devices
One wired endpoint device

I connected the access points to the layer 3 switch with a straight through copper cable.
I want to separate my networks logically so I created two vlans. vlan 20,30.
Next I give each of my vlans an Ip address. They will act as the default router for each vlan network.
One network will be 10.0.0.0/24 and the next is 172.16.0.0/24
On int f0/1 I turn on switchport and give it access to vlan 20
On int f0/2 I turn on switchport and give it access to vlan 30
Now I will configure two DHCP replays one for each network an configure each default-router to its matching vlan.
My final task will be to go into each wireless access point and configure and ssid
One will be named internal and given a passkey the other will be external and give it a passkey.
Now I go into each wireless device and connect to its respective access point.
Give it a few and you devices will get Ip address according to what access point you connect too.
