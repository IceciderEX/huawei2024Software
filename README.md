# 2024华为软件精英挑战赛main.cpp

货物用set存储，初始的left_time置为1000，每过1帧将left_time减1，当left_time为0时将该货物从set中删除

机器人的goods若等于0，去找货物，若等于1，去找货船
机器人应该向哪个货物进发？：价值/时间,优先向该权重最高的货物出发，进行搬运，其中距离使用最短路算法进行计算，储存路径，然后进行输出。不能向墙或者大海移动（若有其他机器人已经锁定该货物，根据权重确定该机器人是否搬运该货物int weight（试用方案1））,每一帧重新计算最短路，判断要走的方向上有没有机器人和墙和海
若status参数等于，不对机器人下任何指令，若等于1，正常运行
机器人卸货时优先往左上卸货

轮船初始都在虚拟点，第一帧的轮船位置无效，第一帧的机器人位置是初始位置
货船装满出发
优先去所花时间较少的泊位，并且优先去没有货船的泊位
