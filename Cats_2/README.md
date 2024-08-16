# Cats 2

My refresher and my first CTF challenge in THM

## Table Of Contents

1. [Flag 1](#flag-1)
2. [Flag 2](#flag-2)
---
# Steps

First i scanned the IP using nmap
>nmap 10.10.54.153 -v

Giving me these outputs

![alt text](image.png)

Knowing port 80 is open i immediately open http://{ip}

Quick preview of the site 

![alt text](image-1.png)

Scrimming through the album i saw this description

![alt text](image-2.png)

I extracted the metadata giving me this note

![alt text](image-3.png)

So i tried opening port 8080 with the note as url giving me this 

![alt text](image-5.png)

Opening port 3000 i got redirected to Gitea

![alt text](image-7.png)

---
# Flag 1
Quick scanning i found the First Flag

![alt text](image-9.png)

I then read the playbook.yaml but nothing interesting for now

now i tried the other open port from the note i got on port 8080 and tried opening the port 1337 

![alt text](image-10.png)

Not familiar with ansible, i did a quick google search and i found out that i can manipulate the playbook.yaml from earlier to execute some linux commands manipulating the ansible execution

first i tried to ls to show the directory contents 

![alt text](image-12.png)

Viola! i got the 2nd Flag

---
# Flag 2

Then i tried to cat flag2.txt giving me this 

![alt text](image-13.png)

---

# Flag 3

Not solve yet as i reached dead end
