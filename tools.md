```
go install -v github.com/tomnomnom/httprobe@latest
go install -v github.com/tomnomnom/assetfinder@latest
go install -v github.com/tomnomnom/waybackurls@latest
go install -v github.com/tomnomnom/meg@latest
go install -v github.com/tomnomnom/anew@latest
go install -v github.com/tomnomnom/qsreplace@latest
go install -v github.com/tomnomnom/unfurl@latest
go install github.com/ffuf/ffuf@latest
go install github.com/lc/gau/v2/cmd/gau@latest
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
go install -v github.com/projectdiscovery/nuclei/v2/cmd/nuclei@latest
```
---
### Finddomain
```
git clone https://github.com/findomain/findomain.git
cd findomain
cargo build --release
sudo cp target/release/findomain /usr/bin/
findomain
```
### Sublist3r
```
git clone https://github.com/aboul3la/Sublist3r.git
cd Sublist3r
pip3 install -r requirements.txt
python3 setup.py install
sublister
```


## Automate bug bounty.
SQLI - XSS - LFI
```
waymore -i urls | tee urls-his

cat urls-his | gf sqli |urless| anew sqli
cat urls-his | gf xss | urless|anew xss
cat urls-his | gf lfi | urless|anew lfi

ghauri -m sqli --confirm --batch --level=3  -b

knoxnl -i xss -X BOTH 

python3 lfimap.py -F lfi --use-long -a --no-stop
```
Use -x Exploit and send reverse shell if RCE is available 
