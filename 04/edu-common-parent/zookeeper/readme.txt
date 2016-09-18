173  wget http://apache.fayea.com/zookeeper/zookeeper-3.4.6/zookeeper-3.4.6.tar.gz
  174  ls
  175  clear
  176  ls
  177  tar -xzvf zookeeper-3.4.6.tar.gz 
  178  ll
  179  clear
  180  ls
  181  cd zookeeper-3.4.6
  182  ls
  183  mkdir data
  184  mkdir logs
  185  ll
  186  cd conf
  187  ls
  188  clear
  189  ls
  190  cp zoo_sample.cfg zoo.cfg
  191  vi zoo.cfg 
  192  cd ..
  193  cd dta
  194  cd data
  195  ls
  196  vi myid
  197  clear
  198  cat /etc/profile
  199  vi /etc/profile
  200  clear
  201  ls
  202  source /etc/profile
  203  vi /etc/sysconfig/iptables
  204  chkconfig iptables on
  205  service iptables restart
  206  vi /etc/sysconfig/iptables
  207  service iptables restart
  208  zkServer.sh start
  209  jps
  210  zkServer.sh status
  211  cd ..
  212  ls
  213  cd conf
  214  ls
  215  cat zoo.cfg 
  216  ps -eaf | grep java
  217  vi /etc/rc.local 
  218  cd ~/tools
  219  ls
  220  clear
  221  ls
  222  tar -xzvf jdk-7u80-linux-x64.tar.gz 
  223  cd jdk1.7.0_80/
  224  pwd
  225  vi /etc/profile
  226  source /etc/profile
  227  java -version
  228  cd ..
  229  zkServer.sh restart
  230  jps
  231  cd zookeeper-3.4.6
  232  ls
  233  cd conf
  234  ls
  235  cat zoo.cfg 
  236  vi zoo.cfg 
  237  zkServer.sh restart
  238  cat /etc/profile
  239  cat zoo.cfg 
  240  vi zoo.cfg 
  241  zkServer.sh restart
  242  jps
  243  ps -eaf | grep java
  244  zkServer.sh status
  245  cd ..
  246  ls
  247  cd logs
  248  ls
  249  clear
  250  ls
  251  cd ..
  252  ls
  253  tail -f zookeeper.out 
  254  zkServer.sh restart
  255  tail -f zookeeper.out 
  256  history