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

### Metasploit Object Modle
### Mixins and Plugins
Plugins work directly with the API and extend the framework functionality. They only work in the msfconsole.
Mixins are a feature of Ruby. They allow the user to include one class into another and override methods. That way the user can manipulate a module and make protocol- or behaviour-specific changes.

## Fundamentals
### MSFcli
### MSFConsole
### Exploits
### Meterpreter

## Information Gathering
Metasploit gathers information by using the following tactics:
* Port Scanning
* Hunting for SQL
* Service Identification
* Password Sniffing
* SNMP Sweeping

## Vulnerability Scanning
* SMB Login Check
* VCN Authentication
* WMAP Web Scanner
* Working with Nexpose
* Working with Nessus


# Comparison with other frameworks

## Canvas
Main Features are 
* Payload Options
* Exploit Delivery
* Exploit Creation Time
* Custom Exploits

## Core Impact
Main features are
* Rapid Penetration Testing
* Core Certified Exploits
* Centralized Toolset



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


* Incase dockerfile is not working properly: docker pull metasploitframework/metasploit-framework
