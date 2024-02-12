# Temperature Controlled Fan With Poweroff Button for RaspberryPI


NOTE: Never connect the fan directly to the I/O Pins

1. Build the circuit
2. Place `main.py` in `/home/pi/services/pi-temp-fan/` or any other directory. 
   Final path should be `/home/pi/services/pi-temp-fan/main.py`
3. Place `pi-temp-fan.service` in `/lib/systemd/system/`.
   Final Path should be `/lib/systemd/system/pi-temp-fan.service`
4. Change the permissions on the service
   `sudo chmod 644 /lib/systemd/system/tcfp.service`
5. Add executable to the py script
   `chmod +x /home/pi/services/pi-temp-fan/main.py`
6. Reload systemd configuration
   `sudo systemctl daemon-reload`
7. Enable te new service
   `sudo systemctl enable pi-temp-fan.service`
8. Run it
   `sudo systemctl start pi-temp-fan.service`



