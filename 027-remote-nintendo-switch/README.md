## #27 - This Nintendo Switch 2 Trick Will Blow 🤯 Your Mind

[![this nintendo switch 2 trick will blow 🤯 your mind](https://img.youtube.com/vi/isLsAP5_Jpo/maxresdefault.jpg)](https://www.youtube.com/embed/isLsAP5_Jpo)

### Installing [RaspberryPi Imager](https://www.raspberrypi.com/software/)
- macOS, Linux
`brew install --cask raspberry-pi-imager`
- Windows
`scoop install extras/raspberry-pi-imager`

### Login using SSH
`ssh vdo@raspbertypi.local`

### Download & install `nxbt`
- Download the binary
`wget "https://github.com/typenoob/nxbt/releases/download/Build_2023.10.29/nxbt-gnu-aarch64"`
- Rename the downloaded binary
`sudo mv nxbt-gnu-aarch64 nxbt`
- Make the binary executable
`chmod +x nxbt`

### Install `tmux`
`sudo apt install -y tmux`

### Running the `vdo.ninja` stream for display
`python3 ~/raspberry_ninja/publish.py --streamid=switchcapture --password=switchcontrol --hdmi --x264 --width 1280 --height 720 --multiviewer`

### Run the `nxbt` webapp and serve over https
`sudo ~/nxbt webapp -r`
