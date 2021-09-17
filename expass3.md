First problem was installing as their was no guide for Arch linux, proceeded with aur. After installing I could not enter the shell with "mongo" or "mongod". 
Ended up givning up and installed docker and pulled mongodb from there. Did not vailidate, cause docker does that for you. 
 
![Alt text](https://github.com/Sigvah/DAT250_experiments/blob/main/Screenshot%20from%202021-09-12%2015-36-17.png)

Installing mongo compass created new problems. First it did not want to install because of something broke in aur installer. Tried lots of things including switching computer, but after a restart and switching aur helper it magically installed. After instaltion I needed to connect with docker, fix was instead of localhost:127.0.0.1:27017/ I used my ipaddress + 127.0.0.1:27017/. 
