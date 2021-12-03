# Paper_Read

---

## Mask2Former

Mask2 Former来了!
用于通用图像分割的 Masked-attention Mask Transforme 本文提出一种用于任何图像分割任务的网络 Mask2 Former,在语义/实例/全景分割上表现 SOTA!如ADE20K上高达57、7mloU!目前排名 第一!代码于3小时前开源!单位:FAIR,UIUC 图像分割是关于对具有不同语义的像素进行分组 例如类别或实例 membership,其中每个语义选择 定义了ー个任务。虽然只有每项任务的语义不 同,但当前的研究重点是为每项任务设计专门的架 构。我们提出了 Masked- attention Mask ansformer(Mask2 Former),这是一种能够解決 任何图像分割任务(全景、实例或语义)的新架 构。它的关键组成部分包括 masked注意力,它通 过将交叉注意力限制在预测的掩码区域内来提取局 部特征。除了将研究工作減少至少三倍之外,它 在四个流行数据集上的表现也明显优于最好的专业 架构。最值得注意的是,Mask2 -ormer为全景分 割(COCO上的57.8PQ)、实例分割(COCO 的50.1AP)和语义分割(ADE20K上的57.7 mloU)设置了新的最新技术。 

关键词：`#Transformer`；`#BERT`；`#大规模预训练`

主页：https://bowenc0221.github.io/mask2former/
代码：https://github.com/facebookresearch/Mask2Former
论文：https://arxiv.org/abs/2112.01527

----

## Sparse-RS

AAAI2022 Sparse-RS:用于查询高效稀硫黑盒 对抗攻击的通用框架 本文提出了一个通用框架: Sparse-RS,提出了 sore- based黑盒条件下的稀疏攻击(10-RS)、对 抗图块( Patch-RS)和对抗框( Frame-RS),代 码已开源!单位:图宾根大学,EPFL

与12和1∞攻击相比，稀疏对抗性扰动在文献中受 到的关注要少得多。然而，准确评估模型对稀疏扰动的鲁棒性同样重要。受此目标的启发，我们提出 了一个基于随机搜索的通用框架 Sparse-RS，用于黑盒设置中基于分数的稀疏目标和非目标攻击。 Sparse-RS不依赖于替代模型，并为多个稀疏攻击模型实现了最先进的成功率和查询效率:10有界抗动、对抗补丁和对抗框架。与现有方法不同,无目标 Sparse-RS的I0版本通过仅抗动总像素数的 0.1%，在 Imagenet上实现了几乎100%的成功率，优于包括10-PGD在内的所有现有白盒攻击。 此外，即使对于20×20对抗性补丁和224×24图 像的2像素宽对抗性帧的挑战性设置，我们的非目标稀疏RS也实现了非常高的成功率。最后,我们表明 Sparse-RS可以应用于universal adversaria patches，它显著优于基于 transferl的方法。

《Sparse-rs: a versatile framework for query efficient sparse black-box adversarial attacks》

关键字：#对抗攻击；#AAAI2022
代码：https://github.com/fra31/sparse-rs
论文：https://arxiv.org/abs/2006.12834

---

