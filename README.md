
## know how process management works on Linux systems?

* **Foreground** processes -> these are initialized and controlled through a terminal session

* **Background processes** -> are processes not connected to a terminal; they don’t expect any user input

* **DAEMONS** ->  background processes that start at system startup and keep running forever as a service; they don’t die.

* **CREATION OF PROCESS** -> System() Function, Using fork() and exec() Function

* **IDENTIFY PROCESS** ->  a program is identified by its process ID (PID) as well as it’s parent processes ID (PPID).

* **Parent processes** -> create other processes during run-time , **Child processes** ->  are created by other processes during run-time.

* Init Process systemd -> **PIDOF** ->to find the PID of a process.

* Foreground, background &, jobs,

* **STATS OF PROCESS** -> **Running,stopped,waiting,zombie**

* COMMANDS 

**ps** -> Show active process

**top** ->  **dynamic real-time view of a running system**

**glances** -> system monitoring tool with advanced features

** SIGNALS** -> **KILL -L** 



## typical filesystem hierarchy

**/** -> Root Directory

**/bin**-> Essential command binaries

**/sbin**-> Essential system binaries
		
**/boot**->  	Boot loader files
		 
**/dev** -> devices /dev/sda, /dev/tty
		
**/etc** -> Configuration files
	
**/home**-> Users' home directories
		
**/lib** ->  Libraries essential for the binaries in /bin and /sbin. 
		
**/media*-> Mount points for removable media such as CD-ROMs
	
**/mnt** -> Temporarily mounted filesystems.
		
**/opt** -> Optional application software packages
		
**/proc**-> Virtual filesystem providing process and kernel information as files
		 
**/root**-> Home directory for the root user. 
		 
**/run** -> Run-time variable data: Information about the running system since last boot, e.g., currently logged-in users and running daemons
		
**/sys** -> Contains information about devices, drivers, and some kernel features
		
**/tmp** -> Temporary files.
		 
**/usr** -> contains the majority of (multi-)user utilities and applications.
		 
**/var** -> Variable files—files whose content is expected to continually change during normal operation of the system—such as logs, spool files, and temporary e-mail files. 


## SERVICES AND DAEMONS

Daemon is a background, non-interactive program. Its detach from the keyboard. 
Daemons -> crond,named,httpd,xinetd,sshd

A service is a program which responds to requests from other programs over some inter-process communication mechanism (usually over a network). 
A service is what a server provides.


## PIPE command lines

ls -la | grep "hola"

cat file | wc -l

cat x | less


## NETWORKING
## OSI MODEL ->   Open Systems Interconnection

**Physical Layer** -> Transmission and reception of raw bit streams over a physical medium, Guarantee the connection

**Data Link Layer** -> NOde-to-node-data-transfer. El switch is the device who uses this layer, revice the data from the router and sends it to their destinataries, error-detection
 
**Network Layer**-> Establish, maintain, and terminate network-connections. The objective of the network layer is to make the data arrive from the origin to the destination, 
even when both are not directly connected but use intermediate devices.
 
**Transport Layer**-> Layer responsible for transporting the data (found inside the package) from the source to the destination machine, independent of the type of physical network that is being used
 
**Session Layer**-> This layer is responsible for maintaining and controlling the link established between two computers that are transmitting data of any kind
 
**Presentation Layer**-> The objective is to take charge of the representation of the information, so that although different equipment can have different internal representations of characters, 
the data arrive in a recognizable way
 
**Application Layer**-> It offers to the applications the possibility of accessing the services of the other layers and defines the protocols that the applications use to exchange data


## machines on a network

**NMAP**

Access to the router



## Important protocols, IP,TCP,TLS,DNS,HTTP


IP -> Network Layer, Sending data packets both locally and through networks.

TCP Transmission Control Protocol -> Transport Layer, It provides host-to-host connectivity at the transport layer of the Internet model. Reliable and bidirectional data transport

TLS Transport Layer Security -> Security in the transport layer.  asymmetric cryptography to authenticate the counterpart with whom they are communicating and to exchange a symmetric key

DNS -> Aplication Layer. Domain name System. To identify the hosts with a name that everybody will know instead to know them by their identity, the ip.  53

HTTP Hypertext Transfer Protocol -> Aplication Layer. client-server.  Allow the exchange of information between web clinets and server http. 80 



## troubleshooting when things don’t behave as expected

First its important to check the **output error**. 

If this isnt enough, try to check an error_log. 

If the problem is still there i suggest you tu come back when the program or script was running correctly and change thing by thing what you want and check when it fails.

If this doesnt work, search for the possible solution to the problem.  Because someone may have had the same issue and it could help you really fast. 










