# AFRL Util Sim Helper files
### Various reusable files for verilog simulation
---

![image](img/AFRL.png)

---

   author: Jay Convertino   
   
   date: 2023.02.25  
   
   details: Various helper funtions.   
   
   license: MIT   
   
---

### Version
#### Current
  - V1.0.0 - initial release

#### Previous
  - none

### IP USAGE
#### INSTRUCTIONS
See Components for usage information pertaining to each file.

##### Dependency include for fusesoc core file
``` 
  dep:
    depend:
      - AFRL:utility:sim_helper:1.0.0
```

### COMPONENTS
#### bin

* 8bit_count.bin : A 1 MiB file of 0 to 255 binary values repeated.
* const_data.bin : A 1 MiB file of DEADBEEF binary values repeated.
* random.bin : A 1 MiB file of /dev/random binary values.

#### py

##### file_check.py
* Python script used to compare files at the end of a simualtion. Comparison by MD5SUM. See code comments for details.
  * Add the following to the end of the fusesoc core file, only icarus is supported, and it pulls the needed file names based on the parameters containing FILE_NAME.

```
  scripts:
  file_check_icarus:
    cmd : [python3, file_check.py, icarus]
```
  
### fusesoc

* fusesoc_info.core created.
* No simulation, this contains scripts and binary data.
