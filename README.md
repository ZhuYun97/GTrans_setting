# GTrans

## 环境配置

### 配置GCC
**For cuda10.2**
注：该方法只适用cuda10.2版本的服务器
1. 创建虚拟环境: `conda create -n gcc python=3.7`
2. 激活虚拟环境: `conda activate gcc`
3. 配置dgl(0.5 > DGL ≥ 0.4.3): `conda install -c dglteam dgl-cuda10.2==0.4.3post2` 该命令安装的是cuda10.2 py3.7 dgl-0.4.3，其他版本请查询https://conda.anaconda.org/dglteam/linux-64
4. 安装torch: `pip install torch==1.5.1 torchvision==0.6.1`

5. clone gcc: `git clone https://github.com/THUDM/GCC.git`
6. 额外配置gcc所需环境: `pip install -r requirements.txt`
7. 安装RDKit: `conda install -c conda-forge rdkit=2019.09.2` (解析时间可能会比较久，请耐心等待)
<!-- 8. 安装一些额外所需的库`pip install joblib` 和 `pip install tensorboard` -->

**For cuda>11.0**
如果你的服务器cuda版本高于11，配置环境则会麻烦一些，因为dgl适配的版本只有>=0.5.3
1. 创建虚拟环境: `conda create -n gcc python=3.7`
2. 激活虚拟环境: `conda activate gcc`
3. 在conda虚拟环境中安装cuda和cudnn: `conda install cudatoolkit=10.2 -c https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/linux-64/` 和 `conda install cudnn`
4. 配置dgl: `conda install -c dglteam dgl-cuda10.2==0.4.3post2`
5. 安装torch: `pip install torch==1.5.1 torchvision==0.6.1`

6. clone gcc: `git clone https://github.com/THUDM/GCC.git`
7. 额外配置gcc所需环境: `pip install -r requirements.txt`
8. 安装RDKit: `conda install -c conda-forge rdkit=2019.09.2` (解析时间可能会比较久，请耐心等待)
<!-- 9. 安装一些额外所需的库`pip install joblib` 和 `pip install tensorboard` -->
这个时候运行程序会出现"ModuleNotFoundError: No module named 'dgl.nodeflow'".
解决办法参考https://github.com/dmlc/dgl/issues/3083

## 工具
GitHub代理：https://ghproxy.com/ ，如果clone项目时间过久可以使用该代理。使用方法git clone https://ghproxy.com/XXX

## 参考
- https://zhuanlan.zhihu.com/p/367740437
- https://github.com/dmlc/dgl/issues/3083
