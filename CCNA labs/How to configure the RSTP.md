## Goal

1. Identify the root bridge using CLI and non-CLI methods
2. Manually configure the appropriate RSTP link types on each interface.

### **Topology**
<img width="1537" height="910" alt="Screenshot 2026-01-04 113938" src="https://github.com/user-attachments/assets/8b46de5c-bfb0-43e9-bd7d-41304f33b04a" />



### **Steps** 

1. Identify the root bridge (Using CLI)

```
SW1 # show spanning-tree
SW1 # show spanning-tree detail
SW1 # show spanning-tree summary
```


2. Identify the Root Bridge (Without Using CLI)

    Root Bridge Selection Logic :
    Choosing the lowest Bridge ID as root bridge , if Bridge IDs are same , then choosing the lowest MAC
   
 3. Configuring  RSTP port types
- a. configure Edge Port 
   ```
   SW1(configure-if)spanning-tree portfast
   # change port to the edge style
   ```
   b. Configure Point-to-point Link
   ```   
   SW1(configure-if)spanning-tree link-type  point-to-point
   # point-to-point or shared
   ```




Tag: #STP  #CCNALAB #RSTP

