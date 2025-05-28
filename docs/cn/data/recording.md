&emsp;&emsp;IGS CORS至少需要提供采样率为30秒的单天RINEX观测文件。采样率可以是15秒，但不鼓励。此外，要求测站操作员提供RINEX导航文件[^1].

&emsp;&emsp;建议提供采样率为30秒的RINEX小时文件。鼓励新建的IGS测站尽可能提供采样率为30秒的RINEX小时文件，以及在可行情况下提供15分钟的高采样（1赫兹）RINEX文件（见“高采样数据”节）。

&emsp;&emsp;每个RINEX文件必须发送到至少两个全球IGS数据中心[^2]。若测站已被纳入区域网络（如APREF、EPN、SIRGAS）且数据已公开，则发送到一个全球数据中心即可。数据传输由IGS网络协调员协调管理。

&emsp;&emsp;通信中断后，缺失的数据文件需提交到数据中心。应向相关组织发送说明中断详情的公告（见[第5.5节](../announcements)）。

&emsp;&emsp;以下列出了每个IGS CORS在信号跟踪、数据记录和数据传输方面应满足的关键指标。

**信号跟踪与数据归档**

- 需完整观测、记录与归档全天99%的可用历元（每日中断时间小于15分钟）
- 需完整观测、记录与归档全年99%的可用历元（全年累计中断时间小于91小时）。

**数据传输**

- 小时数据文件应在每小时结束后的5分钟内完成归档。
- 单天数据文件应在每日结束后的30分钟内完成归档。

**中断后数据补传**

- 所有缺失的单天文件需尽快补传。
- 至少需补传最近三个整天的缺失小时文件。

## 5.1.1 高采样数据

&emsp;&emsp;为支持近实时应用（NRT），鼓励测站操作员提供时长为15分钟、采样率为1赫兹（若适用）的RINEX观测文件和导航文件。此类文件可通过实时数据流生成或由接收机直接记录。
&emsp;&emsp;参与提供高采样数据的测站，建议在最后一个观测历元结束后的5分钟内提交文件。

## 5.1.2 实时数据

&emsp;&emsp;实时测站除了满足常规IGS测站标准外，还需要以至少1赫兹的采样间隔传输GNSS观测数据流。所有新建IGS测站必须具备实时数据传输能力，除非测站对参考框架有贡献（如与SLR或VLBI测站并置），或位于有地理需求的区域。
&emsp;&emsp;IGS实时测站需满足的要求详见参考文献的第2节：[Guidelines for IGS Real-Time Broadcasters and Stations](https://files.igs.org/pub/resource/guidelines/Guidelines-for-IGS-Real-Time-Broadcasters-and-Stations_v1.0.pdf)

## 5.1.3 气象数据

&emsp;&emsp;建议在IGS CORS站安装精密气象设备。传感器具体要求见[第4.4节](../equipment/meteo_sensors.md)。至少提供气压和温度的测量数据，并以RINEX格式分发。（气象）RINEX文件应与RINEX观测文件同步传输（小时和/或单天）。

[^1]: 为了减少文件数量，建议发送包含所有导航数据的混合导航文件。
[^2]: 全球IGS数据中心的完整列表可在IGS官网查询: [https://igs.org/data-access/#data-centers](https://igs.org/data-access/#data-centers)