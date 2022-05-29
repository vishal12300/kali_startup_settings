# kali_startup_settings

### sources.list

```
sudo tee -a /etc/apt/sources.list<<EOF
deb http://http.kali.org/kali kali-rolling main non-free contrib
deb-src http://http.kali.org/kali kali-rolling main non-free contrib
EOF
```

---

### pip3 install 

```
wget https://bootstrap.pypa.io/get-pip.py
python3 get-pip.py
```

---

### Solve apt-get or apt gpg key problem:


```
gpg --keyserver keyserver.ubuntu.com --recv-key 7D8D0BF6
gpg --fingerprint 7D8D0BF6
gpg -a --export 7D8D0BF6 | apt-key add -
apt update

```
---
### Go lang installation 

* Download the Go lang package [https://go.dev/dl/](https://go.dev/dl/)
* After Download run

```
cd /root/Downloads
tar -C /usr/local/ -xzf go1.13.6.linux-amd64.tar.gz
```
* Edit the ` .bashrd ` file
```
vim ~/.bashrc
```

Add the following paths

```
export GOPATH=/root/go-workspace
export GOROOT=/usr/local/go
PATH=$PATH:$GOROOT/bin/:$GOPATH/bin
```


``` 
source ~/.bashrc
go version
```

---

## install Go in Google Compute Engine instance

```
sudo curl -O https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz
```

```
sudo tar -xvf go1.16.2.linux-amd64.tar.gz
sudo rm -rf /usr/local/go
sudo mv go /usr/local
sudo apt-get update
```

```
export PATH=$PATH:/usr/local/go/bin
```


------

``` 
LinPeas: https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/linPEAS
LinEnum: https://github.com/rebootuser/LinEnum
LES (Linux Exploit Suggester): https://github.com/mzet-/linux-exploit-suggester
Linux Smart Enumeration: https://github.com/diego-treitos/linux-smart-enumeration
Linux Priv Checker: https://github.com/linted/linuxprivchecker
```

