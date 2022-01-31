# EOSDG for docker-compose
Used for easy setup of eosdg.  
If you are using this behind a firewall, ports 80 and 3420 have to be opened.
## Usage
### Clone
```bash
git clone --recurse-submodules -j2 git@github.com:eosdg/docker.git
```
### Start Server:
```bash
docker-compose up -d
```

### Stop Server:
```bash
docker-compose down
```
