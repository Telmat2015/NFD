#### Starting NFD on Linux with upstart

Some Linux distributions, such as Ubuntu, use upstart as a standard mechanism to start system daemons, monitor their health, and restart when they die.

#### Initial setup
<li>Edit <b>nfd.conf </b>correcting paths for nfd binary, configuration and log files</li>
<li>Copy upstart config file for NFD</li>


<pre>
sudo cp nfd.conf /etc/init/
</pre>




