# adblock
trial automatic update rule adblock openclash

Untuk menggunakan, edit `config.yaml` pada `/etc/openclash/config/config.yaml` seperti ini:
```
rule-providers:
  OISD_big:
    type: http
    behavior: classical
    path: "./rule_provider/OISD_big.yaml"
    url: https://raw.githubusercontent.com/anggaraw/my_adblock_list/main/OISD_big.yaml
    interval: 86400 # Update rules every 24 hours
  Malicious URL Blocklist (URLHaus):
    type: http
    behavior: classical
    path: "./rule_provider/Malicious URL Blocklist (URLHaus).yaml"
    url: https://raw.githubusercontent.com/anggaraw/my_adblock_list/main/Malicious%20URL%20Blocklist%20(URLHaus).yaml
    interval: 86400 # Update rules every 24 hours      
rules:
- RULE-SET,OISD_big,REJECT
- RULE-SET,Phishing URL Blocklist (PhishTank and OpenPhish),REJECT
- RULE-SET,Malicious URL Blocklist (URLHaus),REJECT
```
