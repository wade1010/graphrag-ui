[English](./README.md) | 简体中文

# GraphRAG-UI

GraphRAG-UI 是 [GraphRAG](https://github.com/microsoft/graphrag) 的用户友好界面,GraphRAG 是一个强大的工具,可使用检索增强生成(RAG)方法对大量文本数据进行索引和查询。本项目支持最新版graphrag-0.3.3，旨在为 GraphRAG 提供方便的管理和交互方式,支持配置 ollama 等本地大模型服务,使其更容易为广大用户所使用。

## 致谢

本项目目前是在 [severian42](https://github.com/severian42) 及其 [GraphRAG-Local-UI](https://github.com/severian42/GraphRAG-Local-UI) 项目的基础上升级而来。在此,我要衷心感谢他,为本项目奠定了坚实的基础。后期可能会加入一些新特性。

## 特性

- **直观的 Web 界面**: GraphRAG-UI 提供了用户友好的 Web 界面,可以轻松配置和使用 GraphRAG。
- **索引管理**: 快速创建、更新和管理您的文本数据索引。
- **查询执行**: 提交自然语言查询,并从索引数据中获取相关内容,之后从大模型获取相应结果。
- **配置选项**: 自定义各种设置和参数,以微调索引和查询过程。
- **日志和监控**: 通过详细的日志和状态更新,监控索引和查询任务的进度。


## 示例截图:
### 索引

![GraphRAG UI](./assets/image1.png)

### 图可视化 (GIF 图)

![GraphRAG UI](./assets/image2.gif)

### 使用 GraphRAG 聊天

![GraphRAG UI](./assets/image3.png)

## pip 安装使用

1. 安装ollama（可选）:

    访问 [Ollama官网](https://ollama.com/) 来安装。如果是 Linux ，可以直接运行下面命令

   ```bash
   curl -fsSL https://ollama.com/install.sh | sh
   ```

2. pip 安装本软件：

   ```bash
   pip install graphrag-ui
   或者
   pip install graphrag-ui -i https://pypi.org/simple
   ```

3. 启动 API Server

    ```bash
    graphrag-ui-server
   ```

4. 启动 UI

    启动综合版 UI

    ```bash
    graphrag-ui
   ```

    或启动纯净版 UI

    ```bash
    graphrag-ui-pure
   ```



## 源码安装使用

1. 创建并激活一个新的conda环境：
    ```bash
    conda create -n graphrag-ui -y python=3.10
    conda activate graphrag-ui
    ```


2. 安装ollama（可选）:

    访问 [Ollama官网](https://ollama.com/) 来安装。如果是 Linux ，可以直接运行下面命令

   ```bash
   curl -fsSL https://ollama.com/install.sh | sh
   ```

3. 克隆存储库:

   ```bash
   git clone https://github.com/wade1010/graphrag-ui.git
   ```


4. 安装所需的软件包：
    ```bash
    cd graphrag-ui
    pip install -r requirements.txt
    ```

5. 启动API服务器
    ```bash
    python api.py --host 0.0.0.0 --port 8012 --reload
    ```

6.  启动

    - **纯净版**

        该版本只做索引、Prompt Tuning 和文件管理，没有查询功能。
        ```bash
        gradio index_app.py
        或者
        python index_app.py
        ```
    - **综合版**

        该版本在纯净版的基础上增加了可视化图表、配置管理和使用 GraphRAG 聊天。
        ```bash
        python app.py
        ```
7. 访问 UI
    - **纯净版**： `http://localhost:7860`
    - **综合版**： `http://localhost:7862`

## 安装使用博客

[https://blog.csdn.net/wade1010/article/details/142374956](https://blog.csdn.net/wade1010/article/details/142374956)