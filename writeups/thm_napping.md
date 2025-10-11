---

title: "Napping"

---
<center>
<strong>1. 🔍 Enumeration Part + Directory Bruteforcing</strong><br> 
<strong>2. ☠️ Exploitation Part</strong><br>
<strong>3. 🔓 Privilege Escalation Part</strong>
</center>

---

<span style="color:red"><strong>1. 🔍 Enumeration Part + Directory Bruteforcing</strong></span><br>
We will start from the nmap scan:<br>
<center>
![NMAP](./images/nmap_napping.png)
</center>

gobuster dir -u http://10.10.136.217/ -w=/usr/share/wordlists/dirbuster/directory-list-lowercase-2.3-medium.txt -x php<br>
gobuster result screen<br>

gobuster dir -u http://10.10.136.217/admin/ -w=/usr/share/wordlists/dirbuster/directory-list-lowercase-2.3-medium.txt -x php<br>
gobuster admin screen<br>

Cheking the page:<br>

Simply open the ip adress in the browser, seeing the login form and register form.<br>
Will create an account and login there:<br>

After creating and sighning up we see the text that says "Please submit your link so that we can get started.
All links will be reviewed by our admin who also built this site!"<br>

Guessing that if we will do a mirroring of login.php page the admin will review it and enter his creds, lets try:<br>


