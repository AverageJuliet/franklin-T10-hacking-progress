# franklin T10 hacking progress
my progress with gaining root on the Franklin T10 hotspot modem

My first course of action was gaining a console, this was pretty easy as the device has a pair of TX/RX pads on the mainboard.
![20241117_153426](https://github.com/user-attachments/assets/c3fa280e-a0f4-4236-a063-065c39732ea7)

 
Upon giving the device power it initially didn't do all that much aside from some bootloader information but pressing the powerbutton began the boot process leading me to discover the entire boot process/logs was fully exposed. (they didn't use the quiet flag thankfully) and that it's console wasn't read only.

But I was hit with a roadblock: I didn't know the root password. And as such the project was later put on hold until [Rich Hathaway over on the wirelessjoint](https://wirelessjoint.com/viewtopic.php?t=4168) forms provided me with [an entire firmware dump](https://github.com/AverageJuliet/franklin-T10-hacking-progress/releases/tag/firmware), and with that begins attempting to find it using the `/etc/passwd` file

Tried for a few hours to crack the password using hashcat, dead end.


I tried to change the password hash in the system dump and tried flashing it. this sadly resulted in a perma brick. (it refused to accept both a T10 and a T9 sys image)

RIP...

random T10 10/31/24-11/17/24 your death wasn't deserved. 
