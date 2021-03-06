# 多旋翼飞行器设计与控制_学习笔记2

## 第一讲 绪论

人们为什么选择多旋翼飞行器？

这个问题涉及多旋翼飞行器的基本概念、操控和评价以及多旋翼技术发展历史。

### 1.基本概念

#### 1.1 常见飞行器分类

（1）固定翼

优点：续航时间最长，飞行效率最高，载荷最大；

缺点：必须要助跑，降落时候必须要滑行。

（2）直升机

优点：垂直起降；

缺点：续航时间没有优势，机械结构复杂，维护成本高。

（3）多旋翼

优点：垂直起降，机械结构简单，易维护；

缺点：载重和续航时间都更差；

一般受力特点：合成拉力垂直桨盘平面，拉力、重力。

四旋翼和六旋翼有何分别？无本质区别，3个力矩+拉力；六旋翼控制分配更灵活。

（4）复合飞行器

#### 1.2 无人驾驶飞机和航模

（1）无人驾驶飞机（Unmanned Aerial Vehicle）：

简称“无人机”，英文缩写为“UAV”,是利用无线电遥控设备和自备的程序控制装置操纵的不载人飞机。微小型无人机英文“Drone”。

（2）航模（Model Aircraft）：

在国际航联制定的竞赛规则里明确规定“航空模型是一种重于空气的，有尺寸限制的，带有或不带有发动机的，可遥控的不能载人的航空器。”

（3）半自主控制方式的多旋翼属于航模范畴，全自主控制的多旋翼属于无人机范畴。

### 2.多旋翼操控和评价

#### 2.1 四旋翼的操控

（1）悬停

当飞行器悬停时，拉力抵消重力；四个螺旋桨拉力产生的滚转、俯仰力矩为零；偏航力矩为零，四个螺旋桨反扭矩效应均被抵消。

ps. 多数直升机即单旋翼直升机都有一个小垂直尾桨来抵消反作用力矩，或者采用共轴双桨，上下两个螺旋桨转动方向相反，从而抵消之间的反扭矩的作用。

（2）升降运动

同时同量地增加四个螺旋桨的转速，则螺旋桨产生的总拉力增大，力矩和依然为零。拉力大于重力时，四旋翼就会上升。

（3）前后运动

同时同量地减少螺旋桨#1、#4的转速，同时同量增加螺旋桨#2、#3的转速，会引起四旋翼向前俯仰。然后，拉力会产生向前的分量。

可以看到，改变俯仰后，拉力的垂直分量会减小，将不再等于多旋翼的重力，因此需要增加拉力。

（4）左右运动

同时同量减小螺旋桨#1、#2的转速，同时同量增加#3、#4的转速，这将产生不平衡力矩使机身向右滚转倾斜。然后，拉力会产生向右的分量。

（5）偏航运动

同时同量减小螺旋桨#2、#4的转速，同时同量增加螺旋桨#1、#3的转速，这将使前后飞行和左右飞行的力矩为零。但顺时针偏航力矩增加了，飞机顺时针偏航。

#### 2.2 多旋翼的评价

（1）对比

多旋翼的易用性、可靠性和维护性很好。多旋翼飞行器运动相互解耦，无机械磨损，结构简单、模块化。也有缺点，多旋翼能量转换效率最低，所以与固定翼飞行器和直升机相比，多旋翼在飞行时间和承载性上没有优势。

（2）局限性（该方式不宜推广到大尺寸的多旋翼）

1）桨叶尺寸越大，越难迅速改变其角速度。

在这个假设下，我们最终得到，桨叶的角加速度与多旋翼的特征长度平方的倒数成正比，也就是多旋翼尺寸越大，角速度越小，即机动性低。

相比之下，直升机靠同时同量改变旋翼的攻角来增加或减少总拉力，从而实现爬升或下降。

2）在大载重下，桨叶上下挥舞会导致刚性大的桨很容易折断。

因此，多旋翼方式不宜推广到大尺寸，改进方式如Volocopter VC200。

总的来说，和相同尺寸的四旋翼相比，VC200在可靠性、维护性、续航性和承载性方面没有优势，它只是原尺寸飞机的一个折中。

### 3.多旋翼技术发展历史

#### 3.1 休眠期（1990以前）

早在1907年的法国，在查尔斯·里歇教授的指导下，布雷盖兄弟进行了他们的旋翼式直升机的飞行试验，这是记录的最早构型。因为涉及不切实际，只飞了1.5米，随后落下。

艾蒂安·奥秘西恩于1920年开始设计多旋翼设计，第一次试飞失败；经过重新设计之后，于1923年实现了起飞并创造了当时直升机领域的世界纪录；该直升机首次实现了14分钟的飞行时间。

1921年乔治·波札特在美国俄亥俄州西南部城市带领的美国空军部建造了另一架的大型的四旋翼直升机，这家四选一飞机除了飞行员外还能承载3个人，原本期望的飞行高度是100米，但最终只飞到5米的高度，主要原因是发动机性能不行。

1956年，马克·阿德曼·卡普兰设计的第一架真正的四旋翼飞行器。试飞取得巨大成功，这架飞机重达1吨，依靠两个90马力的发动机实现悬停和机动。

在20世纪50年代，美国陆军继续测试各种垂直起降方案。VZ-7虽然相对稳定，但是它未能达到军方对高度和速度的要求，该计划并没有得到更进一步的推行。在此之后的30年内，多旋翼飞行器没有取得太大的进展，获得的关注也非常少。

#### 3.2 复苏期（1990-2005）

（1）产品方面

随着四旋翼飞行器的概念逐渐偏离军事用途，它开始通过遥控玩具市场走进消费者。

（2）学术方面

几克重的MEMS惯导系统已经被研制出来。

学术界开始研究建模和控制。

2005年左右，真正稳定的多旋翼无人机自动控制器才被制作出来。

#### 3.3 发展期（2005-2010）

（1）产品方面

德国Microdrones GmbH公司与2005年成立，并于2006年4月推出第一代产品Md4-200，10年推出的Md4-1000四旋翼。美国某公司在2004年推出Draganflyer系列。这些产品在商业市场取得了巨大成功。可以说，德国在这个阶段起到了主导作用。

（2）学术方面

越来越多的学术研究人员开始研究多旋翼，自己搭建四旋翼，验证算法，特别是姿态控制算法。

个别研究者基于商业四旋翼+捕捉系统开发验证环境。

#### 3.4 活跃期（2010-2013）

（1）产品方面

2010年，法国的派诺特公司与学校共同合作，经过6年努力，推出消费级的AR.Drone四旋翼玩具，非常成功，它的技术和理念也十分领先。

2013年左右，大疆推出小精灵Phantom一体机。

（2）学术方面

2012年2月，宾夕法尼亚大学的韦杰·库玛教授在TED上做出了四旋翼飞行器发展历史上里程碑式的演讲，展示了四旋翼的灵活性以及编队协作。

多旋翼开源自驾仪增多。

#### 3.5 爆发期（2013-）

（1）产品方面

大疆小精灵一体机得到持续关注。

连载主编C.Anderson于2012年年底当任3D Robotics公司的CEO，连续推出Iris、X8+、Solo等四旋翼飞行器。同时，该公司维护和支持了APM开源多旋翼的软硬件升级，以及网站建设和维护。

2013年底，3D Robotics公司牵手苏黎世联邦理工学院的PX4开源飞控开发团队，共同推出Pixhawk硬件。

同样在2013年底，互联网巨头亚马逊发布的采用四旋翼送快递的视频，拉近了多旋翼飞行器与普通消费者之间的距离。

（2）学术方面

多旋翼的研究更偏向智能化、群体化。

2013年，苏黎世联邦理工学院的拉斐尔·安德烈教授在TEDGlobal的机器人实验室展示了四选一的惊人运动机能。

《自然》发表综述文章分析和展望了小型自主无人机在民用领域的科学和技术。

#### 3.6 小结

（1）时势造英雄，多旋翼是时间的产物。

硬件小型化、计算能力越来越强、电机功率提升、电池能量密度提升、智能手机、Gopro运动相机、活跃的社交网络。

（2）一体机改变了体验，使飞行简单化。

AR.Drone、大疆小精灵Phantom。

### 4.本门科的安排

#### 4.1 目的

本门课程讲授多旋翼设计、动态模型建立、状态估计、控制和决策等方面的基础知识。具有两大特点：“基础性”和“系统性”。

（1）基础性

本课程力求绝大部分多旋翼涉及的内容能够自包含，使得具有自动化专业本科知识的学生就能够听懂这门课。

（2）系统性

本课程目的是介绍多旋翼飞行器系统性的全貌，而不仅仅是某一个技术点。本课程通过多旋翼例子，将散落的知识实例化。

#### 4.2 结构

（1）仅对多旋翼设计感兴趣的同学，可参加第一讲、设计单元和第十五讲课程；

（2）仅对多旋翼感知感兴趣的同学，可参加第一讲、模型单元、感知单元和第十五讲课程；

（3）仅对多旋翼控制算法感兴趣的同学，可参加第一讲、模型单元、控制单元和第十五讲课程。

