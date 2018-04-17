# HelloWorld
这是对GitHub的学习
对分支的尝试

1.更改一
2018/4/17
关于iis 配置问题的解决方法之一
问题是[Win32Exception (0x80004005): 拒绝访问。]

[ExternalException (0x80004005): 无法执行程序。所执行的命令为 "C:\wwwroot\lanjia_qx57c6\web\bin\roslyn\csc.exe" /shared /keepalive:"10" /noconfig  /fullpaths @"C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Temporary ASP.NET Files\root\037c0e7d\a7f491d1\gq3pb2ov.cmdline"。]


-----解决方案1--------------------
具体的不是很清楚，但下面的可以参考下。
允许匿名访问 IIS 应用程序。
启用模拟为 Web 应用程序在本地 Web.config 文件中，如下所示： 
<configuration>
<system.web>	
<identity impersonate="true" />
</system.web>
</configuration>
运行 IIS Lockdown 工具，或 IUSR _ COMPUTERNAME 或 Csc.exe 文件上的 IWAM _ COMPUTERNAME 帐户拒绝访问您请求该页面之前。
-----解决方案1--------------------
