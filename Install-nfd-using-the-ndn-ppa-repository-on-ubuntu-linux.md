#### Install NFD Using the NDN PPA Repository on Ubuntu Linux

NFD binaries and related tools for Ubuntu 14.04 and 16.04 can be installed using PPA packages from named-data repository. First, you will need to add <b>named-data/ppa</b> repository to binary package sources and update list of available packages.
<p>
<p>


  <li><b>Preliminary steps if you haven’t used PPA packages before</b><p></li>
    To simplify adding new PPA repositories, Ubuntu provides add-apt-repository tool, which is not installed by default on some systems.

  <pre>
  sudo apt-get install software-properties-common
  </pre>

<li><b>Adding NDN PPA</b><p></li>
  After installing <b>add-apt-repository</b>, run the following command to add [[NDN PPA repository.] ](https://launchpad.net/~named-data/+archive/ppa)

  <pre>
  sudo add-apt-repository ppa:named-data/ppa
  sudo apt-get update
  </pre>
