Add this lines to the file ~/.bashrc
```
date=`date +%H%M_%d%m%Y`
alias nameServer="ssh user@ip_address | tee -a /tmp/ssh_$date.log"
```
Restart the ssh session or run this to load the changes ```. ~/.bashrc```

To access the SSH machine, we only have to type the name we have given to our alias.
```$ nameServer```

Our log will record everything that is done in the ssh session in a file in the path we have defined, ```/tmp/ssh_$date.log```

