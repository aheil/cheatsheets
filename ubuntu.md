# Update Error 

You get 

```
E: The repository 'http://archive.ubuntu.com/ubuntu disco Release' no longer has a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
```

Run 

```
sudo sed -i -re 's/([a-z]{2}\.)?archive.ubuntu.com|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list
```
then 

```
sudo apt-get update && sudo apt-get dist-upgrade
```

afterwards do 

```
sudo apt-get update
sudo apt-get install ubuntu-release-upgrader-core
sudo do-release-upgrade

```


