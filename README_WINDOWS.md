# Windows + VS Code下使用

## Python 安装

1. 官网下载 [python3.10.6 installer](https://www.python.org/downloads/windows/)  
2. **安装：需在弹出的安装窗口勾选 Add Python to PATH！！！**  

## VS Code 下创建虚拟环境

1. Ctrl+Shift+P -> 选择解释器 -> 创建虚拟环境 -> 快速创建使用 venv
2. 这会在当前工作区目录去下创建 .venv 目录
3. 重新选择解释器，选择刚才创建的虚拟环境 venv

## Powershell下环境激活和使用  

1. 激活环境

在 Powershell终端下执行，激活后应该看到终端变为(.venv)开头  

```Shell
# 设置ps1脚本运行权限
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
# 激活环境
[path_to_venv]\Scripts\Activate.ps1
# 例如：
# & d:\WJH\Documents\reinforcement-learning\.venv\Scripts\Activate.ps1
```

2. 检查 Python 是否安装成功

```Shell
python --version
```

3. 安装必须的 python pkg

```Shell
python -m pip install numpy scipy matplotlib tqdm ipython jupyterlab ipykernel pandas
python -m pip install gym==0.21.0
pip install pyglet==1.5.27
pip install "scikit-learn<1.4"
```