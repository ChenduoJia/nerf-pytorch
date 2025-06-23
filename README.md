本项目参考自https://github.com/yenchenlin/nerf-pytorch 的源码

文件结构应如下所示
nerf-pytorch/
	└── data/
 		└── my_scene/
   		├── transforms.json
     		├──poses_bounds.npy
       		└── images/
	 其中poses_bounds.npy和transforms.json需要调用colmap和colmap2nerf.py生成
  
运行训练的指令为python run_nerf.py --config configs/my_scene.txt
可以在configs/my_scene.txt中设置训练参数，训练步长的设置需要在run_nerf.py的train()函数中修改N_iters的值
结果会输出在logs文件夹中
