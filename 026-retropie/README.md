## #26 - Play Retro Games Remotely Using Retropie and Tailscale

[![Play Retro Games Remotely Using Retropie and Tailscale](https://img.youtube.com/vi/kiTPVO1WfRI/maxresdefault.jpg)](https://www.youtube.com/embed/kiTPVO1WfRI)

### Installing RetroPie as a Docker container : https://github.com/nwildner/retropie-docker

### Installing [RaspberryPi Imager](https://www.raspberrypi.com/software/)
- macOS, Linux
`brew install --cask raspberry-pi-imager`
- Windows
`scoop install extras/raspberry-pi-imager`

### Login using SSH
`ssh pi@retropie.local`

### Updating Raspberry Pi OS
```bash
sudo apt update -y; sudo apt-get update -y; sudo apt-get upgrade -y;
```

### Installing `git`
```bash
sudo apt install git lsb-release -y
```

### Running the RetroPie Setup
```bash
cd RetroPie-Setup/;
chmod +x retropie_setup.sh;
sudo ./retropie_setup.sh;
```

### Copying the Games to RetroPie
```bash
scp -r <roms-path> pi@retropie.local:~/RetroPie/roms
```

### Mounting the NAS Share
* Edit the `fstab` file with
```bash
sudo nano /etc/fstab;
```
* Add this line to the bottom. Replace with `<nas-ip>` with your NAS's IP and `<roms-path>` with the location for the ROMs.
* Also replace `<username>` & `<password>` with you NAS's username and password
```bash
//<nas-ip>/<roms-path> /home/pi/RetroPie/roms cifs username=<username>,password=<password>,nounix,noserverino,defaults,users,auto 0 0
```
You can run `sudo mount -a` to check if you NAS mounts correctly before rebooting.
