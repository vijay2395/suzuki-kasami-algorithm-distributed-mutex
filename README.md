## Suzuki Kasami's Mutual Exclusion Algorithm for the Distributed system
This project is an implementation of the token based Suzuki-Kasami's broadcasting algorithm in a distributed system. Here we consider five sites for demonstration.

#### Configuration files:
The configuration file can be provided as argument, which should be given in absolute file path. This file should contain the information associated with site number, its ip address and it's port number. If no file is specified it would be defaulted to `site_nodes.conf` present in repo.

- The format of configuration file is : 
`<site_id> <Ip_of_site> <port>`

This file should be changed as requirement. (e.g. how many sites should be in the system). Here, client_id is started from 1 and can be assigned incrementally to each client.

#### Details of the system:
The Suzuki–Kasami algorithm is a token-based algorithm for achieving mutual exclusion in distributed systems. In the system there are multiple site which can execute some specific task with entering into the critical section, mutual exclusively. To achieve this mutual exclusion, we implement token based Suzuki-Kasami Broadcasting Algorithm here.
If a site possess a unique token, then only it can be allowed to execute in the critical section.

**For implementation:**

1. MacOS operating system (since the directory structure will be different for MacOS, it uses \ (backslash) as opposed to (/) slash in windows. If we can change this in SuzukuKasamiMutualExclusion.java line 26 , then it may work for windows

2. Requires Java 1.8, Java Socket Programming, and Threading. the program will achieve mutual exclusion over the network or on a local computer using different ports. Note that, the ip's and ports should be ensured to be accessible to each sites.

3. More steps are detailed below. 


#### Steps:
 - The program can be run locally on terminals/command prompt.
 - Each terminal runs a single site.
 - To start a site: 
    - We need to run the command `java -jar suzuki-kasami-algorithm-distributed-mutex.jar <optional-input-file>`
 - Once the program starts, it will ask the site number : `Enter site number (1-5):`
 - After entering the corresponding site number, it would display the message `Press <ENTER> to enter Critical Section: `
 - It is recommended to ensure that all sites are initialized and running(one terminal for each site for running the program in a single local computer). 
 - When all the sites are running simultaneously, press enter on any site for requesting entering into the critical section. 
 - Initially, Site 1 possesses the token.
 - In this implementation, the program will run until terminating it deliberately using `Ctrl+C` or `Cmd+C`.
 - Embedded video for running steps :
  
   https://user-images.githubusercontent.com/20264360/198835584-4c569917-f042-4a57-bc91-9c24e5b60f86.mp4

 - Git repo for the same : https://github.com/vijay2395/suzuki-kasami-algorithm-distributed-mutex





