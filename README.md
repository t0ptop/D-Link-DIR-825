# D-Link DIR-825 Unauthorized Remote Command Execution
An authorization command injection vulnerability about DIR-825

</br>**Exploit Author:** KeenSight Lab.Tgp (topsuchow@gmail.com)
</br>**Vender:** D-Link

## /cgi-bin/webupg
**Firmware version:** 
DIR-825(G1): all
</br>......
<br/>**Hardware Link:**https://downloads.d-link.co.za/DAP/dap1360/Firmware/Hardware%20Version%20F/
## The detail of vulnerability
In the "webupg" binary, because of the lack of parameter verification, attackers can use "file" parameters to execute arbitrary system commands after obtaining authorization.

#### Vulnerability trigger function
![image](https://github.com/tgp-top/DAP-1360/blob/4f10977bb7356d1393fefcba24ca438be95248b2/%E5%9B%BE%E7%89%87/5.png)


`UPGCGI_CreateDir`
![image](https://github.com/tgp-top/DAP-1360/blob/2d09c23efafd8d3199b0a84d5b159f3cdbd26638/%E5%9B%BE%E7%89%87/1.png)

`UPGCGI_Delete`
![image](https://github.com/tgp-top/DAP-1360/blob/2d09c23efafd8d3199b0a84d5b159f3cdbd26638/%E5%9B%BE%E7%89%87/2.png)

`UPGCGI_ModifyMac`
![image](https://github.com/tgp-top/DAP-1360/blob/2d09c23efafd8d3199b0a84d5b159f3cdbd26638/%E5%9B%BE%E7%89%87/3.png)

`Burpsuite intercept`
![image](https://github.com/tgp-top/DAP-1360/blob/220154515d7b765ecc8daffd6c990ba45df4735f/%E5%9B%BE%E7%89%87/4.png)
