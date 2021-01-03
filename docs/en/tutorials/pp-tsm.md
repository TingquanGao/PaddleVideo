PP-TSM：An Effective and Efficient video-recognition model   

PP-TSM is an optimized model based on TSM in PaddleVideo,   
whose performance (top-1 on UCF101 and Kinetics400) and inference spped   
are better than TSM paper(https://arxiv.org/abs/1811.08383 ) and   
other open source TSM，PaddlePaddle2.0(available on pip now) or   
Daily Version( https://www.paddlepaddle.org.cn/documentation/docs/zh/install/Tables.html#whl-dev )   
is required to run PP-TSM.    

When only use ImageNet for pretrain and only use 8X1 sample，  
PP-TSM’s top1 reached to 89.5% and 73.5% on UCF101 and Kinetics400,   
and inference speed of FP32 on single V100 is DOING,   
inference speed of FP16 with TensorRT on single V100 isTODO.  

As far as we know, under the same conditions,    
top1=73.5% on Kinetics400 is the best performance for 2D video model until now.  


PP-TSM improved performance and speed of TSM with following methods:   
1、Model Tweaks: ResNet50vd  
2、ImageNet pretrain weights based on Knowledge Distillation  
3、beter batch size  
4、beter L2  
5、label_smoothing  
6、beter lr decay  
7、Data augmentation  
8、beter epoch num  
9、bn strategy  
10、integrated PaddleInference  
11、more strategies todo: Knowledge Distillation、optimizer and so on.  