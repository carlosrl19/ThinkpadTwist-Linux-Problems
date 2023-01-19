# Thinkpad Twist Touchpad Fix 
A way to fix touchpad problem to Lenovo Thinkpad Twist laptops.


1. Run the following command in terminal:

```bash
  sudo nano /etc/default/grub
```


2. The GRUB configuration file should open. Locate the following line:

+ GRUB_CMDLINE_LINUX=" "

3. Add this into the parameters:

+ i8042.nomux=1 locale=fr_FR i8042.reset

4. The final line should look like this:

+ GRUB_CMDLINE_LINUX="i8042.nomux=1 locale=fr_FR i8042.reset"

5. Save the file and exit gedit.

6. Run the following command in terminal:
sudo update-grub

7. Let the grub.conf file get recreated, and then restart.

