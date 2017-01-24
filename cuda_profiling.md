###[1]select the avg from the following nvprofling trace
```bash
==9630== NVPROF is profiling process 9630, command: ./h2d 1 0 1                 
==9630== Profiling application: ./h2d 1 0 1                                     
==9630== Profiling result:                                                      
"Time(%)","Time","Calls","Avg","Min","Max","Name"                               
%,us,,us,us,us,                                                                 
100.000000,3.840000,2,1.920000,1.504000,2.336000,"[CUDA memcpy HtoD]"           
==9708== NVPROF is profiling process 9708, command: ./h2d 1 0 1                 
==9708== Profiling application: ./h2d 1 0 1                                     
==9708== Profiling result:                                                      
"Time(%)","Time","Calls","Avg","Min","Max","Name"                               
%,us,,us,us,us,                                                                 
100.000000,3.968000,2,1.984000,1.632000,2.336000,"[CUDA memcpy HtoD]"  
```

