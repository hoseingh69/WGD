# WGD
Gradient
Optimizers are key components of deep neural networks that perform weight updates. In this paper, we introduce a new updating method for optimizers based on gradient descent, called whitened gradient descent (WGD). This method is easy to implement and can be used in every optimizer that is based on the gradient descent algorithm. Despite the addition of WGD mathematical calculations to the learning algorithm, the learning time does not change. This method smooths the training curve and improves classification metrics. To evaluate the proposed algorithm, we performed 48 different tests on two datasets, Cifar100 and Animals-10, using three network structures including densenet121, resnet18, and resnet50. The experiments show that using the WGD method in gradient descent based optimizers, improves the classification results significantly. For example, integrating WGD in RAdam optimizer increased the accuracy of DenseNet from 87.69% to 90.02% on the Animals-10 dataset.  

To use this method, it is enough to use the above optimizers when calling the optimizer.
For example:


optimizer = WGD_SGD(model.parameters(), lr 0.02, momentum=0.9,weight_decay = 0.0005)
