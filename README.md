# --- 该项目为2019年全国研究生数学建模大赛D题的代码实现 --- 请勿用于商业用途 转载请注明出处 --- 

基于主成分分析与聚类的车辆工况建模

详细代码和数据请进D文件夹

1. D_data2 对原始数据做了处理，对时间序列做了补全，采用线性插值法对各特征缺失值进行了填充，对时间序列数据按特征进行了切割，以时间序列内的车辆运动学片段特征关系，识别出运动学片段并切割。

2. D_data4 对各运动学片段内的数据计算该片段内的各项运动学特征，构建运动学特征数据集，对特征做主成分分析，并通过聚类算法对车辆运动学片段进行分类并获取各片段距聚类中心的距离。

3. D_data5 通过聚类结果，选取各类别距聚类中心较近的运动学片段各十个（较近说明差别较大），对进行运动学合成，随机不重复选取这三十个运动学片段合成出总时间在1200-1300s的新片段作为能体现该车运动学规律的工况片段。

4. D_data6 对测试数据进行运动学片段提取，与获取的车辆工况进行拟合，误差分析以及评价。
