![image](https://github.com/TooBunReal/bandit-wu/assets/89735990/8afac0d6-9c49-4ff2-8293-539660f998f9)# WU_for_ae
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
## Bandit 13->14
## Bandit 14->15
## Bandit 15->16
## Bandit 16->17
## Bandit 17->18
## Bandit 18->19
## Bandit 19->20
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
