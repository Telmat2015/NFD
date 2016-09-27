#### Install NFD Using the NDN PPA Repository on Ubuntu Linux

NFD binaries and related tools for Ubuntu 14.04 and 16.04 can be installed using PPA packages from named-data repository. First, you will need to add <b>named-data/ppa</b> repository to binary package sources and update list of available packages.




  <li><b>Preliminary steps if you haven’t used PPA packages before</b><p></li>
    To simplify adding new PPA repositories, Ubuntu provides add-apt-repository tool, which is not installed by default on some systems.

  <pre>
  sudo apt-get install software-properties-common
  </pre>
  <pre>
  bertopeng17@bertopeng17-ThinkPad-T520:~$ <b>sudo apt-get install software-properties-common</b>
  </pre>
  
  ![alt tag](![alt tag](https://github.com/syaifulahdan/ndnlearn/blob/master/image/Screenshot%20from%202016-09-22%2011-51-27.png)
)

  
  
  
<li><b>Adding NDN PPA</b><p></li>
  After installing <b>add-apt-repository</b>, run the following command to add [[NDN PPA repository.] ](https://launchpad.net/~named-data/+archive/ppa)

  <pre>
  sudo add-apt-repository ppa:named-data/ppa
  sudo apt-get update
  </pre>
