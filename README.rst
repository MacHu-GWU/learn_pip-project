pip Cheet Sheet
===============


安装pip本身
----------
1. `下载 <https://bootstrap.pypa.io/get-pip.py>`_ ``get-pip.py`` 文件。
2. 在命令行运行 ``python get-pip.py``, 为你指定的Python版本安装。 比如为python3安装该pip, 则需要将命令改为 ``python3 get-pip.py``。 若是MacOS系统中, 则需要使用超级用户权限 ``sudo python get-pip.py``。 若是Linux系统, 同样也需要超级用户权限。 最后, Ubuntu系统自带Python27/Python34和pip2/pip3。


检查pip是否成功安装了
------------------
在命令行输入 ``pip`` 看是否返回了菜单信息。 如没有返回, 很可能你需要手动将pip的安装路径添加到环境变量(通常只有Windows下的Python27以下的版本会需要这么做)。 

有3个命令都可以运行pip, 他们分别是:

- ``pip``: 若你的电脑上只安装了1个Python, 或你是运行在virtualenv环境下, 可以使用这个命令以默认的Python版本运行。
- ``pip2``/``pip3``: 若你的电脑为Python2/Python3各安装了一个大版本, 则可以使用这个命令以你需要的Python版本运行。
- ``pip2.7``/``pip3.4``: 若你的电脑安装了多个Python版本, 则可以使用这个命令以你需要的Python版本运行。


使用pip安装扩展包
---------------
常用的安装模式大约有以下几种 (我们以著名的 `requests <https://github.com/kennethreitz/requests>`_ 为例):

- PyPI在线下载安装: ``pip install requests``
- 从源码包安装: ``pip install requests-2.10.0.tar.gz``, ``pip install requests-2.10.0.zip``
- 从Wheel安装: ``pip install requests-2.10.0-py2.py3-none-any.whl``
- 从项目目录安装, 要确保当前目录下有 ``setup.py`` 文件: ``pip install .``
- 从GitHub远程安装(不推荐, 因为GitHub上的代码可能并不是发布版本状态, 可能是处于Dev状态下), 需要安装 `git <https://git-scm.com/>`_: ``pip install git+https://github.com/kennethreitz/requests.git``

一些特殊的安装方式:

- 安装指定版本, 若以安装了其他版本, 则会删除已安装版本: ``pip install requests==2.10.0``
- 更新至最新版本: ``pip install --upgrade requests``
- 安装 ``requirements.txt`` 文件中的扩展包: ``pip install -r requirements.txt``
- 更新pip本身至最新版本: ``pip install --upgrade pip``


使用pip删除扩展包
---------------
``pip uninstall requests``


pip的其他常用命令
---------------
- 列出所有已安装的扩展包: ``pip list``
- 将所有已安装的扩展包输出至requirements文件中: ``pip freeze > requirements.txt``
- 列出某个扩展包的详细信息: ``pip show requests``
- 使用全文搜索搜索包名和description: ``pip search requests``


附录
----
- `pip官方文档 <https://pip.pypa.io/en/stable/>`_