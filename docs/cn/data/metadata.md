&emsp;&emsp;GNSS元数据指台站的相关信息，包括台站所有权、联系方式、标石信息、台站坐标及设备安装历史。可靠且最新的元数据对GNSS测站管理与使用至关重要，由测站操作员负责维护。

## 5.4.1 IGS台站日志/GeodesyML

&emsp;&emsp;IGS要求CORS以IGS台站日志（ASCII）或GeodesyML记录并维护元数据，并向IGS和所有用户公开。IGS通过[网页应用程序](https://slm.igs.org)来维护测站元数据。

&emsp;&emsp;所有CORS必须完成并发布元数据，以便为分析中心与用户提供一致的台站信息分发方法。CORS操作员可能需要保留额外的元数据以支持内部管理与运营。

&emsp;&emsp;所有IGS测站使用唯一的九字符缩写进行标识。前四个字符应全球唯一，通常选择代表台站所在的郊区、城镇或（其他）位置的名称。GNSS操作员应与IGS网络协调员确认拟用于新建CORS的四字符标识尚未使用。可从Scripps轨道与永久阵列中心（[SOPAC](http://sopac-old.ucsd.edu/checkSiteID.shtml)）获得当前和历史CORS台站四字符标识的非详尽列表。此外，每个IGS CORS都需要申请一个[IERS DOMES编号](domes-request)。通过查询[IERS DOMES编号列表](domes-list)，确保拟使用的四字符代码没有用于其他大地测量技术。

## 5.4.2 RINEX头文件

&emsp;&emsp;RINEX头文件必须与IGS台站日志中记录的元数据一致。若存在元数据差异，应重新提交RINEX文件。RINEX头文件中的所有信息必须采用ASCII编码。使用其他编码标准（如UTF-8）的字符可能导致解码时头文件元素移位，如使用变音符。表10列出了每个RINEX头文件必须包含的头文件元素。

| RINEX 头文件元素  | 建议 | 示例 |
| --------------------- | --------------- | ------- |
| `标记名称（MARKER NAME）`         | <ul><li>建议使用九字符测站代码。</li><li>也可使用四字符测站代码。</li><li>所有字母必须大写。</li></ul> | OUS200NZL<br>OUS2 |
| `标记编号（MARKER NUMBER）`       | <ul><li>IERS Domes 编号。</li><li>所有字母必须大写。 | 50212M002 |
| `标记类型（MARKER TYPE）`         | <ul><li>必须设置为 GEODETIC. ||
| `观测员（OBSERVER）`            | <ul><li>建议提供通用的电子邮件地址。 </li><li>最大字符数为20。 | gnss@agency.org |
| `机构（AGENCY）`              | <ul><li>建议使用IGS台站日志第11节和第12节中规定的机构缩写。<li>如果列出多个机构，使用斜杠（“/”）分隔。<li>最大字符数为60。 | OUSD/GFZ |
| `接收机编号/型号/版本（REC # / TYPE / VERS）` | <ul><li>所有接收机信息必须与IGS台站日志中的元数据一致。<ul><li> 第1列：接收机序列号 <li> 第2列：接收机型号 <li> 第3列：接收机固件版本||
| `天线编号/型号（ANT # / TYPE）`        | <ul><li>所有天线信息必须与IGS台站日志中的元数据一致。<ul><li> 第1列：天线序列号 <li> 第2列：天线型号 ||
| `近似位置 XYZ（APPROX POSITION XYZ）` | <ul><li>近似坐标应该与IGS台站日志中所述的坐标保持1米以内的精度一致。 ||
| `天线：ΔH/E/N（ANTENNA: DELTA H/E/N）` | <ul><li>天线偏心率应与IGS台站日志中的一致。 ||

## 5.4.3 数字照片

&emsp;&emsp;每个CORS必须提供天线安装位置的四个基本方向（最好每45°拍摄，共8张照片）、标石及其周围环境的照片。在台站发生任何事件或硬件变更后，这些照片应该及时更新。
照片必须采用以下命名规则进行标记和命名：

`SSSSMRCCC_YYYYMMDD_D[D].fff`

&emsp;&emsp;下表描述了该规则的各个元素。所有元素之间用下划线（“_”）分隔。

| 组件   | 描述 | 示例 |
| ----------- | ----------- | ------- |
| `SSSSMRCCC` | <ul><li>九字符测站代码。 | NYA200NOR |
| `YYYYMMDD`  | <ul><li>（变更）启用日期（年、月、日），无分隔符且以零填充。 | 20210131 |
| `D[D]`      | <ul><li>基本方向：N、E、S、W及其两两组合<li>天线序列号：AS<li>天线底座：AM<li>接收机：R<li>标石：M | N (North)<br>SE (South-East) |
| `fff`      | <ul><li>图像文件格式。<li>支持JPEG和PNG格式。 | .jpg |

&emsp;&emsp;或者可将照片上传至测站操作员或其上级组织管理的网站。

## 5.4.4 单天线校准

&emsp;&emsp;虽然不是强制性的，但建议提供单独的天线校准信息。这些信息对不同IGS工作组（如天线工作组）的活动和研究非常有用。相应的ANTEX文件需提供给IGS网络协调员。

## 5.4.5 数据保护合规性

&emsp;&emsp;欧盟和其他国家实施了关于个人数据保护的法规。由于IGS没有设置严格意义的法律代理部门，IGS只是一个自愿联合组织，因此IGS不希望处理这些法规带来的各种细节问题。
&emsp;&emsp;因此，要求将所有元数据（IGS台站日志/GeodesyML）和RINEX头文件（全名和电子邮件地址）中的个人信息替换为通用名称和邮件列表，例如：

- IGS台站日志/GeodesyML：
    - 联系人姓名：“Agency”网络操作员
    - 电子邮件：gnss@agency.org
- RINEX头文件：
    - 观测员：gnss@agency.org
    - 注释附带免责声明信息

&emsp;&emsp;在获得许可前，新建的IGS测站必须遵守这些规定。更新测站元数据的操作员也需使用符合数据保护规定的联系信息。

[domes-request]: https://itrf.ign.fr/en/network/domes/request
[domes-list]: https://itrf.ign.fr/en/network/list