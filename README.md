# IW04

> @StuID：181840211
>
> @Author：汤远航

## 实现思路

1. CoreM L实现模型的训练, 作业 1 可以直接使用给定的数据集, 作业 2 则需要对数据集进行简单的修改。使用其中的水果和蔬菜等食品共 10 种作为 healthy 样本, 其他的食品共 10 种作为 unhealthy 样本. 修改通过Python代码实现, 写于 `dir_tools.ipynb` 中
2. ViewController 中, 使用 Dispatch.global 将模型的预测至于后台进行, 通过 Dispatch.main 实现前台label的更新
3. 通过 UIimage.cgImage 获得合适的模型输入图像格式
4. OOD检测通过MSP方法实现, softmax最大预测信度超过 0.8 的样本进行预测, 小于 0.8 的样本返回 “我不确定”

## 结果

1. 在 IOS15 的 Iphone6s 上进行了测试, 模型预测较慢, 往往需要图片显示后才显示预测结果, 这印证了将其至于后台处理的优势
2. MSP方法表现在作业 1 上良好, 但是在作业 2 上表现不佳
