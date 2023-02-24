# ESDE Workshop 2022 for the Metasploit Framework
by Niklas Thürnau and Julia Sartori-Schwendemann

The Metasploit Framework (MSF) is a computer security project by Rapid7 to facilitate penetration testing. It is written in Ruby and available as open source software. It allows ethical hackers to scan for vulnerabilities and to fix these vulnerabilities befor they can be exploited.

### Disclaimer!
#### Only use the skills you learn in this workshop on your own systems or on systems which are provided for this purpose

### Practical
For the practical part please use exercise.md (and if you want to spoil yourself the solutions.md) in github. 

## Architecture
### Filesystem
The MSF is organized as a file system with several directories. Each directory serves its own purpose and contains specific information / files.
The subdirectories are:
* Data
* Documentation
* Lib
* Modules
* Plugins

### Libraries
With the use of libraries, the user can run exploits without writing code for basic and recurring tasks like http requests.
The main libraries are:
* REX: basic library for most tasks
* MSF Core: base API for MSF
* MSF Base: easier to use API

### Modules
Modules are used execute tasks.
There are five main types of modules:
* Exploits: Executing of command sequences
* Payload: Code that runs remotely
* Encoder: Make sure that payloads can be execute in the exploited system
* NPOs: Generate random byte sequences to conceal payloads
* Auxiliary: Tools like scanners, sniffers, fuzzer, etc.

### Mixins and Plugins
Plugins work directly with the API and extend the framework functionality. They only work in the msfconsole.
Mixins are a feature of Ruby. They allow the user to include one class into another and override methods. That way the user can manipulate a module and make protocol- or behaviour-specific changes.

## Fundamentals

### Interfaces
There are several interfaces for Metasploit. Each with their specific strength and weaknesses. 
#### MSFcli
Even though the MSFcli is no longer supported, we still think it is a useful tool. Especially for one-off exploits or when developing and testing new exploits.
#### MSFconsole
The MSFconsole is probably the most widely used Metasploit interface. As the name suggests it is a console-based interface that allows the user to execute commands. It is the only supported way to access most of the features within Metasploit. 
When starting out or if you need assistance down the line, you can use the help command to get a list of all your options.

### Exploits
There are two kinds of exploits in the Metasploit Framework, active and passive exploits.

While active exploits will target a specific host, run the exploit, and then exit, passive exploits wait until a host establishes a connection and then run exploits on them.

## Information Gathering
One of the most important tasks for successful penetration testing is the gathering of information. The more you know about a potential target, the easier it is to exploit that target.
Metasploit gathers information by using the following tactics:
* Port Scanning
* Hunting for SQL
* Service Identification
* Password Sniffing
* SNMP Sweeping

## Vulnerability Scanning
Another useful task for penetration testing is scanning for vulnerabilities. There are many known vulnerabilities that give an experienced penetration tester an idea which exploits might be successful. Metasploit has several features that are used to scan for vulnerabilities.
Some important ones are:
* VCN Authentication 
* SMB Login Check
* WMAP Web Scanner
* Working with Nessus
* Working with Nexpose


## Comparison with other frameworks

### Canvas
Main Features are 
* Payload Options
* Exploit Delivery
* Exploit Creation Time
* Custom Exploits

### Core Impact
Main features are
* Rapid Penetration Testing
* Core Certified Exploits
* Centralized Toolset

While there are other tools for penetration testing, the community driven aspect of and that it is available as open-source software are two key advantages of Metasploit. They facilitate the sharing of knowledge within the community and make easy for beginners to find a starting point.

## Quiz

Here you can find the quiz to test your knowledge of Metasploit:
QUIZIZZ: https://quizizz.com/join/quiz/63737acf0f9a4a001dfcd9be/start?studentShare=true

# Sources for the Workshop

* Metasploit Unleashed https://www.offensive-security.com/metasploit-unleashed/

* Where can you download the target vm for yourself?
-> Rapid7 https://information.rapid7.com/download-metasploitable-2017.html

* Metasploit https://www.metasploit.com

* turingpoint. https://turingpoint.de/blog/was-ist-metasploit/

* Core Impact https://www.coresecurity.com/products/core-impact

* Canvas https://immunityinc.com/products/canvas/

* packthub https://hub.packtpub.com/pentest-tool-in-focus-metasploit/ 


* Incase dockerfile is not working properly: docker pull metasploitframework/metasploit-framework
