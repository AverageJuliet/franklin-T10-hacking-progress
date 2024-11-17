# franklin T10-hacking progress
my progress with gaining root on the Franklin T10 hotspot modem

My first course of action was gaining a console, this was pretty easy as the device has a pair of TX/RX pads on the mainboard.
 
Upon giving the device power it initially didn't do all that much aside from some bootloader information but pressing the powerbutton began the boot process leading me to discover the entire boot process/logs was fully exposed. (they didn't use the quiet flag thankfully) and that it wasn't read only.

But I was hit with a roadblock: I didn't know the root password. And as such the project was later put on hold until Rich Hathaway over on the wirelessjoint forms provided me with an entire firmware dump, and with that begins attempting to find it using the `/etc/shadow` file


