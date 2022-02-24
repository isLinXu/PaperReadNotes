# Paper_Read

---

## PreViTS：

哥大提出 Previos：具有视频跟踪监督的对比预训练 
本文提出使用视频跟踪监督( Previos)进行预训练，以利用无监督的目标跟踪从视频中学习视觉表示，可以产生更准确和更强大的视觉特征表示，单位：哥伦比亚大学，Salesforce研究院。

由于存在对象的自然时间变换，视频是视觉表示的自监督学习(SSL)的丰富来源。然而，当前的方法通常随机采样视频剪辑以进行学习,这会导致监控信号不佳。在这项工作中,我们提出了 PreViTS，这是一种SSL框架，它利用无监督跟踪信号来选择包含相同对象的剪辑，这有助于更好地利用对象的时间变换。

PreViTS进一步使用跟踪信号在空间上约束帧区域以通过对Grad-CAM注意力图提供监督来学习和训练模型以定位有意义的对象。为 了评估我们的方法，我们使用 PreViTS在VGG-Sound和 Kinetics-400数据集上训练动量对比 (MoCo)编码器。在图像识别和视频分类下游任务vios使用 Previos进行的训练优于MoCo单独学 习的表示，从而在动作分类方面获得了最先进的性能。 Previos有助vios于学习对背景和上下文变化更 稳健的特征表 在背景变化的图像和视频数据集上的实验所见。使用 Previos从大规模未经策划的视频中学习可以产生更准确和更强大的视觉特征表示。 

《Previts: Contrastive Pretraining with Video acking supervision 》

论文：https://arxiv.org/abs/2112.00804

---

## VST

场景文本识别的视觉语义Transformer本文提出了视觉语义 Transformer来解决场景文本识别问题，其中设计了视觉-语义对齐模块，表现 SOTA!性能优于 ABINET、PREN等网络,单位：平安财产保险 

建模语义信息有助于场景文本识别。在这项工作 中，我们提出与视觉语义 Transformer(VST)联合建模语义和视觉信息。VST首先使用 stormer模块和主要视觉语义对齐模块从视觉 特征图中显式地提取主要语义信息。然后将语义信息与视觉特征图(视为序列)结合，形成一个结合视觉和语义信息的伪多域序列,随后将其输入到基于Transformer的交互模块中，以便学习视觉和语义之间的交互语义特征。

通过这种方式，可以通过语义信息增强视觉特征，反之亦然。视觉特征的增强版本由二级视觉语义对齐模块进一步解码，该模块与主要模块共享权重。最后，解码的视觉特征和增强的语义特征由第三个Transformer模块联合 处理，获得最终的文本预测。在包括常规/不规则文本识别数据集在内的七个公共基准上的实验验证了我们提出的模型的有效性，在七个基准中的四个基准上达到了最先进的水平。

关键字：#Transformer; #场景文本识别；#OCR; @AAAI2022

论文：https://arxiv.org/abs/2112.00948

---

## Swin Track

屠榜目标跟踪! Swin Track: Transformer跟踪的简单而强大的基线 
本文为 Transformer跟踪器提出了一个强大的基线 Swin Track，其由Swin骨干、一个基于串联的融合编码器、一个通用位置编码解决方案组成，并结合 了一些流行的训练技巧，霸榜多个目标跟踪数据集 (如LaSOT、 TrackingNet等)，优于 STARK等网 络，代码刚开源! 单位:南方科技大学，鹏城实验室等。

Transformer最近在改进视觉跟踪算法方面表现出了明显的潜力。尽管如此,现有的基于变换器的跟踪器大多使用变换器来融合和增强卷积神经网络CNN)生成的特征。相比之下，在本文中，我们提出了一种完全基于注意力的 Transformer跟踪算法， Swin-transformer Tracker(Swin Track) SwinTrack使用Transformer进行特征提取和特征 融合，允许目标对象和搜索区域之间进行完全交互以进行跟踪。为了进一步提高性能，我们全面研究了特征融合、位置编码和训练损失的不同策略。所有这些努力使 SwinTrack成为一个简单而可靠的基线。在我们彻底的实验中，SwinTrack在LaSOT上以0.717SUC创造了新记录，在仍以45FPS 运行的情況下，超过 STARK4.6%。此外，它在其他具有挑战性的LaSOText、TrackingNet和GOT-10k上实现了0.483SUC、0.832SUC和 0.694AO的最先进性能。 

 (Swintrack: A Simple and Strong Baseline for ranstormer I racking )

关键词：#目标跟踪；#Transformer；

代码：https://github.com/LitingLin/SwinTrack

论文：https://arxiv.org/abs/2112.00995

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

## OW-DETR

OW-DETR:开放世界检测Transformer 
本文针对开放世界目标检测问题提出了一种新的基于Transformer的方法: OWDETR，表现SOTA性能优于ORE等网络,代码将开源! 单位:IIAI,谷歌,ANU, MBZUA等 

开放世界目标检测(OWOD)是一个具有挑战性的计算机视觉问题，其任务是检测一组已知的对象类别，同时识别未知对象。此外，模型必须逐步学习在下一个训练集中已知的新类。与标准目标检测不同，OWOD设置对在澘在未知对象上生成高质量候选 proposals、将未知对象与背景分离以及检测各种未知对象提出了重大挑战。

在这里,我们介绍 了一种新颖的基于端到端Transformer的框架OWDETR，用于开放世界目标检测。
提出的OW- DETR包括三个专用组件，即注意力驱动的伪标签、新颖性分类和客观性评分，以明确解决上述 OWOD挑战。我们的OW-DETR显式编码多尺度上下文信息，具有较少的归纳偏差，能够将知识从已知类转移到未知类，并且可以更好地区分未知对象和背景。综合实验在两个基准上进行：MS COCO和 PASCAL VOC。
广泛的消融揭示了我提出的贡献的优点。此外,我们的模型优于最近引入的OWOD方法ORE，在MS-COCO基准上的未知召回率方面，绝对收益从1.8%到3.3%不等。在增量目标检測的情況下，OW-DETR在 PASCAL VOC基准测试中的所有设置都优于最新技术。我们的代码和模型将公开发布。 

《OW-DETR: Open-world Detection Transformer》  

关键词：#Transformer; #Open-Set; #目标检测

论文：https://arxiv.org/abs/2112.01513

---

## RPG

#AAA1 2022 RPG:用于医学语义分割的参考引导伪标签生成 
本文提出了一种用于半监督医学语义分割生成分割监督的新方法，可以轻松插入现有分割框架中，即使标记图像减少95%，也能保持与全监督模型相同的性能，单位:卡尔斯鲁厄理工学院,埃森大学医学院 

生成密集注释的数据对于医学成像应用来说是一项艰巨而乏味的任务。为了解決这个问题，我们提出 了一种新的方法来为半监督语义分割生成监督。我们认为标记和未标记图像之间视觉上相似的区域可能包含相同的语义,因此应该共享它们的标签。遵循这一想法，我们使用少量标记图像作为参考材料，并将未标记图像中的像素与参考集中最佳拟合像素的语义进行匹配。这样，我们避免了诸如确认偏差之类的陷阱，这在纯粹基于预測的伪标记中很常见。由于我们的方法不需要任何架构更改或伴随的网络，因此可以轻松地将其插入现有框架中。我在X射线解剖学分割方面实现了与标准全监督模 型相同的性能，尽管标记图像减少了95%。除了对我们提出的方法的不同方面进行深入分析之外，我们通过将我们的方法与具有竞争性能的现有视网膜液分割方法进行比较，进一步证明了我们的参考指导学习范式的有效性，因为我们在最近的工作基础上进行了改进15%的平均loU。

 《reference-guided Pseudo-label Generation for Medical Semantic Segmentation)》

关键词：#医学图像分割；#半监督语义分割；#AAAI2022

论文：https://arxiv.org/abs/2112.00735

---

## FAIR

FAIR提出:用于分类和检测的改进多尺度视觉 ansforme MVT官方升级!在图像分类、目标检测和视频识別上表现SOTA!如ImageNet准确率为88.8% COCO AP为56.1, Kinetics-400视频分类准确率为 86.1%,代码将开源!单位:FAIR,UC伯克利 

MViT官方升级!在图像分类、目标检测和视频识別上表现SOTA!如ImageNet准确率为88.8% COCO AP为56.1,，Kinetics-400视频分类准确率为86.19%，代码将开源!单位:FAIR,UC伯克利 

在本文中，我们研究了多尺度视觉 Transformel (MViT)作为图像和视频分类以及目标检测的统一架构。我们提出了MVT的改进版本，它结合了分解的相对位置嵌入和残差池连接。我们将这种架构实例化为五种尺寸，并针对 Image Net分类 COCO检測和 Kinetics视频识别对其进行评估在这些方面它优于先前的工作。

我们进一步将 MViT的集中注意力与窗口注意力机制进行了比较，它在准确性计算方面优于后者。

没有花里胡哨，MViT在3个领域拥有最先进的性能Imagenet分类准确率为88.8%，COCO目标检测准确率为56.1，以及 Kinetics-400视频分类准确率为86.1%。代码和模型将公开提供。 

《Improved Multiscale Vision Transformers for Classification and Detection 》

关键词：#目标检测；#行为识别；#视频理解

论文：https://arxiv.org/abs/2112.01526

---

## SVT

SVT:自监督视频 Transforme 本文提出了一种新的视频 Transformer自监督训练 机制,利用跨空间和时间的不同视野(全局和局 部)之间的时空对应关系,表现SOTA!性能优于 CORP等网络,代码将开源!单位:石溪大学 ANU, MBZUALS等 

在本文中，我们提出了使用未标记视频数据对视频Transformeri进行自监督训练。从给定的视频中，我们创建具有不同空间大小和帧速率的局部和全局时空视图。我们的自监督目标试图匹配代表同视频的这些不同视图的特征，以保持动作的时空变化不变。据我们所知，所提出的方法是第一个减轻自监督视频Transformer(SVT)中对负样本或专用存储库的依赖的方法。此外，由于Transformer模型的灵活性，SVT支持使用动态调整位置编码的单一架构内的慢速视频处理，并支持沿时空维度的长期关系建模。我们的方法在四个动作识别基准 ( Kinetics-400、UCF-101、HMDB-51和SSv2) 表现良好，并且在小批量下收敛速度更快。 

关键词：#自监督Transformer; #视频Transformer; #Transformer

代码：https://github.com/kahnchana/svt

论文：https://arxiv.org/abs/2112.01527

---

