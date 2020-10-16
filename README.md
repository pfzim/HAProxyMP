# [HAProxy Management Pack for SCOM](https://github.com/pfzim/HAProxyMP)

Discovery search for `/etc/haproxy/haproxy.cfg` file and get frontends from it.  
Monitor check for service is running `systemctl show haproxy.service -p ActiveState`.  
Performance Rule collect data `show stat` and `show table $1` for every frontend.  
If `/opt/haproxy/scom_perf_collect.sh` file exist, then it run for collect performance data `/opt/haproxy/scom_perf_collect.sh $1`.  
Output comma separated like this:  
```
CounterObject,CounterInstance,CounterName1,CounterValue1
CounterObject,CounterInstance,CounterName2,CounterValue2
CounterObject,CounterInstance,CounterName3,CounterValue3
CounterObject,CounterInstance,CounterName4,CounterValue4
```
