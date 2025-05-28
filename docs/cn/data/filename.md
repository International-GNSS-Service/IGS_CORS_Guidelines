&emsp;&emsp;目前，IGS支持三个主要的RINEX标准版本，即RINEXv.2、RINEXv.3和RINEXv.4。鼓励所有测站操作员传输最新可用的主/次版本。新建的IGS CORS必须提交至少符合RINEX 3.04版本的数据。

## 5.2.1 RINEX v.4/v.3

&emsp;&emsp;[RINEX v.3](https://files.igs.org/pub/data/format/rinex305.pdf) 和 [RINEX v.4](https://files.igs.org/pub/data/format/rinex_4.01.pdf) 中的数据必须采用以下文件命名规则：

*观测和气象文件：*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_FRU_DT.fff.cmp`

*导航文件：*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_DT.fff.cmp`

&emsp;&emsp;文件名主体的所有元素必须使用大写ASCII字母或数字，且所有元素均为固定长度并用下划线“_”分隔。文件类型和压缩字段（扩展名）使用点号“.”作为分隔符，且必须为小写的ASCII字符。各字段需用零填充至指定宽度，如下所示。

=== "SSSSMRCCC"
    九字符的IGS测站名称

    - SSSS：4字符，（现有）IGS测站名称
    - M：标石或标记的编号（0-9）
    - R：接收机编号（0-9）
    - CCC：ISO-3166国家或地区代码（3位字母）
    
    示例：POTS00DEU

    备注：为了与SINEX格式保持一致，目前不支持除0以外的标记和标石编号。
    
=== "S"
    数据来源

    支持R（来自接收机，使用厂商或其他软件）和S（RTCM或其它数据流格式）

=== "YYYYDDDHHMM"

    起始时间

    - YYYY：公历年份（如, 2024）
    - DDD：年积日（如, 260）
    - HHMM：天内时和天内分（如, 1000）

    优先使用文件的标称起始时间，也可以使用实际起始时间。

=== "DDU"
    文件时段

    - DD：文件时长
    - U：时长单位
    - 可接受的值：15M, 01H, 01D

=== "FRU"
    数据频率

    - FR：数据频率
    - U：频率单位
    - 可接受的值：对高采样数据为01S，对小时/天数据为30S或15S

    RINEX导航文件不需要此字段。

=== "DT"
    数据类型

    - 两字符表示类型
    - D：卫星系统（允许的值：G，R，E，C，J，S，I和M（混合））
    - T：RINEX文件类型（允许的值：O，N，M）

    示例：MO

=== "fff"
    文件格式
    
    支持的值：rnx（RINEX）和crx（压缩RINEX）

=== "cmp"
    压缩格式
    
    支持的值：gzip（gz）

&emsp;&emsp;为了进一步减少观测文件大小，应使用Hatanaka压缩工具包。有关Hatanaka压缩方案的更多信息请访问：[https://terras.gsi.go.jp/ja/crx2rnx.html](https://terras.gsi.go.jp/ja/crx2rnx.html)。

## 5.2.2 RINEX v.2

&emsp;&emsp;RINEX v.2 [（Gurtner, 2007）](https://ﬁles.igs.org/pub/data/format/rinex211.txt)中的数据必须采用以下文件命名规则传输：

`ssssdddf.yyt`

&emsp;&emsp;下表列出了此命名规则的每个元素。建议传输RINEX v.2文件的测站提供gzip压缩文件。即使文件以Z-compression格式传输，IGS数据中心也将重新压缩这些文件并以[gzip格式公开提供](https://ﬁles.igs.org/pub/data/format/Addendum-rinex211.pdf)。

=== "ssss"
    4字符IGS测站名称

    示例：pots

=== "ddd"
    第一条记录的年积日

    示例：260

=== "f"
    单天的文件序列号/字符
    
    - 单天文件（30秒）：f=0
    - 小时文件（30秒）：
        - f=a（00:00:00 至 00:59:30）,
        - f=b（01:00:00 至 01:59:30）, 
        - ...
        - f=x（23:00:00 至 23:59:30）
    - 高采样文件（15分钟, 1赫兹）：
        - f=a00（00:00:00 至 00:14:59）
        - f=a15（00:15:00 至 00:29:59） ...
        - f=m30（12:30:00 至 12:44:59） ...
        - f=x45（23:45:00 至 23:59:59）

=== "yy"
    两位数年份（如, 24）

=== "t"
    文件类型
    
    允许类型：
      - O：观测文件
      - D：Hatanaka压缩观测文件
      - N：GPS导航文件
      - G：GLONASS导航文件
      - M：气象文件
