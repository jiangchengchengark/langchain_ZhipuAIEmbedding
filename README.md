# 智谱AI Embedding 使用说明

## 简介
本脚本 `ZhipuAIEmbedding.py` 是为 `langchain` 库编写的，用于集成智谱AI的embedding模型。通过将此脚本放置在 `langchain` 库的 `embedding` 文件夹中，并配置好环境变量 `ZHIPUAI_KEY`，即可使用智谱AI的embedding功能。

## 安装步骤

1. **下载并安装 `langchain` 库**：
   ```bash
   pip install langchain
   ```

2. **将 `ZhipuAIEmbedding.py` 脚本放置在 `langchain` 库的 `embedding` 文件夹中**：
   - 通常路径为：`langchain/embedding/ZhipuAIEmbedding.py`

3. **配置环境变量 `ZHIPUAI_KEY`**：
   - 在您的操作系统中设置环境变量 `ZHIPUAI_KEY`，值为您从智谱AI获取的API密钥。
   - 例如，在Linux或macOS上，可以在终端中运行：
     ```bash
     export ZHIPUAI_API_KEY=your_api_key_here
     ```
   - 在Windows上，可以在命令提示符中运行：
     ```cmd
     set ZHIPUAI_API_KEY=your_api_key_here
     ```

## 使用示例

以下是一个简单的使用示例，展示如何使用 `ZhipuAIEmbedding` 进行文本embedding：

```python
import os
os.environ["ZHIPUAI_API_KEY"]="your api key"
from langchain.embeddings.ZhipuAIEmbedding import ZhipuAIEmbeddings

embeddings = ZhipuAIEmbeddings()
# 示例文本
text = "这是一个测试文本。"

# 获取embedding向量
embedding_vector = embeddings.embed_query(text)

print(embedding_vector)
```

## 注意事项

1. **确保网络连接正常**：使用智谱AI的embedding服务需要稳定的网络连接。
2. **API密钥安全**：请妥善保管您的API密钥，避免泄露。

## 联系我们

如果您在使用过程中遇到任何问题，或有任何建议，请随时联系我们：
- 邮箱：3306065226@qq.com
- 官方网站：https://www.zhipuai.cn/

感谢您选择智谱AI！
```

请根据实际情况调整和完善上述内容。希望这个 `readme.py` 文件能帮助用户顺利使用 `ZhipuAIEmbedding.py` 脚本。
