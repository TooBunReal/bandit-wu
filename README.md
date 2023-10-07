# WU_for_ae_dont_copy_meo_meo
- Sẽ có những chall mình lười nên chỉ chụp payload ( mong mn hiểu cho sự lười này :'> )
- Chall nào mình thấy hơi khó hiểu thì sẽ giải thích một xíu nha.
## Bandit 0
  ```ssh bandit0@bandit.labs.overthewire.org -p 2220```
  
  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/1321d19f-53ea-43d7-85fe-26a58f2fdf8b)

  pass: ```NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL```
## Bandit 0->1
  ```ssh bandit1@bandit.labs.overthewire.org -p 2220:NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/50c4da73-97ca-4b3f-97c0-f496a70da43e)

  pass: ```rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi```
  
## Bandit 1->2
  ```ssh bandit2@bandit.labs.overthewire.org -p 2220:rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi```
  
  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/683ee8ee-822b-47cc-b81a-843dab0e9e07)
  
  pass: ```aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG```
## Bandit 2->3
  ```ssh bandit3@bandit.labs.overthewire.org -p 2220:aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/2ef767a7-a588-4871-93ac-a317f49a05ec)

  pass: ```2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe```

## Bandit 3->4
  ```ssh bandit4@bandit.labs.overthewire.org -p 2220:2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/1fabb68f-1715-4bc5-bc5c-9ac1587054f3)
  
  pass: ```lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR```
  
## Bandit 4->5  
  ```ssh bandit5@bandit.labs.overthewire.org -p 2220:lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/e3f64d09-a82f-4cff-92bf-0a0f176ca2cf)

  pass: ```P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU```
  
## Bandit 5->6
  ```ssh bandit6@bandit.labs.overthewire.org -p 2220:P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/2f1872f4-b61b-4119-8acf-0838e8c68e30)

  pass: ```z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S```

## Bandit 6->7
  ```ssh bandit7@bandit.labs.overthewire.org -p 2220:z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/cf43d87f-1bc4-4d88-8a77-1dacfbaff451)

  pass: ```TESKZC0XvTetK0S9xNwm25STk5iWrBvP```

## Bandit 7->8
  ```ssh bandit8@bandit.labs.overthewire.org -p 2220:TESKZC0XvTetK0S9xNwm25STk5iWrBvP```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/19e6be13-27d4-4d56-b4e8-dc5111ad9cf3)

  pass: ```EN632PlfYiZbn3PhVK3XOGSlNInNE00t```

## Bandit 8->9
  ```ssh bandit9@bandit.labs.overthewire.org -p 2220:EN632PlfYiZbn3PhVK3XOGSlNInNE00t```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/f82bd358-0ec4-48df-8368-28de0490670e)

  pass: ```G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s```
  
## Bandit 9->10
  ```ssh bandit10@bandit.labs.overthewire.org -p 2220:G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/974de3c7-79bf-43ed-aaae-425a1cdec679)

  pass: ```6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM```

## Bandit 10->11
  ```ssh bandit11@bandit.labs.overthewire.org -p 2220:6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/a37adde1-3b34-412a-a531-05971bf1215d)

  pass: ```JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv```
  
## Bandit 11->12
  ```ssh bandit12@bandit.labs.overthewire.org -p 2220:JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv```

  - Có lẻ đây là chall mình không thích nhất của Bandit, nó khá mất thời gian.
  - Chall này cho ta một file hex, nhiệm vụ ở đây là phải giải nén theo định dạng file để có dc pass.
  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/78e04172-877f-4e4c-a1f1-6b14186f6c1f)

  pass: ```wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw```
  
## Bandit 12->13
  ```ssh bandit13@bandit.labs.overthewire.org -p 2220:wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw```
  - Truy cập vào thì ta nhận dc một key RSA.
  - Mình dùng lệnh ```scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private``` để dowload key về.
  - Tiến hành cấp quyền và kết nối với chall14 thông qua key.
  
  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/bbd024f4-5dbe-468d-9a85-c281723f1310)
 
## Bandit 13->14
  ```ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220```
  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/ff4ba056-4418-4b48-8ca1-caff39afb87b)

  pass: ```jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt```
## Bandit 14->15
  ```ssh bandit15@bandit.labs.overthewire.org -p 2220:jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/5fdf602f-c0ff-4980-baf2-c37c3872c250)

  pass:```JQttfApK4SeyHwDlI9SXGR50qclOAil1```
  
## Bandit 15->16
  ```ssh bandit16@bandit.labs.overthewire.org -p 2220:JQttfApK4SeyHwDlI9SXGR50qclOAil1```

  - Bài này chúng ra sẽ làm quen với khái niệm Bash script.
  - Bạn có thể làm tay nếu muốn, nhưng làm bằng script nhàn hơn :>
  - Ý tưởng của bài này là check port từ 31000 tới 32000 xem có cổng nào đang mở hay không từ đó có thể kết nối vào đó để lấy pass.
  ```sh
for i in {31000..32000} ; do
SERVER="localhost"
PORT=$i
(echo  > /dev/tcp/$SERVER/$PORT) >& /dev/null &&
echo "Port $PORT open"
done
```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/a8b8a11b-4aff-4732-bbc1-e7f5812e3080)

  - Với các cổng đã mở, ta sẽ kết nối ssl với cổng đó.

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/f987348d-87fd-45ed-89c4-c347ede14fe4)


  pass: 
  ```
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
  ```
  
## Bandit 16->17
  - Ở bài này chúng ta sẽ không connect như những lần trước, thay vào đó ta sẽ phải ssh vào bằng Key đã lấy được ở chall phía trên.
  - Nhưng trước hết, bạn cần phải cấp quyền cho key
  ```
chmod 400 key
ssh -i key bandit17@bandit.labs.overthewire.org -p 2220
  ```
  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/de3edaef-1f33-4dce-8b66-74b693c57566)

  pass: ```hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg```
## Bandit 17->18
  ```ssh bandit18@bandit.labs.overthewire.org -p 2220:hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/68161f5c-3512-4f45-b4b4-e8130da3188b)
  
  - Oh no, có lẽ chúng ta không được chào đón ở đây rồi.
  - Tuy nhiên, dựa theo hint của đề bài, ta có thể chèn cmd vào ngay sau ssh để nó tự động exec.

  ```ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat *"```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/f79b55df-a82a-4dbf-8fb0-e60c80dba55c)

  pass: ```awhqfNnAbc1naukrpqDYcF95h7HoMTrC```
## Bandit 18->19
  ```ssh bandit19@bandit.labs.overthewire.org -p 2220:awhqfNnAbc1naukrpqDYcF95h7HoMTrC```

  ![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/adb71d66-8873-4362-9847-55883ef243a2)

  pass: ```VxCazJaVykI6W36BkBU0mJTCM8rR95XT```

## Bandit 19->20
  ```ssh bandit20@bandit.labs.overthewire.org -p 2220:VxCazJaVykI6W36BkBU0mJTCM8rR95XT```
  
## Bandit 20->21
## Bandit 21->22
## Bandit 22->23
## Bandit 23->24
## Bandit 24->25
## Bandit 25->26
## Bandit 26->27
## Bandit 27->28
## Bandit 28->29
## Bandit 29->30
## Bandit 30->31
## Bandit 31->32
## Bandit 32->33
## Bandit 33->34
