# D-Link DIR-825 Unauthorized Remote Command Execution
An authorization command injection vulnerability about DIR-825

</br>**Exploit Author:** KeenSight Lab.Tgp (topsuchow@gmail.com)
</br>**Vender:** D-Link

## /cgi-bin/webupg
**Firmware version:** 
DIR-825(G1): all
</br>......
<br/>**Hardware Link:**https://downloads.d-link.co.za/DIR/dir825%20(new)/firmware/
## The detail of vulnerability
#### 1.Authentication bypasses the vulnerability
In the "webupg" binary, attackers can bypass authentication through parameters "autoupgrade.asp", and perform functions such as downloading configuration files and updating firmware without authorization.

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
