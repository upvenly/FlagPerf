### 模型Checkpoint下载
[模型Checkpoint下载](../README.md#模型checkpoint)
### 测试数据集下载
[测试数据集下载](../README.md#数据集)

### Nvidia GPU配置与运行信息参考
#### 环境配置
- ##### 硬件环境
    - 机器、加速卡型号: NVIDIA_A100-SXM4-40GB
    - 多机网络类型、带宽: InfiniBand，200Gb/s
- ##### 软件环境
   - OS版本：Ubuntu 20.04
   - OS kernel版本: 5.4.0-113-generic     
   - 加速卡驱动版本：470.129.06
   - Docker 版本：20.10.16
   - 训练框架版本：pytorch-1.8.0a0+52ea372
   - 依赖软件版本：无


### 运行情况
| 训练资源 | 配置文件        | 运行时长(s) | 目标精度 | 收敛精度 | Steps数 | 性能（samples/s) |
| -------- | --------------- | ----------- | -------- | -------- | ------- | ---------------- |
| 单机1卡  | config_A100x1x1 | 17049.92    | 0.8      | 0.8044   | 9600    | 4.66             |
| 单机2卡  | config_A100x1x2 | 8621.41     | 0.8      | 0.8065   | 4800    | 9.24             |
| 单机4卡  | config_A100x1x4 | 5386.60     | 0.8      | 0.8052   | 3000    | 18.47            |
| 单机8卡  | config_A100x1x8 | 2755.73     | 0.8      | 0.8059   | 1500    | 36.56            |
| 两机8卡  | config_A100x2x8 | 1417.68     | 0.8      | 0.8008   | 750     | 72.73            |

### 许可证


本项目基于Apache 2.0 license。

本项目部分代码基于MLCommons https://github.com/mlcommons/training_results_v1.0/tree/master/NVIDIA 实现。