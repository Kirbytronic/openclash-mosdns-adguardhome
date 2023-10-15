# openclash+mosdns+adguardhome配置

## AdGuard Home效果 (*平均处理时间4ms*)
![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/d3c19474-3d64-4c3d-b5dd-811ea4441330)
## 1.openclash配置
  ### 先去配置订阅里面订阅自己的机场
  ### 插件设置-模式设置(选择Redir-Host模式,不选FakeIP模式是因为会产生私有IP和SSH连接错误)
  ![{95CA935A-D7DF-46bc-B6FD-1CC2C95C5DF6}](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/a671f0a1-cf3e-4fc1-b1bc-6bdc37b52322)
  ### 插件设置-流量控制(取消勾选绕过中国大陆IP)
  ![{BEAEB8A9-DF40-4c1d-8759-5B08C964F899}](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/e3085d0e-c513-4390-a6a0-ac44ad5b0fe5)
  ### 插件设置-DNS设置
  ![{F69E74F8-1EC7-4151-9943-64902AEF1DE2}](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/265e428e-8da8-49ea-8f46-b7912bf21dc1)
  ### 插件设置-IPV6设置(不支持IPV6的话可以全部不勾选)
  ![{D620025A-E552-4a5d-AE52-B78A3717E013}](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/4a2f1895-8a7a-4747-a29e-b797647b805d)
  ### 插件设置-GEO数据库订阅(把三个选项都勾选，并更新)
  ![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/27078522-1ab9-4204-baf5-a1cc67233ddd)
  ### 复写设置-DNS设置(勾选自定义上游 DNS 服务器)
  #### NameServer只添加一条服务类型为UDP的dns规则，*服务器地址和端口为ADGuardHome的监听地址*
  ![{034158BD-AF11-40de-BEA4-4078405CBD98}](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/eefcfaa0-b6b9-4c9c-b446-16a1d8f67079)
  #### FallBack只添加一条服务类型为UDP的dns规则，*服务器地址和端口为ADGuardHome的监听地址*
  ![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/c9ccff26-ab38-44ec-928d-4fb6fe7ea2a1)
  ### 复写设置-Meta设置
  ![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/2fec384b-92ab-46c5-8cf4-cabae35cc3c1)

## 2.MosDNS配置
  ### 基本设置(*记住自己设置的监听端口号*)
  ![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/11550acf-3e49-47c9-b8e0-7cacc0409b69)
  ### 更新数据库
  ![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/2374fc4a-56ed-42c1-b339-3779fcec0049)

## 3.AdGuard Home配置
  ### luci界面配置
  ![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/12aff815-62bd-470f-b187-be376a339a8c)
  ### AdGuardHome设置界面-DNS设置(DNS地址填写你的MosDNS监听地址)
  ![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/cd37d7df-934e-4756-84ad-8e4455152ad5)
  ![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/98e13e78-fb16-4886-a868-156a5a3ec22c)
  ![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/1a5a1df4-f709-4b35-90ed-6ac7866911cf)

  ### 过滤器-NDS黑名单
  ![image](https://github.com/Kirbytronic/openclash-mosdns-adguardhome/assets/40047753/36a194aa-eccf-4d8a-99ec-e2dd3da4ce56)






  
