# GTrans

## 环境配置

### 配置GCC
1. 创建虚拟环境: `conda create -n gcc python=3.7`
2. 激活虚拟环境: `conda activate gcc`
3. 配置dgl(0.5 > DGL ≥ 0.4.3): `conda install -c dglteam dgl-cuda10.2` 该命令安装的是cuda10.2 py3.7 dgl-0.4.3，其他版本请查询https://conda.anaconda.org/dglteam/linux-64
4. 安装torch: 'pip install torch==1.5.1 torchvision==0.6.1'

5. clone gcc: `git clone https://github.com/THUDM/GCC.git`
6. 额外配置gcc所需环境: `pip install -r requirements.txt`
7. 安装RDKit: `conda install -c conda-forge rdkit=2019.09.2`

