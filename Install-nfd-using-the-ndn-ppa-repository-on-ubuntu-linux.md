#### Install NFD Using the NDN PPA Repository on Ubuntu Linux

[[Source : Install NFD ](http://named-data.net/doc/NFD/current/INSTALL.html#install-nfd-using-the-ndn-ppa-repository-on-ubuntu-linux) 
[[Source : Install NDN-CXX] ](http://named-data.net/doc/ndn-cxx/current/INSTALL.html) 

NFD binaries and related tools for Ubuntu 14.04 and 16.04 can be installed using PPA packages from named-data repository. First, you will need to add <b>named-data/ppa</b> repository to binary package sources and update list of available packages.




  <li><b>Preliminary steps if you haven’t used PPA packages before</b><p></li>
    To simplify adding new PPA repositories, Ubuntu provides add-apt-repository tool, which is not installed by default on some systems.

  <pre>
  sudo apt-get install software-properties-common
  </pre>
  <pre>
  bertopeng17@bertopeng17-ThinkPad-T520:~$ <b>sudo apt-get install software-properties-common</b>
  </pre>
  
![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2022-01-24.png)

  
  
  
<li><b>Adding NDN PPA</b><p></li>
  After installing <b>add-apt-repository</b>, run the following command to add [[NDN PPA repository.] ](https://launchpad.net/~named-data/+archive/ppa)

  <pre>
  sudo add-apt-repository ppa:named-data/ppa
  sudo apt-get update
  </pre>
  
  <pre>
  bertopeng17@bertopeng17-ThinkPad-T520:~$ <b>sudo add-apt-repository ppa:named-data/ppa</b>
  </pre>
  
  <pre>
  bertopeng17@bertopeng17-ThinkPad-T520:~$ <b>sudo apt-get update</b>

  </pre>


  ![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2022-05-10.png)
  ![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2022-06-12.png)

<li><b>Installing NFD and other NDN packages</b><p></li>

  <pre>
  bertopeng17@bertopeng17-ThinkPad-T520:~$ <b>sudo apt-get install nfd</b>
  </pre>
  
  ![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2022-11-29.png)
  
  
<li><b>Building from Source</b><p></li>

  <b>Downloading from Git</b>
  The first step is to obtain the source code for NFD and, its main dependency, the ndn-cxx library. If you are not planning to work with the bleeding edge code, make sure you checkout the correct release tag (e.g., *-0.2.0) for both repositories:
    
  <pre>
    Download ndn-cxx : git clone https://github.com/named-data/ndn-cxx
    Download NFD  : git clone --recursive https://github.com/named-data/NFD
  </pre>

  <pre>
  bertopeng17@bertopeng17-ThinkPad-T520:~$ <b>git clone https://github.com/named-data/ndn-cxx</b>
  bertopeng17@bertopeng17-ThinkPad-T520:~$ <b>git clone --recursive https://github.com/named-data/NFD</b>
  </pre>
  <p>

![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2022-30-21.png)
![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2022-42-42.png)


 <li><b>Prerequisites </b>Install the ndn-cxx library and its requirements</li>
    -  pkg-config
    -  libpcap
    -  doxygen, graphviz, python-sphinx

   <pre>
   sudo apt-get install pkg-config
   sudo apt-get install libpcap
   sudo apt-get install doxygen
   sudo apt-get install graphviz
   sudo apt-get install python-sphinx

   </pre>
   <pre>
   bertopeng17@bertopeng17-ThinkPad-T520:~$ <b>sudo apt-get install pkg-config</b>
   bertopeng17@bertopeng17-ThinkPad-T520:~$ <b>sudo apt-get install libpcap-dev</b>
   </pre>
 
   <pre>
   bertopeng17@bertopeng17-ThinkPad-T520:~$ <b>sudo apt-get install doxygen graphviz python-sphinx</b>
   </pre>
 


![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2023-13-50.png)

 
 
 
 <li><b>Build </b>The following basic commands should be used to build NFD on Ubuntu:</li>
 To build in a terminal, change directory to the <b>ndn-cxx</b> root. Enter:


 <pre>
  ./waf configure
  ./waf
  sudo ./waf install
 </pre>

If you have installed ndn-cxx library and/or other dependencies into a non-standard paths, you may need to modify <b>PKG_CONFIG_PATH</b> environment variable before running ./waf configure. For example,

<pre>
export PKG_CONFIG_PATH=/custom/lib/pkgconfig:$PKG_CONFIG_PATH
</pre>
<pre>
bertopeng17@bertopeng17-ThinkPad-T520:~/NFD$ <b>export PKG_CONFIG_PATH=/custom/lib/pkgconfig:$PKG_CONFIG_PATH</b>
</pre>

 <pre>
 bertopeng17@bertopeng17-ThinkPad-T520:~/ndn-cxx$ <b>./waf configure</b>
</pre>
![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2023-47-24.png)

<pre>
 bertopeng17@bertopeng17-ThinkPad-T520:~/ndn-cxx$ <b>./waf</b>
</pre>

![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2023-47-56.png)
![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2023-49-44.png)
![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2023-50-15.png)




<pre>
 bertopeng17@bertopeng17-ThinkPad-T520:~/ndn-cxx$ <b>sudo ./waf install</b>
</pre>

![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2023-55-52.png)
![alt tag](https://github.com/Telmat2015/NFD/blob/master/image/Screenshot%20from%202016-09-27%2023-56-17.png)


