## Goal

1. Check the root bridge (Using CLI and without using CLI)
2. Manually configure the appropriate RSTP link type on each interface.

 ![[Pasted image 20260104113953.png]]

### **Steps** 

1. Identify the root bridge 

```
SW1 # show spanning-tree
SW1 # show spanning-tree detail
SW1 # show spanning-tree summary
```

   2. Choosing the lowest Bridge ID as root bridge , if Bridge IDs are same , then choosing the lowest MAC
   3. Configuring the ports of switches to the different type of RSTP
   ```
   SW1(configure-if)spanning-tree pord portfast -- change to the edge style
   SW1(configure-if)spanning-tree pord link-type  -- point to point or shared
   ```
   
## Summary

1. What is RSTP ?

2. What are differences between RSTP and STP ?

3. How to choose Root bridge ? 
    Choosing the lowest Bridge ID as root bridge , if Bridge IDs are same , then choosing the lowest MAC.

4. What different types between the ports of switches in the STP ?
    Root port / designated port / non-designated port (backup port & alternative port)

5. What different types between the ports of switches in the STP Link typed ?
    edge(connect to hosts) / point to point (connect to switches)/ shared(connect to hub)




Tag: #STP  #CCNALAB #RSTP

