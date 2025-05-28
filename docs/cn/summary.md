&emsp;&emsp;本节概述了CORS加入IGS网所需满足的强制性和建议性要求。这些要求适用于现行IGS测站和拟建测站。尽管IGS明确希望测站全面遵守本指南规范，但在无法完全符合相关规定的情况下，建议测站运营方咨询基础设施委员会。有关这些要求的详细信息可参见本指南后续章节。

!!! info "图例"

    :material-check-bold: 最低要求

    :fontawesome-solid-triangle-exclamation: 推荐

    :x: 不推荐

## 常规

| 建议 | 分类  |
| -------------- | --------------- |
| 测站属于国家/区域大地测量网络[^1]                                      | :fontawesome-solid-triangle-exclamation: |
| 测站被规划为连续和永久运行站                             | :material-check-bold: |
| 测站运营机构具备维修、升级和维护能力 | :material-check-bold: |

## 基础与选址（第3.2.1节）

| 建议 | 分类  |
| -------------- | --------------- |
| 基岩或大型混凝土基础 | :material-check-bold: |
| 安装于建筑物或类似结构上[^2] | :x: |
| 在10度高度角以上视野开阔，仅存在有限的障碍物 | :material-check-bold: |
| 台站无信号遮挡或射频干扰 | :material-check-bold: |
| 台站无反射材料 | :material-check-bold: |

## 埋石与安装（第3.2节）

| 建议 | 分类  |
| -------------- | --------------- |
| 混凝土支柱或支撑式（三脚架、四脚架等）基座 | :material-check-bold: |
| 安装在建筑物上的（钢制）底座 | :x: |
| 底座将天线锁定在适当位置以保持其方向和水平 | :material-check-bold: |
| 相对于原始位置和方位，底座天线装卸的容许偏差为0.5毫米和1度 | :material-check-bold: |

## 供电与通信（第3.3节）

| 建议 | 分类  |
| -------------- | --------------- |
| 确保所有通信设备连续运行 | :fontawesome-solid-triangle-exclamation: |
| 确保可远程控制访问接收机 | :material-check-bold: |

## 接收机（第4.1节）

| 建议 | 分类  |
| -------------- | --------------- |
| 对所有GNSS 进行多频码和载波相位跟踪[^3] | :material-check-bold: |
| 连续记录原始GNSS数据 | :fontawesome-solid-triangle-exclamation: |
| 实时数据流（RTCM） | :fontawesome-solid-triangle-exclamation: |
| 全视角卫星（健康和非健康）跟踪，最低5度高度角（鼓励0度） | :material-check-bold: |
| 禁用伪距和相位平滑 | :material-check-bold: |
| 禁用多路径抑制 | :material-check-bold: |
| 具备存储合理容量原始数据的能力（视具体情况而定） | :material-check-bold: |

## 天线（第4.2节）

| 建议 | 分类  |
| -------------- | --------------- |
| 使用列入官方 [IGS ANTEX](https://files.igs.org/pub/station/general/igs20.atx) 中的带有IGS校准的绝对天线相位中心（平均校准）的天线  | :material-check-bold: |
| 独立校准的绝对天线相位中心 | :fontawesome-solid-triangle-exclamation: |
| 天线应在真北方向5度范围内调平与定向 | :material-check-bold: |
| 天线罩保护 | :x: |

## 数据（第5节）

| 建议 | 分类  |
| -------------- | --------------- |
| 数据必须以RINEX格式提供[^4] | :material-check-bold: |
| 若提供实时数据流[^5]，则采用RTCM3 MSM5格式的数据流[^6] | :material-check-bold: |
| 通信中断后须向数据中心重新提交数据 | :material-check-bold: |
| RINEX数据须在接收机上直接或由原始二进制文件转换生成 | :material-check-bold: |
| 文件完整性目标 | 99% |

### 高采样RINEX文件（第5.1节）

| 建议 |             | 分类  |
| -------------- | ------------| --------------- |
| 提供      |             | :fontawesome-solid-triangle-exclamation: |
| 延迟        | < 5 分钟 | :material-check-bold: |
| 采样率  | 1 赫兹        | :material-check-bold: |
| 持续时间       | 15 分钟  | :material-check-bold: |

### 小时的RINEX文件（第5.1节）

| 建议 |             | 分类  |
| -------------- | ------------| --------------- |
| 提供      |             | :fontawesome-solid-triangle-exclamation: |
| 延迟        | < 5 分钟 | :material-check-bold: |
| 采样率  | 30 秒  | :material-check-bold: |

### 单天的RINEX文件（第5.1节）

| 建议 |             | 分类  |
| -------------- | ------------| --------------- |
| 提供      |             | :material-check-bold: |
| 延迟        | < 30 分钟| :material-check-bold: |
| 采样率  | 30 秒  | :material-check-bold: |

## 元数据（第5节）

| 建议 | 分类  |
| -------------- | --------------- |
| 完整且最新的IGS台站日志/GeodesyML格式的元数据 | :material-check-bold: |
| 由IGS批准的唯一九字符测站标识符 | :material-check-bold: |
| 分配唯一的IERS DOMES编号 | :material-check-bold: |
| 在台站变更后24小时内更新IGS测站日志 | :material-check-bold: |
| RINEX头文件与IGS元数据记录中的信息相符 | :material-check-bold: |
| 提供天线在四个主要方向（北、东、南、西）上的安装照片 | :material-check-bold: |

[^1]: 对位于APREF、EPN和SIRGAS覆盖范围内的区域CORS是强制性的。
[^2]: 经SPC审查后可获特许。
[^3]: 新测站应具备跟踪所有可用频率码和载波相位的能力。
[^4]: 对于新测站：最低须提供RINEX 3.04版本，不接受RINEX 2.11版本。
[^5]: 强烈建议新测站提供实时数据流。
[^6]: 鼓励使用MSM7。
