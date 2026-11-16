# ESP32_P1_reader
The purpose is to read the output of the P1 connector of smart-meter



for the connectic see shema.gif



		



#Here are the result for a sagecom XT211

 0-0:1.0.0(261105135123W)
 
 0-0:96.1.1(353733353631)
 
 1-0:1.8.1(001330.083*kWh)
 
 1-0:1.8.2(000948.870*kWh)
 
 1-0:2.8.1(009290.728*kWh)
 
 1-0:2.8.2(002454.424*kWh)
 
 0-0:96.14.0(0002)
 
 1-0:1.7.0(00.000*kW)
 
 1-0:2.7.0(00.744*kW)
 
 0-0:96.7.21(00062)
 
 0-0:96.7.9(00007)
 
 1-0:99.97.0(3)(0-0:96.7.19)(240725134853S)(0007186139*s)(240826051939S)(0000001345*s)(251119120721W)(0000000049*s)
 
 1-0:32.32.0(00003)
 
 1-0:52.32.0(00002)
 
 1-0:72.32.0(00002)
 
 1-0:32.36.0(00000)
 
 1-0:52.36.0(00000)
 
 1-0:72.36.0(00000)
 
 1-0:32.7.0(240.8*V)
 
 1-0:52.7.0(240.0*V)
 
 1-0:72.7.0(239.5*V)
 
 1-0:31.7.0(001*A)
 
 1-0:51.7.0(001*A)
 
 1-0:71.7.0(001*A)
 0-0:96.13.0()
 
 1-0:21.7.0(00.000*kW)
 
 1-0:22.7.0(00.255*kW)
 
 1-0:41.7.0(00.000*kW)
 
 1-0:42.7.0(00.232*kW)
 
 1-0:61.7.0(00.000*kW)
 
 1-0:62.7.0(00.256*kW)
 
load the prog into esp32 with arduino IDE ESP32_P1_READER.ino

connect to 192.168.4.1. fill the network and the passed


use the results of ESP32_P1_READER_DSMR to edit the following . attrib. in ESP32_P1_READER
if (strncmp(telegram, "1-0:1.8.1", strlen("1-0:1.8.1")) == 0)
    ECLT = getValue(telegram, len);
all of them so they match the list of results from ESP32_P1_READER_DSMR













