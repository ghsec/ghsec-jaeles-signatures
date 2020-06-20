# ghsec-jaeles-signatures

Author: @j3ssie

jaeles official repository and documentation: https://jaeles-project.github.io/

jaeles signatures by j3ssie: https://github.com/jaeles-project/jaeles-signatures


### Signatures: 
#### Reflect XSS
* js-xss.yaml ```detects reflect XSS in js code and reflection in tags```
* simple-xss.yaml ```detects reflect XSS with <xsshere>```

### Errors and Vulnerabilities
*  	ErrorsAndVulns.yaml ```detects errors and vulnerabilities```
1. sqli
2. lfi
3. ssti
4. other

### SSRF
* ssrf.yaml 
need run with -p flag

Example: ```jaeles scan -u http://example.com/path?param=something -s ssrf.yaml -p "dest=yourServer" ```

### LFI

* lfi-Unix.yaml
* lfi-windows.yaml

### OS Command Injection
* OS_command_injection.yaml

### SSTI
* Template-Injection.yaml


Twitter: @[GochaOqradze](https://twitter.com/GochaOqradze)

### Donate me: 
https://www.paypal.me/Okradze
