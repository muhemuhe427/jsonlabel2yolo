# jsonlabel2yolo
a tool for transferring the json label of cityscapes to a trainable labels for yolov5



由于yolov5分割工具箱仅提供coco128-segment数据集为示例，其标签数据为txt，不同于传统的语义分割标签。以cityscapes数据集为例，如图所示，提供了标注的像素点位置，
需要根据长宽将其归一化成0-1之间的数
![image](https://user-images.githubusercontent.com/79949048/203745676-45426f51-77c4-4a14-9fdd-6be938d27071.png)
最后的标签效果如图所示，第一个元素为0 表示标注的类ID，再依次按照x,y的顺序排列标注像素点归一化后的值。
![image](https://user-images.githubusercontent.com/79949048/203746272-82c161d5-79c0-438e-bdc4-1d9ac6488aa7.png)
最后验证的效果能够正常训练，如下图所示：

![94ff0d9552098e2e435328048c2699b](https://user-images.githubusercontent.com/79949048/203746844-10a18966-8274-4ef4-8232-a143edc4e7bc.png)
由于目前还没有转换训练集的标签数据，只转换了训练集，所以验证部分指标为0，等到转换完成时再来补充
