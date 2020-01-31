## IDA插件安装
- 咱只有`IDA7.0`, 只能用`Python2`, 而且时64位
- 可移植版在安装`pip`包时会有诸多问题, 所以要用安装版

## 内容更新
- `git submodule init`
- `git submodule foreach git pull/checkout master???`

## Sark
- Python 3 & IDA 7.4: `pip3 install -U git+https://github.com/tmr232/Sark.git#egg=Sark`
- Python 2 & IDA < 7.4: `pip2 install -U git+https://github.com/tmr232/Sark.git@IDA-6.x#egg=Sark`
- 将`plugin_loader.py`放到IDA的插件目录
- 创建文件`plugins.list`, 并在其中按行写入`IDAPython`脚本的绝对路径
    - 系统范围: `%IDA%\cfg\plugins.list`
    - 用户范围:
        - Linux: `$HOME/.idapro/plugins.list`
        - Windows: `%idaapi.get_user_idadir()%\plugins.list`
- 示例
```
C:\Plugins\my_plugin.py
# This is a comment. Comments are whole lines.
C:\OtherPlugins\another_plugin.py
```

# py

## flare-ida
- 修改环境变量: `PYTHONPATH`, 添加值`flare-ida\python`(绝对路径)
- 安装`vivisect`: `pip2 install vivisect`
- `plugins`: 插件
- `decompiler_scripts/MSDN_crawler/shellcode_hashes`: 脚本

## ida
- `install.py`功能是拷贝和移除
- `modules/plugins`: 插件
- `scripts`: 脚本
