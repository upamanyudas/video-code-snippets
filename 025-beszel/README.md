## #25 - Open Source and lightweight server monitoring for Windows, Mac Linux

[youtube-link-slug]: qj65pNgSPtE

[![Open Source and lightweight server monitoring for Windows, Mac Linux](https://img.youtube.com/vi/[youtube-link-slug]/sddefault.jpg)](https://www.youtube.com/embed/[youtube-link-slug])

- `docker` and `docker-compose` install commands

```bash
sudo apt update -y; sudo apt-get update -y; sudo apt-get upgrade -y; curl -sSL https://get.docker.com | sh; sudo usermod -aG docker ${USER}; groups ${USER}; sudo apt-get install -y libffi-dev libssl-dev; sudo apt install -y python3-dev; sudo apt-get install -y python3 python3-pip; sudo apt-get install docker-compose; sudo systemctl enable docker; sudo docker run hello-world;
```

- Run the following command to download and run the `beszel-agent` on a Mac
- Replace `<url>` with the download url for your system
- Replace `<key>` with the generated **ssh-key** from the Beszel Dashboard

```bash
curl -sL <url> -o beszel-agent.tar && tar -xf beszel-agent.tar && rm beszel-agent.tar && chmod +x ./beszel-agent && PORT=45876 KEY="<key>" ./beszel-agent
```

---

If you want to run `beszel-agent` on Windows as Binary, here are some resources:
- https://github.com/henrygd/beszel/discussions/18

