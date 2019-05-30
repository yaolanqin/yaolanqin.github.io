---
layout:     post
title:      The Inception Family-Going Deeper
subtitle:   Building a deep neural network from Inception
date:       2019-05-30
author:     yaodong cui
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - Deep learning
    - Image Processing
    - Inception
    - Batch Normalization
---


## Background

In 2014, a team in Google proposed a convolutional neural network architecture, called GoogLeNet or  [Inception](https://arxiv.org/abs/1409.4842) , which increase the depth and width of the network while maintaining the computational expense. 


##  The Inception Family

### Inception V1：Go Deeper

The network achieves this with several techniques including 1 X  1 convolution, Inception modules and global average pooling. 

The 1 X 1 convolution is used to reduce computation bottleneck by dimension reduction. The Inception modules, as shown in Fig.1, concatenates the results 1 X 1 Convolution, 3 X 3 Convolution,5 X 5 Convolution and X 3 max pooling, while using 1 X 1 Convolution for dimensionality reduction.
Instead of the fully connected layers, the global average pooling is used at the end of the network to reduce the number of weights.


<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="https://raw.githubusercontent.com/yaodongC/yaodongC.github.io/master/img/InceptionV101.png"
    width = "300" height = "300">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">Fig.1  Inception module with 1 X 1 Convolution</div>
</center>


The GoogLeNet also employs auxiliary classifier during the training process. Therefore, the total loss function is a weighted sum of the final loss and auxiliary loss. This methodology can prevent vanishing gradient problem and provide regularization. 



### 





###




```js
<!-- Gitalk 评论 start  -->
{% if site.gitalk.enable %}
<!-- Link Gitalk 的支持文件  -->
<link rel="stylesheet" href="https://unpkg.com/gitalk/dist/gitalk.css">
<script src="https://unpkg.com/gitalk@latest/dist/gitalk.min.js"></script>

<div id="gitalk-container"></div>
    <script type="text/javascript">
    var gitalk = new Gitalk({

    // gitalk的主要参数
		clientID: `Github Application clientID`,
		clientSecret: `Github Application clientSecret`,
		repo: `存储你评论 issue 的 Github 仓库名`,
		owner: 'Github 用户名',
		admin: ['Github 用户名'],
		id: '页面的唯一标识，gitalk会根据这个标识自动创建的issue的标签',
    
    });
    gitalk.render('gitalk-container');
</script>
{% endif %}
<!-- Gitalk end -->
```



# Conclusion

