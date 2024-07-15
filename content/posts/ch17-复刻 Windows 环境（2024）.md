+++
title = 'Ch17-复刻 Windows 环境（2024）'
date = 2024-05-26T23:35:19+08:00
lastmod = 2024-06-04T18:37:52+08:00
draft = false
tags = ["Windows", "记录", "MSYS2"]
categories = ["娱乐"]
+++

2024 年换机，记录当前顺手的 Windows 环境。

1. Desktop Apps；
2. Microsoft Store Apps；
3. MSYS2 Pkgs；
4. Powershell 配置；
5. Geek Uninstaller、AutoClock（shell:startup）、Traffic Monitor（[VC++运行时](https://docs.microsoft.com/zh-CN/cpp/windows/latest-supported-vc-redist?view=msvc-170)）、迅雷 11、B0pass、LS-DYNA、Fliqlo.scr等。
6. [停止 Windows 更新][1]，性能较低的 PC，可以关闭 Win11 的动画效果。

```cmd
@echo off  :: 阻止Windows更新
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsUpdate\UX\Settings" /v "FlightSettingsMaxPauseDays" /t REG_DWORD /d 15535
```

[1]: https://zhuanlan.zhihu.com/p/633610238

**跳过TPM验证安装Win11教程：**

Win10/Win11升级至Win11，可跳过TPM验证，采用脚本 [MediaCreationTool.bat](https://github.com/AveYo/MediaCreationTool.bat)。然后装载下载的镜像，使用镜像中的
setup.exe更新同样许可证版本的Windows11，可以保持个人数据与应用。

## 17.1 Desktop Apps

<div class="my-custom-class">
    <html>
<head>
<META http-equiv="Content-Type" content="text/html; charset=utf-8">
<style type="text/css">
.title{font: bold 10pt "Tahoma";color:#000000;}
.default{font: 8pt "Tahoma";color:#000000;}
.header{font: 8pt "Tahoma";color:#000000;}
.noborder{border-style:none;padding-left:4px;padding-right:4px;}
.normalborder {border-top:none; border-left:none; vertical-align:top;border-right:none;border-bottom:none;padding-left:4px;padding-right:4px;}
</style>
</head>
<body>
<p class="title">
已安装程序 (Software)
</p>
<p class="default">
由 <a href="https://geekuninstaller.com/">Geek Uninstaller 1.5.1</a> 于 Saturday, April 27, 2024 11:50:41 生成<br>WIN-PEOQDUKOHTK
</p>
<table class="default" bgcolor=#FFFFFF  cellspacing="0" cellpadding=4>
<tr class="header" style="padding-left:4px;padding-right:4px;">
<th height="20px" align=left colspan="2" bgcolor=#ECE9D8 width="600px">程序名称</th><th height="20px" align=left bgcolor=#ECE9D8 width="80px">大小</th><th height="20px" align=right bgcolor=#ECE9D8 width="120px">安装时间</th></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Edge WebView2 Runtime</td> <td class="normalborder"
height="34px" align=left>5.06 GB</td> <td class="normalborder"  height="34px" align=right>27.04.2024 08:50</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Lenovo Vantage Service</td> <td class="normalborder"
height="34px" align=left>2.93 GB</td> <td class="normalborder"  height="34px" align=right>27.04.2024 00:12</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Fork - a fast and friendly git client</td> <td class="normalborder"
height="34px" align=left>570 MB</td> <td class="normalborder"  height="34px" align=right>26.04.2024 18:56</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2015-2022 Redistributable (x64) - 14.38.33135</td> <td class="normalborder"
height="34px" align=left>20.6 MB</td> <td class="normalborder"  height="34px" align=right>22.04.2024 19:43</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">imFile 1.0.7</td> <td class="normalborder"
height="34px" align=left>274 MB</td> <td class="normalborder"  height="34px" align=right>22.04.2024 10:53</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">QQ</td> <td class="normalborder"
height="34px" align=left>598 MB</td> <td class="normalborder"  height="34px" align=right>22.04.2024 10:29</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">AntiCheatExpert</td> <td class="normalborder"
height="34px" align=left>73.1 MB</td> <td class="normalborder"  height="34px" align=right>14.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">START</td> <td class="normalborder"
height="34px" align=left>383 MB</td> <td class="normalborder"  height="34px" align=right>14.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">WPS Office (12.1.0.16729)</td> <td class="normalborder"
height="34px" align=left>0.99 GB</td> <td class="normalborder"  height="34px" align=right>14.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual Studio Code</td> <td class="normalborder"
height="34px" align=left>356 MB</td> <td class="normalborder"  height="34px" align=right>13.04.2024 20:18</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">DropIt (v8.5.1)</td> <td class="normalborder"
height="34px" align=left>7.68 MB</td> <td class="normalborder"  height="34px" align=right>12.04.2024 07:50</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Waterfox (x64 en-US)</td> <td class="normalborder"
height="34px" align=left>1.42 GB</td> <td class="normalborder"  height="34px" align=right>12.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft .NET Runtime - 8.0.4 (x64)</td> <td class="normalborder"
height="34px" align=left>98.2 MB</td> <td class="normalborder"  height="34px" align=right>11.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">XTerminal 1.20.23</td> <td class="normalborder"
height="34px" align=left>500 MB</td> <td class="normalborder"  height="34px" align=right>11.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">搜狗输入法 14.4.0正式版</td> <td class="normalborder"
height="34px" align=left>474 MB</td> <td class="normalborder"  height="34px" align=right>11.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Windows Desktop Runtime - 8.0.4 (x64)</td> <td class="normalborder"
height="34px" align=left>216 MB</td> <td class="normalborder"  height="34px" align=right>11.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">RayLink 8.0.3.8</td> <td class="normalborder"
height="34px" align=left>221 MB</td> <td class="normalborder"  height="34px" align=right>10.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Intel(R) Management Engine Components</td> <td class="normalborder"
height="34px" align=left>193 MB</td> <td class="normalborder"  height="34px" align=right>08.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">PowerToys (Preview) x64</td> <td class="normalborder"
height="34px" align=left>899 MB</td> <td class="normalborder"  height="34px" align=right>07.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">R for Windows 4.3.3</td> <td class="normalborder"
height="34px" align=left>173 MB</td> <td class="normalborder"  height="34px" align=right>06.04.2024 21:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">RStudio</td> <td class="normalborder"
height="34px" align=left>903 MB</td> <td class="normalborder"  height="34px" align=right>06.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft OneDrive</td> <td class="normalborder"
height="34px" align=left>4.73 GB</td> <td class="normalborder"  height="34px" align=right>05.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Edge Update</td> <td class="normalborder"
height="34px" align=left>4.41 GB</td> <td class="normalborder"  height="34px" align=right>04.04.2024 21:08</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">腾讯会议</td> <td class="normalborder"
height="34px" align=left>531 MB</td> <td class="normalborder"  height="34px" align=right>03.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Office 家庭和学生版 2016 - zh-cn</td> <td class="normalborder"
height="34px" align=left>3.07 GB</td> <td class="normalborder"  height="34px" align=right>02.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visio - zh-cn</td> <td class="normalborder"
height="34px" align=left>7.44 GB</td> <td class="normalborder"  height="34px" align=right>02.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">汽水音乐 1.6.1</td> <td class="normalborder"
height="34px" align=left>794 MB</td> <td class="normalborder"  height="34px" align=right>01.04.2024 11:27</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">qBittorrent</td> <td class="normalborder"
height="34px" align=left>176 MB</td> <td class="normalborder"  height="34px" align=right>01.04.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Fluent Reader 1.1.4</td> <td class="normalborder"
height="34px" align=left>253 MB</td> <td class="normalborder"  height="34px" align=right>30.03.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">EditPad Pro 7 v.7.3.1</td> <td class="normalborder"
height="34px" align=left>21.6 MB</td> <td class="normalborder"  height="34px" align=right>29.03.2024 22:13</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Oracle VM VirtualBox 7.0.14</td> <td class="normalborder"
height="34px" align=left>211 MB</td> <td class="normalborder"  height="34px" align=right>28.03.2024 23:44</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">爱校对插件</td> <td class="normalborder"
height="34px" align=left>8.05 MB</td> <td class="normalborder"  height="34px" align=right>27.03.2024 14:52</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Grammarly for Windows</td> <td class="normalborder"
height="34px" align=left>140 MB</td> <td class="normalborder"  height="34px" align=right>27.03.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">FxSound</td> <td class="normalborder"
height="34px" align=left>64.2 MB</td> <td class="normalborder"  height="34px" align=right>26.03.2024 18:19</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Cloudflare WARP</td> <td class="normalborder"
height="34px" align=left>281 MB</td> <td class="normalborder"  height="34px" align=right>26.03.2024 17:48</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">百度网盘</td> <td class="normalborder"
height="34px" align=left>847 MB</td> <td class="normalborder"  height="34px" align=right>21.03.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">微软OfficePLUS</td> <td class="normalborder"
height="34px" align=left>65.1 MB</td> <td class="normalborder"  height="34px" align=right>21.03.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Visual Basic for Application 7.0.1590</td> <td class="normalborder"
height="34px" align=left></td> <td class="normalborder"  height="34px" align=right>18.03.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Zotero</td> <td class="normalborder"
height="34px" align=left>458 MB</td> <td class="normalborder"  height="34px" align=right>15.03.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Edge</td> <td class="normalborder"
height="34px" align=left>169 MB</td> <td class="normalborder"  height="34px" align=right>11.03.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">网易云音乐</td> <td class="normalborder"
height="34px" align=left>375 MB</td> <td class="normalborder"  height="34px" align=right>10.03.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Todo清单 3.6.4</td> <td class="normalborder"
height="34px" align=left>230 MB</td> <td class="normalborder"  height="34px" align=right>10.03.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Q-Dir</td> <td class="normalborder"
height="34px" align=left>4.64 MB</td> <td class="normalborder"  height="34px" align=right>24.02.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">WinFsp 2023</td> <td class="normalborder"
height="34px" align=left>1.43 MB</td> <td class="normalborder"  height="34px" align=right>23.02.2024 07:26</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">CloudDrive2 版本 1.0</td> <td class="normalborder"
height="34px" align=left>43.3 MB</td> <td class="normalborder"  height="34px" align=right>23.02.2024 07:26</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">pot</td> <td class="normalborder"
height="34px" align=left>43.3 MB</td> <td class="normalborder"  height="34px" align=right>16.02.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">爱思助手7.0</td> <td class="normalborder"
height="34px" align=left>749 MB</td> <td class="normalborder"  height="34px" align=right>17.01.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">PowerShell 7-x64</td> <td class="normalborder"
height="34px" align=left>267 MB</td> <td class="normalborder"  height="34px" align=right>12.01.2024 12:50</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">uTools 4.0.1</td> <td class="normalborder"
height="34px" align=left>296 MB</td> <td class="normalborder"  height="34px" align=right>12.01.2024 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">MSC.Licensing 11.13</td> <td class="normalborder"
height="34px" align=left>27.0 MB</td> <td class="normalborder"  height="34px" align=right>11.01.2024 10:16</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Revision Tool version 1.6.2</td> <td class="normalborder"
height="34px" align=left>35.7 MB</td> <td class="normalborder"  height="34px" align=right>01.01.2024 00:13</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">WinSCP 6.1.2</td> <td class="normalborder"
height="34px" align=left>89.5 MB</td> <td class="normalborder"  height="34px" align=right>19.12.2023 01:15</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2005 Redistributable</td> <td class="normalborder"
height="34px" align=left>5.06 MB</td> <td class="normalborder"  height="34px" align=right>28.11.2023 00:29</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">TreeSize Free V4.7.1 (64 bit)</td> <td class="normalborder"
height="34px" align=left>49.2 MB</td> <td class="normalborder"  height="34px" align=right>28.11.2023 00:09</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">哈工程VPN</td> <td class="normalborder"
height="34px" align=left>39.5 MB</td> <td class="normalborder"  height="34px" align=right>08.11.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">LibreOffice 7.5.8.2</td> <td class="normalborder"
height="34px" align=left>696 MB</td> <td class="normalborder"  height="34px" align=right>05.11.2023 17:57</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">LibreOffice 7.5 Help Pack (Chinese (simplified))</td> <td class="normalborder"
height="34px" align=left>696 MB</td> <td class="normalborder"  height="34px" align=right>05.11.2023 17:44</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">PPSSPP</td> <td class="normalborder"
height="34px" align=left>85.3 MB</td> <td class="normalborder"  height="34px" align=right>31.10.2023 18:36</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">钉钉</td> <td class="normalborder"
height="34px" align=left>2.54 GB</td> <td class="normalborder"  height="34px" align=right>31.10.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">carnac</td> <td class="normalborder"
height="34px" align=left>20.2 MB</td> <td class="normalborder"  height="34px" align=right>23.10.2023 12:42</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">VLC media player</td> <td class="normalborder"
height="34px" align=left>179 MB</td> <td class="normalborder"  height="34px" align=right>20.10.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">ParaView</td> <td class="normalborder"
height="34px" align=left>1.49 GB</td> <td class="normalborder"  height="34px" align=right>04.10.2023 23:44</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Intel® oneAPI Base Toolkit</td> <td class="normalborder"
height="34px" align=left>13.9 GB</td> <td class="normalborder"  height="34px" align=right>24.09.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Intel® oneAPI HPC Toolkit</td> <td class="normalborder"
height="34px" align=left>13.9 GB</td> <td class="normalborder"  height="34px" align=right>24.09.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">MathType 6</td> <td class="normalborder"
height="34px" align=left>20.5 MB</td> <td class="normalborder"  height="34px" align=right>13.09.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">TIM</td> <td class="normalborder"
height="34px" align=left>407 MB</td> <td class="normalborder"  height="34px" align=right>12.09.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Update Health Tools</td> <td class="normalborder"
height="34px" align=left>1.02 MB</td> <td class="normalborder"  height="34px" align=right>25.08.2023 14:15</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Patran 2019</td> <td class="normalborder"
height="34px" align=left>3.74 GB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 09:59</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2008 Redistributable - x86 9.0.30729.6161</td> <td class="normalborder"
height="34px" align=left>10.1 MB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 09:59</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2010  x86 Redistributable - 10.0.30319</td> <td class="normalborder"
height="34px" align=left>9.71 MB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 09:59</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2008 Redistributable - x86 9.0.30729.17</td> <td class="normalborder"
height="34px" align=left>10.2 MB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 09:59</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2010  x64 Redistributable - 10.0.30319</td> <td class="normalborder"
height="34px" align=left>12.3 MB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 09:58</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Dassault Systemes Software VC9 Prerequisites x86-x64</td> <td class="normalborder"
height="34px" align=left>21.9 MB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 09:58</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2008 Redistributable - x64 9.0.30729.17</td> <td class="normalborder"
height="34px" align=left>12.4 MB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 09:58</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">阿里云盘</td> <td class="normalborder"
height="34px" align=left>325 MB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">向日葵远程控制</td> <td class="normalborder"
height="34px" align=left>90.4 MB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2012 Redistributable (x64) - 11.0.61030</td> <td class="normalborder"
height="34px" align=left>20.5 MB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2012 Redistributable (x86) - 11.0.61030</td> <td class="normalborder"
height="34px" align=left>17.3 MB</td> <td class="normalborder"  height="34px" align=right>17.08.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">7-Zip 23.01 (x64)</td> <td class="normalborder"
height="34px" align=left>5.52 MB</td> <td class="normalborder"  height="34px" align=right>14.08.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">SumatraPDF</td> <td class="normalborder"
height="34px" align=left>38.3 MB</td> <td class="normalborder"  height="34px" align=right>13.08.2023 16:03</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Inkscape</td> <td class="normalborder"
height="34px" align=left>535 MB</td> <td class="normalborder"  height="34px" align=right>13.08.2023 16:02</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">ToDesk</td> <td class="normalborder"
height="34px" align=left>259 MB</td> <td class="normalborder"  height="34px" align=right>11.08.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">WeChat</td> <td class="normalborder"
height="34px" align=left>574 MB</td> <td class="normalborder"  height="34px" align=right>22.07.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Chocolatey (Install Only)</td> <td class="normalborder"
height="34px" align=left>4.88 MB</td> <td class="normalborder"  height="34px" align=right>20.07.2023 11:17</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Bonjour</td> <td class="normalborder"
height="34px" align=left>616 KB</td> <td class="normalborder"  height="34px" align=right>25.06.2023 21:18</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Apple Mobile Device Support</td> <td class="normalborder"
height="34px" align=left>45.3 MB</td> <td class="normalborder"  height="34px" align=right>25.06.2023 21:18</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Miniforge3 23.1.0-1 (Python 3.10.10 64-bit)</td> <td class="normalborder"
height="34px" align=left>5.49 GB</td> <td class="normalborder"  height="34px" align=right>19.06.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">oCam版本520.0</td> <td class="normalborder"
height="34px" align=left>30.6 MB</td> <td class="normalborder"  height="34px" align=right>19.05.2023 10:27</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">剪映专业版</td> <td class="normalborder"
height="34px" align=left></td> <td class="normalborder"  height="34px" align=right>19.05.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Inno Setup version 6.2.2</td> <td class="normalborder"
height="34px" align=left>15.1 MB</td> <td class="normalborder"  height="34px" align=right>12.05.2023 10:56</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Honeyview</td> <td class="normalborder"
height="34px" align=left>38.8 MB</td> <td class="normalborder"  height="34px" align=right>12.05.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">CAJViewer</td> <td class="normalborder"
height="34px" align=left>128 MB</td> <td class="normalborder"  height="34px" align=right>13.03.2023 11:17</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Windows Desktop Runtime - 6.0.14 (x64)</td> <td class="normalborder"
height="34px" align=left>210 MB</td> <td class="normalborder"  height="34px" align=right>28.02.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2013 Redistributable (x64) - 12.0.30501</td> <td class="normalborder"
height="34px" align=left>20.5 MB</td> <td class="normalborder"  height="34px" align=right>23.02.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2013 Redistributable (x86) - 12.0.30501</td> <td class="normalborder"
height="34px" align=left>17.1 MB</td> <td class="normalborder"  height="34px" align=right>23.02.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft MPI (10.1.12498.16)</td> <td class="normalborder"
height="34px" align=left>4.37 GB</td> <td class="normalborder"  height="34px" align=right>21.02.2023 20:42</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft MPI SDK (10.1.12498.16)</td> <td class="normalborder"
height="34px" align=left>8.20 MB</td> <td class="normalborder"  height="34px" align=right>21.02.2023 20:42</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">知云文献翻译 版本 7.8.0</td> <td class="normalborder"
height="34px" align=left>334 MB</td> <td class="normalborder"  height="34px" align=right>16.02.2023 19:46</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2008 Redistributable - x64 9.0.30729.6161</td> <td class="normalborder"
height="34px" align=left>13.2 MB</td> <td class="normalborder"  height="34px" align=right>13.02.2023 15:41</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2005 Redistributable (x64)</td> <td class="normalborder"
height="34px" align=left>6.83 MB</td> <td class="normalborder"  height="34px" align=right>13.02.2023 15:41</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">QTTabBar ver 2048</td> <td class="normalborder"
height="34px" align=left>8.20 MB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 14:14</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">福昕高级PDF编辑器</td> <td class="normalborder"
height="34px" align=left>932 MB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 14:12</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Windows SDK AddOn</td> <td class="normalborder"
height="34px" align=left>152 KB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 13:39</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft .NET Framework 4 Multi-Targeting Pack</td> <td class="normalborder"
height="34px" align=left>83.4 MB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 13:34</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual Studio Installer</td> <td class="normalborder"
height="34px" align=left>59.8 MB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 13:31</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Notepad3 (x64) 6.23.203.2</td> <td class="normalborder"
height="34px" align=left>22.5 MB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 13:30</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">MSYS2</td> <td class="normalborder"
height="34px" align=left>12.7 GB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 13:09</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Realtek Card Reader</td> <td class="normalborder"
height="34px" align=left>15.1 MB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 12:54</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Neat Download Manager version 1.4</td> <td class="normalborder"
height="34px" align=left>2.31 MB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 12:32</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Visual Studio Community 2019</td> <td class="normalborder"
height="34px" align=left>2.90 GB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Windows Software Development Kit - Windows 10.0.19041.685</td> <td class="normalborder"
height="34px" align=left>2.00 GB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Visual C++ 2015-2019 Redistributable (x86) - 14.29.30139</td> <td class="normalborder"
height="34px" align=left>17.9 MB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 00:00</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Everything 1.4.1.935 (x64)</td> <td class="normalborder"
height="34px" align=left>50.7 MB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 00:00</td></tr>
</table><hr><p class="default">
总计 <b>113</b> 个程序占用空间 <b>111 GB</b>
</p></body></html>
</div>

经验：

1. 建议在 Everything 中设置索引数据库存储路径，以避免频繁启动时重新检索磁盘。

## 17.2 Microsoft Store Apps

<div class="my-custom-class">
<html>
<head>
<META http-equiv="Content-Type" content="text/html; charset=utf-8">
<style type="text/css">
.title{font: bold 10pt "Tahoma";color:#000000;}
.default{font: 8pt "Tahoma";color:#000000;}
.header{font: 8pt "Tahoma";color:#000000;}
.noborder{border-style:none;padding-left:4px;padding-right:4px;}
.normalborder {border-top:none; border-left:none; vertical-align:top;border-right:none;border-bottom:none;padding-left:4px;padding-right:4px;}
</style>
</head>
<body>
<p class="title">
已安装程序 (Software)
</p>
<p class="default">
由 <a href="https://geekuninstaller.com/">Geek Uninstaller 1.5.1</a> 于 Wednesday, April 10, 2024 07:32:14 生成<br>WIN-PEOQDUKOHTK
</p>
<table class="default" bgcolor=#FFFFFF  cellspacing="0" cellpadding=4>
<tr class="header" style="padding-left:4px;padding-right:4px;">
<th height="20px" align=left colspan="2" bgcolor=#ECE9D8 width="600px">程序名称</th><th height="20px" align=left bgcolor=#ECE9D8 width="80px">大小</th><th height="20px" align=right bgcolor=#ECE9D8 width="120px">安装时间</th></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Edge</td> <td class="normalborder"
height="34px" align=left>83.0 KB</td> <td class="normalborder"  height="34px" align=right>07.04.2024 23:03</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Windows Package Manager Source (winget)</td> <td class="normalborder"
height="34px" align=left>9.87 MB</td> <td class="normalborder"  height="34px" align=right>06.04.2024 20:52</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Copilot</td> <td class="normalborder"
height="34px" align=left>138 KB</td> <td class="normalborder"  height="34px" align=right>28.03.2024 23:20</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">云·星穹铁道</td> <td class="normalborder"
height="34px" align=left>356 KB</td> <td class="normalborder"  height="34px" align=right>21.03.2024 17:22</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Notion</td> <td class="normalborder"
height="34px" align=left>69.0 KB</td> <td class="normalborder"  height="34px" align=right>18.03.2024 16:13</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">QQ邮箱</td> <td class="normalborder"
height="34px" align=left>195 KB</td> <td class="normalborder"  height="34px" align=right>13.03.2024 23:12</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Spotify</td> <td class="normalborder"
height="34px" align=left>88.0 KB</td> <td class="normalborder"  height="34px" align=right>13.03.2024 23:03</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">YouTube</td> <td class="normalborder"
height="34px" align=left>50.0 KB</td> <td class="normalborder"  height="34px" align=right>11.03.2024 11:47</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Debian</td> <td class="normalborder"
height="34px" align=left>490 MB</td> <td class="normalborder"  height="34px" align=right>10.03.2024 10:47</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">抖音</td> <td class="normalborder"
height="34px" align=left>60.0 KB</td> <td class="normalborder"  height="34px" align=right>04.03.2024 16:25</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Pantone Color of the Year 2022</td> <td class="normalborder"
height="34px" align=left>3.33 MB</td> <td class="normalborder"  height="34px" align=right>01.01.2024 00:29</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Lenovo Vantage</td> <td class="normalborder"
height="34px" align=left>645 MB</td> <td class="normalborder"  height="34px" align=right>09.12.2023 18:48</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">App Installer</td> <td class="normalborder"
height="34px" align=left>142 MB</td> <td class="normalborder"  height="34px" align=right>19.11.2023 22:50</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">WinGet COM Server</td> <td class="normalborder"
height="34px" align=left>142 MB</td> <td class="normalborder"  height="34px" align=right>19.11.2023 22:50</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Windows Package Manager Client</td> <td class="normalborder"
height="34px" align=left>142 MB</td> <td class="normalborder"  height="34px" align=right>19.11.2023 22:50</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">App Installer</td> <td class="normalborder"
height="34px" align=left>142 MB</td> <td class="normalborder"  height="34px" align=right>19.11.2023 22:50</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">wolai</td> <td class="normalborder"
height="34px" align=left>65.0 KB</td> <td class="normalborder"  height="34px" align=right>10.11.2023 16:57</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">终端</td> <td class="normalborder"
height="34px" align=left>17.5 MB</td> <td class="normalborder"  height="34px" align=right>06.11.2023 12:28</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Store</td> <td class="normalborder"
height="34px" align=left>68.0 MB</td> <td class="normalborder"  height="34px" align=right>05.11.2023 18:05</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Calculator</td> <td class="normalborder"
height="34px" align=left>18.9 MB</td> <td class="normalborder"  height="34px" align=right>05.11.2023 18:04</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">中文(简体)本地体验包</td> <td class="normalborder"
height="34px" align=left>62.1 MB</td> <td class="normalborder"  height="34px" align=right>05.11.2023 18:02</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">有道云笔记</td> <td class="normalborder"
height="34px" align=left>104 KB</td> <td class="normalborder"  height="34px" align=right>02.11.2023 10:47</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">NxShell</td> <td class="normalborder"
height="34px" align=left>323 MB</td> <td class="normalborder"  height="34px" align=right>01.09.2023 13:30</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Store Experience Host</td> <td class="normalborder"
height="34px" align=left>34.2 MB</td> <td class="normalborder"  height="34px" align=right>24.08.2023 14:19</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">HEIF Image Extensions</td> <td class="normalborder"
height="34px" align=left>5.57 MB</td> <td class="normalborder"  height="34px" align=right>24.08.2023 14:19</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Intel® Graphics Command Center</td> <td class="normalborder"
height="34px" align=left>122 MB</td> <td class="normalborder"  height="34px" align=right>13.08.2023 12:50</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">百度网盘</td> <td class="normalborder"
height="34px" align=left>4.36 MB</td> <td class="normalborder"  height="34px" align=right>09.08.2023 15:07</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Webp Image Extensions</td> <td class="normalborder"
height="34px" align=left>914 KB</td> <td class="normalborder"  height="34px" align=right>09.08.2023 15:06</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Web 媒体扩展</td> <td class="normalborder"
height="34px" align=left>2.71 MB</td> <td class="normalborder"  height="34px" align=right>02.07.2023 00:53</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">VP9 Video Extensions</td> <td class="normalborder"
height="34px" align=left>5.58 MB</td> <td class="normalborder"  height="34px" align=right>24.06.2023 12:22</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Snip & Sketch</td> <td class="normalborder"
height="34px" align=left>3.81 MB</td> <td class="normalborder"  height="34px" align=right>31.03.2023 09:57</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">ELAN TrackPoint for Thinkpad</td> <td class="normalborder"
height="34px" align=left>1.14 MB</td> <td class="normalborder"  height="34px" align=right>14.02.2023 15:48</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">ELAN Touchpad for Thinkpad</td> <td class="normalborder"
height="34px" align=left>997 KB</td> <td class="normalborder"  height="34px" align=right>14.02.2023 15:48</td></tr>
<tr class="default">
<td class="normalborder"  height="34px" align=left colspan="2">Microsoft Pay</td> <td class="normalborder"
height="34px" align=left>4.96 MB</td> <td class="normalborder"  height="34px" align=right>11.02.2023 12:17</td></tr>
</table><hr><p class="default">
总计 <b>34</b> 个程序占用空间 <b>2.34 GB</b>
</p></body></html>
</div>

## 17.3 MSYS2 环境

2024 年 4 月开始，更换笔记本，将新笔记本的 [MSYS2 环境设为 UCRT64][4]。

[MSYS2][2] 是作者主力编程和开源工具环境，提供了诸如 GCC、Python 等编程环境，也提供了诸如 mdbook、LaTex、inkscape
等工具。

常用命令：

```sh
pacman -Syu         # 更新包索引
pacman -S <pkg>     # 安装包
pacman -Rs <pkg>    # 删除包
```

国内开发者可以使用[清华大学的镜像][3]。

[2]: https://mirrors.tuna.tsinghua.edu.cn/msys2/distrib/x86_64/
[3]: https://mirrors.tuna.tsinghua.edu.cn/help/msys2/
[4]: https://my.oschina.net/zuozhihua/blog/8757266

```sh
$ pacman -Qe
mingw-w64-clang-x86_64-clang 17.0.6-7
mingw-w64-clang-x86_64-cmake 3.28.3-2
mingw-w64-clang-x86_64-llvm-15 15.0.7-2
mingw-w64-clang-x86_64-ninja 1.11.1-3
mingw-w64-x86_64-argparse-f 0.1.0-1
mingw-w64-x86_64-binutils 2.41-1
mingw-w64-x86_64-cmake 3.27.2-1
mingw-w64-x86_64-crt-git 11.0.0.r107.gd367cc9d7-1
mingw-w64-x86_64-fastfetch 2.1.2-1
mingw-w64-x86_64-fffc 1.5.202310-1
mingw-w64-x86_64-flang 17.0.6-1
mingw-w64-x86_64-fortran-stdlib 0.3.0-1
mingw-w64-x86_64-fpm 0.10.0-1
mingw-w64-x86_64-fzf 0.48.1-1
mingw-w64-x86_64-gcc 13.2.0-2
mingw-w64-x86_64-gcc-fortran 13.2.0-2
mingw-w64-x86_64-gcc-libgfortran 13.2.0-2
mingw-w64-x86_64-gcc-libs 13.2.0-2
mingw-w64-x86_64-gcc-objc 13.2.0-2
mingw-w64-x86_64-gdb 13.2-3
mingw-w64-x86_64-github-cli 2.32.0-1
mingw-w64-x86_64-go 1.21.0-2
mingw-w64-x86_64-h5part 1.2.20230625-1
mingw-w64-x86_64-headers-git 11.0.0.r107.gd367cc9d7-2
mingw-w64-x86_64-kiss_fft 1.3.1-1
mingw-w64-x86_64-lfortran 0.33.1-2
mingw-w64-x86_64-libgccjit 13.2.0-2
mingw-w64-x86_64-libmangle-git 11.0.0.r107.gd367cc9d7-1
mingw-w64-x86_64-libwinpthread-git 11.0.0.r107.gd367cc9d7-1
mingw-w64-x86_64-llvm-15 15.0.7-1
mingw-w64-x86_64-lua 5.4.6-2
mingw-w64-x86_64-make 4.4-2
mingw-w64-x86_64-mdbook 0.4.37-1
mingw-w64-x86_64-meson 1.2.1-1
mingw-w64-x86_64-minpack 2.0.0-1
mingw-w64-x86_64-nnps 1.3.0-1
mingw-w64-x86_64-octave 9.1.0-4
mingw-w64-x86_64-onefetch 2.18.1-3
mingw-w64-x86_64-pkgconf 1~2.0.1-1
mingw-w64-x86_64-python-ipykernel 6.25.2-1
mingw-w64-x86_64-python-jupyter_notebook 7.0.6-1
mingw-w64-x86_64-python-matplotlib 3.7.1-2
mingw-w64-x86_64-python-pandas 2.2.1-1
mingw-w64-x86_64-python-pip 23.2.1-2
mingw-w64-x86_64-python-scipy 1.11.1-2
mingw-w64-x86_64-python-toml 0.10.2-4
mingw-w64-x86_64-python-websocket-client 1.6.2-1
mingw-w64-x86_64-quadrature-fortran 1.0.0-1
mingw-w64-x86_64-rust 1.72.0-1
mingw-w64-x86_64-scc 3.1.0-1
mingw-w64-x86_64-sccache 0.5.4-1
mingw-w64-x86_64-seakeeping 2.7.202312-1
mingw-w64-x86_64-starship 1.17.1-2
mingw-w64-x86_64-test-drive 0.4.0-1
mingw-w64-x86_64-tools-git 11.0.0.r107.gd367cc9d7-1
mingw-w64-x86_64-winpthreads-git 11.0.0.r107.gd367cc9d7-1
mingw-w64-x86_64-winstorecompat-git 11.0.0.r107.gd367cc9d7-1
```

## 17.4 Powershell 配置

* [Starship](https://starship.rs/)：跨平台的 Shell 提示符；
* [PSReadLine](https://github.com/PowerShell/PSReadLine)：PowerShell 命令行界面。

```powershell
# PWD: C:\Users\zoziha\Documents\WindowsPowerShell 或者 C:\Users\zoziha\Documents\PowerShell
# 命令：notepad $PROFILE
# 依赖：
# - Startship
# - PSReadLine

Import-Module PSReadLine
Set-PSReadLineOption -PredictionSource History
# 下面是三条是文档里推荐的，根据自己的习惯决定是否添加
# 其他有用的命令是：
# - F2 选择历史命令;
# - Ctrl-l 清屏;
# - Ctrl-左右键 跳转.
Set-PSReadLineKeyHandler -Key Tab -Function Complete
Set-PSReadlineKeyHandler -Key UpArrow -Function HistorySearchBackward
Set-PSReadlineKeyHandler -Key DownArrow -Function HistorySearchForward

Invoke-Expression (starship init powershell)        # Starship
[System.Console]::OutputEncoding=[System.Text.Encoding]::GetEncoding(65001)     # utf-8
```

## 17.5 Edge 浏览器插件

1. [uBlock Origin](https://github.com/gorhill/uBlock)：阻止广告、跟踪、恶意软件；
2. [豆包](https://www.doubao.com/chat/)：网页翻译和总结。
