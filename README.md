# Lithum Battery Health Analysis

## Version 1
### Data Collection

【数据背景】新能源车电池模组的充放电数据是指电池在使用过程中进行充电和放电时所记录的相关信息。这些数据包含了电池的性能指标、工作状态和使用情况，可以帮助监测和评估电池的健康状况、性能表现以及寿命预测。这些数据通过车辆的电池管理系统（Battery Management System，简称BMS）进行监测和记录。基于这些数据，制造商和维护人员可以进行电池性能分析、故障诊断以及优化电池使用和充电策略。同时，这些数据也可以用于研究和改进电池技术，提高新能源车的续航里程和可靠性。

【应用领域】AI+电池充放电

【文件目录】20个#x的csv数据文件（比如第一辆的名称就是#1.csv）

【数据说明】共20辆新能源车的电池模组充放电数据，每个#x代表一辆新能源车电池模组的充放电数据，数据时间段为2019/07/25—2021/11/15，数据跨度约29个月，数据集大小约1.1GB。每个csv数据表包含10个数据字段，具体如下：

1. record_time：时间戳
2. soc：车辆电池剩余容量，单位为%
3. pack_voltage：电池模组电压，单位为V
4. charge_current：充电电流，单位为A
5. max_cell_voltage：电池单体最大电压，单位为V
6. min_cell_voltage：电池单体最小电压，单位为V
7. max_temperature：最高温度，单位为℃
8. min_temperature：最低温度，单位为℃
9. available_energy：可用能量，单位为kW
10. available_capacity：可用容量，单位为Ah

### Model 1: Random Forest

> Result 1
> 
> ![Image](./V1/RF_Epoch2.png)
>
> This is the 'Actual vs Predicted Health Status' with epoch 2

> Result 2
> 
> ![Image](./V1/RF_Epoch10.png)
>
> This is the 'Actual vs Predicted Health Status' with epoch 10

### Model 2: Neural Network

> ![Image](./V1/NN_Epoch20.png)

### Model 3: RNN

> ![Image](./V1/RNN_Epoch5.png)


## Version 2
