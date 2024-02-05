# Python依赖管理及打包利器：Poetry

## **简介**

Poetry 是一个包管理和打包的工具。 在 Python 中，对于初学者来说，打包系统和依赖管理是非常复杂和难懂的。即使对于经验丰富的开发者，一个项目总是要同时创建多个文件： `setup.py` ,`requirements.txt`,`setup.cfg` , `MANIFEST.in` ，还有最新的 `Pipfile`，十分繁琐。因此， poetry 将所有的配置都放置在一个 toml 文件（`pyproject.toml`）中，这些配置包括：依赖管理、构建、打包、发布。

Poetry 的灵感来自于其他语言的一些工具： composer(PHP) 和 cargo (Rust) 。

## **安装**

### **使用在线脚本进行安装（推荐）**

```
curl -sSL <https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py> | python

```

### **其他的安装方法（不推荐）**

**pip安装**

```
pip install --user poetry

```

pip这种安装方式可能引起依赖包冲突。还可以考虑使用pipx（3.6及之后的版本）或者pipsi（3.6之前的版本）

安装后可以使用下面的命令确认安装成功：

```
poetry --version

```

### **更新Poetry版本**

更新到最新版本

> poetry self update

更新到预发布版本

> poetry self update --preview

更新到指定版本

> poetry self update 0.8.0
> 
> **注意：**
> 
> ```
> self update
> ```

## **常用命令汇总**

poetry 提供了一系列覆盖整个开发流程的命令，这些命令使用简单，如表所示：

## **项目初始化**

### **新建项目**

```
poetry new demo-project

```

新建项目的目录结构如下：

```
tree demo-project

demo-project
├── README.rst
├── poetry.lock
├── pyproject.toml
├── demo_project
│   └── __init__.py
└── tests
    ├── __init__.py
    └── test_demo_project.py

3 directories, 6 files
```

同时，项目下会自动生成pyproject.toml文件，该文件的主要用途是依赖管理、构建、打包、发布，内容如下：

```
[tool.poetry]
name = "demo-project"
version = "0.1.0"
description = ""
authors = ["吃果冻不吐果冻皮 <liguodongiot@163.com>"]

[tool.poetry.dependencies]
python = "^3.9"

[tool.poetry.dev-dependencies]
pytest = "^5.2"

[build-system]
requires = ["poetry-core>=1.0.0"]
build-backend = "poetry.core.masonry.api"
```

配置说明：

**[tool.poetry.dependencies]** ：在这里您可以列出项目需要的所有依赖包。 就像旧 `requirements.txt` 文件一样。 您可以手动完成此操作，然后调用命令 `poetry install` 以将其全部安装以用于软件包开发和工作目的。 如果您使用 `poetry add <dependency_name>`安装依赖包 相当于使用 `pip install <dependency_name>` 。

**[tool.poetry.dev-dependencies]** ：配置仅用于开发的依赖包。

> 备注：

### **已有项目初始化**

```
poetry init

```

根据它的提示输入你的项目信息，不确定的内容就按下 Enter 使用默认值，后续也可以手动更新。

## **虚拟环境管理**

### **创建虚拟环境**

**方式一：**

利用 `virtualenvs.create=true` 自动创建虚拟环境

当参数 **virtualenvs.create=true** (默认)时，执行 **poetry install/add/remove** 时会检测当前项目是否有虚拟环境，没有就自动创建（确保当前目录有 pyproject.toml 文件）。

```
poetry install

```

这个命令会读取 `pyproject.toml` 中的所有依赖（包括开发依赖）并安装，如果不想安装开发依赖，可以附加 `--no-dev` 选项。如果项目根目录有 `poetry.lock` 文件，会安装这个文件中列出的锁定版本的依赖。

**方式二：**

指定创建虚拟环境时使用的`Python`解释器版本，如下：

```
poetry env use python3

```

`python3`是`python`解释器，相当于`cmd`下输入`python3`。还可以指定解释器路径来创建：

```
poetry env use /usr/bin/python

# Update:20210917
# 指定为conda创建的虚拟环境的解释器（Mac M1安装一些机器学习库可以使用，支持X86架构）
poetry env use /Users/dm/.miniconda3/envs/py37/bin/python

```

### **激活虚拟环境**

执行 poetry 开头的命令并不需要激活虚拟环境，因为它会自动检测到当前虚拟环境。如果你想快速在当前目录对应的虚拟环境中执行命令，可以使用`poetry run <你的命令>` 命令，比如执行`app.py`文件：

> poetry run python [app.py](http://app.py)

如果你想显式的激活虚拟环境，使用 `poetry shell` 命令：

> poetry shell

### **查看虚拟环境信息**

> poetry env info

### **显示虚拟环境所有列表**

> poetry env list

### **显示虚拟环境绝对路径**

> poetry env list --full-path

### **删除虚拟环境**

1. 可以直接删除虚拟环境文件夹
2. 通过`poetry env remove`命令删除

```
# 执行删除虚拟环境时，需要指定对应的解析器版本
poetry env remove python3

```

### **查看python版本**

```
poetry run python -V

```

## **依赖包管理**

### **安装依赖包**

可以使用install命令直接解析并安装pyproject.toml的依赖包

> poetry install

`pyproject.toml`文件的配置如下：

```
[tool.poetry.dependencies]
pendulum = "^1.4"

```

也可以可以使用add命令来安装Python工具包，

> poetry add numpy

还可以，通过添加配置参数--dev来区分不同环境下的依赖包。

> poetry add pytest --dev

`poetry add`依赖安装常见命令如下表格：

### **更新所有锁定版本的依赖包**

> poetry update

### **更新指定依赖包**

> poetry update numpy

### **卸载依赖包**

> poetry remove numpy

### **查看可以更新的依赖**

> poetry show --outdated

### **查看项目安装的依赖**

> poetry show

### **以树形结构查看项目安装的依赖关系**

> poetry show --tree

## **配置Poetry(poetry config)**

Poetry提供了全局配置(config.toml)和特定项目的配置(poetry.toml)。

### **全局配置**

> poetry config virtualenvs.create false
> 
> ```
> virtualenvs.create
> ```

### **特定项目配置**

poetry config后加--local来配置当前项目。

> poetry config virtualenvs.create true --local

### **重置配置**

poetry config的--unset就是用来重置配置的。

**重置全局配置**：

```
poetry config virtualenvs.create --unset

```

**重置项目配置**：

```
poetry config virtualenvs.create --local --unset

```

查看项目下的poetry.toml文件，可以看到值被重置了。

### **列出当前项目的配置**

> poetry config --list

```
cache-dir = "/Users/liguodong/Library/Caches/pypoetry"

experimental.new-installer = **true**

installer.parallel = **true**

virtualenvs.create = **true**

virtualenvs.in-project = **null**

virtualenvs.path = "{cache-dir}/virtualenvs"   # /Users/liguodong/Library/Caches/pypoetry/virtualenvs
```

列出配置时，包括了全局和本地的配置，本地的配置会覆盖全局的参数，例如：`virtualenvs.create`全局为false，本地为true，那这里 `virtualenvs.create=true`

Poetry支持的常用参数有：

## **项目构建及发布**

### **项目打包**

> poetry build

**参数：**

- `-format (-f)`: 限制打包的格式为 `wheel`(whl) 或 `sdist`(tar.gz).

**请注意，目前只支持纯python的wheel。**

### **发布项目包**

此命令将使用build命令生成的包发布到远程仓库，默认上传至PYPY（因此，你需要事先创建一个账号）。 如果这是第一次提交包，它将在上传前自动注册包。

> poetry publish

执行结果：

```
# 需要输入PYPI的用户名和密码
Username: liguodong
Password:
Publishing py-sanic-samples (0.1.0) to PyPI
 - Uploading py-sanic-samples-0.1.0.tar.gz 100%
 - Uploading py_sanic_samples-0.1.0-py3-none-any.whl 100%

```

**参数：**

- `-repository（-r）`：配置将包注册到的存储库（默认值：pypi）。应与config命令设置的存储库名称匹配。
- `-username（-u）`：访问该存储库的用户名。
- `-password（-p）`：访问该存储库的密码。
- `-干运行`：执行除上传包以外的所有操作。

## **总结**

本文简单介绍了Poetry的虚拟环境管理，依赖包管理以及配置Poetry等常用操作。除此之外，还介绍了如何使用Poetry构建包和发布包等操作。

我是果冻，希望我的文章能够帮助到你。

## **参考文档**

- **[poetry official docs](https://link.zhihu.com/?target=https%3A//python-poetry.org/docs/)**