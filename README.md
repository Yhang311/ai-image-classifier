## 项目简介

这是一个基于 Streamlit 的 AI 图片分类 Web 应用，使用 `MobileNetV2` 预训练模型对上传的图片进行识别，返回概率最高的前三个类别及其置信度。

## 功能特性

- 上传本地 `jpg` / `png` 图片进行在线预测
- 使用 `TensorFlow` 官方提供的 `MobileNetV2` 预训练模型
- 自动展示预测 Top 3 标签与概率
- 通过 Streamlit 提供交互式 Web 界面

## 环境要求

- Python 3.9+
- `pip` 或 `pipenv` 等包管理工具
- 能联网下载 `tensorflow` 预训练权重（首次运行时）

## 安装与运行

```bash
git clone <your-repo-url>
cd project2

python -m venv .venv
.\.venv\Scripts\activate  # Windows PowerShell

pip install -r requirements.txt  # 若无该文件，请参照 pyproject.toml 安装依赖

streamlit run main.py
```

> 如果使用 `pyproject.toml` 管理依赖，可执行：
>
> ```bash
> pip install .
> ```

## 使用说明

1. 在浏览器打开 `http://localhost:8501`。
2. 点击“Choose an image…”上传需要识别的图片。
3. 点击“Classify Image”按钮。
4. 在“Predictions”区域查看预测标签及对应置信度。

## 常见问题

- **启动缓慢**：首次运行会自动下载 `MobileNetV2` 预训练权重，需耐心等待。
- **GPU 支持**：当前脚本默认使用 CPU，若需 GPU，请安装支持 CUDA 的 TensorFlow 版本。
- **缓存机制**：模型加载使用 `@st.cache_resource` 进行缓存，重复请求无需重新下载或加载模型。

## 许可证

根据项目实际情况填写许可证信息，例如 MIT、Apache-2.0 等。

