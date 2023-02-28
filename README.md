# AFRL Util Sim Helper files
### Various reusable files for verilog simulation
---

   author: Jay Convertino   
   
   date: 2023.02.25  
   
   details: Various helper funtions.   
   
   license: MIT   
   
---

![rtl_img](./rtl.png)

### IP USAGE
#### INSTRUCTIONS

##### Dependency include for fusesoc core file
``` 
  dep:
    depend:
      - AFRL:utility:sim_helper:1.0.0
```

### COMPONENTS
#### bin

* 8bit_count.bin : A 1 MB file of 0 to 255 binary values repeated.
* const_data.bin : A 1 MB file of DEADBEEF binary values repeated.
* random.bin : A 1 MB file of /dev/random binary values.

#### py

* file_check.py : Python script used to compare files at the end of a simualtion. Comparison by MD5SUM.
  
### fusesoc

* fusesoc_info.core created.
* No simulation, this contains scripts and binary data.
  * FUTURE: Unit Tests for scripts.
