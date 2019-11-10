# JGU WEKA Rest Service

Here is a summary of the commands to run to start profiling the JGU Weka application.

## Prerequisites
- JGU weka is deployed. (See Q2_README.md for more information)
- Installing JProfiler

## Retrieving the IP address of the JGU Weka container
```
$ docker inspect weka | grep -P "IPAddress" | grep -P "\d+"
```

## Demonstration of JGU Weka container profiling
```
$ docker exec -it weka bash
$ chmod +x /home/tomcat/start_profiling.exp
$ /home/tomcat/start_profiling.exp
```

### JProfiler
- Open the application jprofiler
- Press Ctrl + n to start a new session
- Press "Attach to remote VM"
- Enter the IP address to recover above
- Enter port 8849
- Press the button "ok" and press the next buttons "next" without changing any parameter.
