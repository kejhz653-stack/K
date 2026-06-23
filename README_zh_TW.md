```markdown
<div align="center">
<img src="./assets/xorbits-logo.png" width="180px" alt="xorbits" />

# Xorbits Inference：模型推理， 輕而易舉 🤖

<p align="center">
  <a href="https://xinference.cn">Xinference 企業版</a> ·
  <a href="https://inference.readthedocs.io/zh-cn/latest/getting_started/installation.html#installation">自託管</a> ·
  <a href="https://inference.readthedocs.io/zh-cn/latest/index.html">文件</a>
</p>

[![PyPI Latest Release](https://img.shields.io/pypi/v/xinference.svg?style=for-the-badge)](https://pypi.org/project/xinference/)
[![License](https://img.shields.io/pypi/l/xinference.svg?style=for-the-badge)](https://github.com/xorbitsai/inference/blob/main/LICENSE)
[![Build Status](https://img.shields.io/github/actions/workflow/status/xorbitsai/inference/python.yaml?branch=main&style=for-the-badge&label=GITHUB%20ACTIONS&logo=github)](https://actions-badge.atrox.dev/xorbitsai/inference/goto?ref=main)
[![Docker Pulls](https://img.shields.io/docker/pulls/xprobe/xinference?style=for-the-badge&logo=docker)](https://hub.docker.com/r/xprobe/xinference)
[![WeChat](https://img.shields.io/badge/添加微信小助手-07C160?style=for-the-badge&logo=wechat&logoColor=white)](https://xinference.cn/images/WeCom.jpg)
[![Telegram](https://img.shields.io/badge/join_Telegram-26A5E4.svg?logo=telegram&style=for-the-badge&logoColor=white)](https://t.me/+nCNpwmySwk9iYmI1)
[![Zhihu](https://img.shields.io/static/v1?style=for-the-badge&message=未来速度&color=0084FF&logo=Zhihu&logoColor=FFFFFF&label=)](https://www.zhihu.com/org/xorbits)

<p align="center">
  <a href="./README.md"><img alt="README in English" src="https://img.shields.io/badge/English-d9d9d9?style=for-the-badge"></a>
  <a href="./README_zh_CN.md"><img alt="簡體中文版自述文件" src="https://img.shields.io/badge/中文介紹-454545?style=for-the-badge"></a>
  <a href="./README_ja_JP.md"><img alt="日本語のREADME" src="https://img.shields.io/badge/日本語-d9d9d9?style=for-the-badge"></a>
</p>
</div>
<br />


Xorbits Inference（Xinference）是一個效能強大且功能完整的分佈式推理框架。可用於大型語言模型（LLM）、語音辨識模型、多模態模型等各類模型的推理。透過 Xorbits Inference，你可以輕鬆一鍵部署你自己的模型或內建的前沿開源模型。無論你是研究者、開發者，或是資料科學家，都可以透過 Xorbits Inference 與最前沿的 AI 模型，發掘更多可能。


<div align="center">
<i><a href="https://xinference.cn/images/WeCom.jpg">👉 新增企業微信、加入Xinference 社群！</a> · <a href="https://t.me/+nCNpwmySwk9iYmI1">加入 Telegram 群組！</a></i>
</div>

## 🔥 近期熱點
### 框架增強
- Agent 原生服務能力：Xinference 與 [Xagent](https://github.com/xorbitsai/xagent) 深度整合，支援動態規劃、工具調用與多步自主推理，突破傳統靜態流程的限制。
- 自動 Batch：多個並發請求會被自動合批處理，大幅提升吞吐量。: [#4197](https://github.com/xorbitsai/inference/pull/4197)
- 支援寒武紀晶片：[#3693](https://github.com/xorbitsai/inference/pull/3693)
- [Xllamacpp](https://github.com/xorbitsai/xllamacpp)：全新 llama.cpp 的 Python binding，由 Xinference 團隊維護，支援持續並行且更適合生產使用: [#2997](https://github.com/xorbitsai/inference/pull/2997)
- 分佈式推理：在多個 worker 上執行大型模型：[#2877](https://github.com/xorbitsai/inference/pull/2877)
- VLLM 引擎增強：跨副本共享 KV Cache: [#2732](https://github.com/xorbitsai/inference/pull/2732)
### 新模型
- 內建 [MiniCPM5-1B](https://huggingface.co/openbmb/MiniCPM5-1B): [#5010](https://github.com/xorbitsai/inference/pull/5010)
- 內建 jina-embeddings-v5 系列（[text-nano](https://huggingface.co/jinaai/jina-embeddings-v5-text-nano)、[text-small](https://huggingface.co/jinaai/jina-embeddings-v5-text-small)、[omni-nano](https://huggingface.co/jinaai/jina-embeddings-v5-omni-nano)、[omni-small](https://huggingface.co/jinaai/jina-embeddings-v5-omni-small)）: [#5018](https://github.com/xorbitsai/inference/pull/5018)
- 內建 MiniCPM-V-4.6 系列（[MiniCPM-V-4.6](https://huggingface.co/openbmb/MiniCPM-V-4.6)、[MiniCPM-V-4.6-Thinking](https://huggingface.co/openbmb/MiniCPM-V-4.6-Thinking)）: [#5025](https://github.com/xorbitsai/inference/pull/5025)
- 內建騰訊 Hy-MT2 系列（[1.8B](https://huggingface.co/tencent/Hy-MT2-1.8B)、[7B](https://huggingface.co/tencent/Hy-MT2-7B)、[30B-A3B](https://huggingface.co/tencent/Hy-MT2-30B-A3B)）: [#5029](https://github.com/xorbitsai/inference/pull/5029)
- 內建 [PaddleOCR-VL-1.6](https://huggingface.co/PaddlePaddle/PaddleOCR-VL-1.6): [#5033](https://github.com/xorbitsai/inference/pull/5033)
- 內建 [VoxCPM2](https://huggingface.co/openbmb/VoxCPM2): [#5045](https://github.com/xorbitsai/inference/pull/5045)
- 內建 [DeepSeek V4](https://api-docs.deepseek.com/news/news260424): [#4938](https://github.com/xorbitsai/inference/pull/4938)
- 內建 [MiniMax-M2.7](https://www.minimax.io/models/text/m27): [#4843](https://github.com/xorbitsai/inference/pull/4843)
### 整合
- [Xagent](https://github.com/xorbitsai/xagent)：企業級 Agent 平台，用於構建與執行具備規劃、記憶與工具調用能力的智能體，不再受限於僵化的工作流程。
- [FastGPT](https://doc.fastai.site/docs/development/custom-models/xinference/)：一個基於 LLM 的開源 AI 知識庫建置平台。提供了開箱即用的資料處理、模型調用、RAG 檢索、視覺化 AI 工作流程編排等能力，幫助您輕鬆實現複雜的問答場景。
- [Dify](https://docs.dify.ai/advanced/model-configuration/xinference)：一個涵蓋大型語言模型開發、部署、維運與最佳化的 LLMOps 平台。
- [RAGFlow](https://github.com/infiniflow/ragflow)：是一款基於深度文件理解構建的開源 RAG 引擎。
- [MaxKB](https://github.com/1Panel-dev/MaxKB)：MaxKB = Max Knowledge Base，是一款基於大型語言模型與 RAG 的開源知識庫問答系統，廣泛應用於智慧客服、企業內部知識庫、學術研究與教育等場景。

## 主要功能
🌟 **模型推理，輕而易舉**：大型語言模型、語音辨識模型、多模態模型的部署流程被大幅簡化。一個指令即可完成模型的部署工作。 

⚡️ **前沿模型，應有盡有**：框架內建眾多中、英文的前沿大型語言模型，包括 baichuan、chatglm2 等，一鍵即可體驗！內建模型列表仍在快速更新中！

🖥 **異構硬體，快如閃電**：透過 [ggml](https://github.com/ggerganov/ggml)，同時使用你的 GPU 與 CPU 進行推理，降低延遲、提高吞吐！

⚙️ **介面調用，靈活多樣**：提供多種使用模型的介面，包括與 OpenAI 相容的 RESTful API（包含 Function Calling）、RPC、命令列、Web UI 等等。方便模型的管理與互動。

🌐 **叢集運算，分佈協同**：支援分佈式部署，透過內建的資源調度器，讓不同大小的模型按需調度到不同機器，充分使用叢集資源。

🔌 **開放生態，無縫對接**：與流行的第三方函式庫無縫對接，包括 [LangChain](https://python.langchain.com/docs/integrations/providers/xinference)、[LlamaIndex](https://gpt-index.readthedocs.io/en/stable/examples/llm/XinferenceLocalDeployment.html#i-run-pip-install-xinference-all-in-a-terminal-window)、[Dify](https://docs.dify.ai/advanced/model-configuration/xinference)，以及 [Chatbox](https://chatboxai.app/)。

## 為什麼選擇 Xinference
| 功能特色                    | Xinference | FastChat | OpenLLM | RayLLM |
|-------------------------|------------|----------|---------|--------|
| 相容 OpenAI 的 RESTful API | ✅ | ✅ | ✅ | ✅ |
| vLLM 整合                 | ✅ | ✅ | ✅ | ✅ |
| 更多推理引擎（GGML、TensorRT）   | ✅ | ❌ | ✅ | ✅ |
| 更多平台支援（CPU、Metal）       | ✅ | ✅ | ❌ | ❌ |
| 分佈式叢集部署                 | ✅ | ❌ | ❌ | ✅ |
| 影像模型（文生圖）               | ✅ | ✅ | ❌ | ❌ |
| 文字嵌入模型                  | ✅ | ❌ | ❌ | ❌ |
| 多模態模型                   | ✅ | ❌ | ❌ | ❌ |
| 語音辨識模型                  | ✅ | ❌ | ❌ | ❌ |
| 更多 OpenAI 功能（函數調用）     | ✅ | ❌ | ❌ | ❌ |

## 使用 Xinference

- **自託管 Xinference 社群版**
使用 [入門指南](#getting-started) 快速在你自己的環境中執行 Xinference。
參考 [文件](https://inference.readthedocs.io/zh-cn) 以獲得參考與更多說明。

- **面向企業/組織的 Xinference 版本**
我們提供額外的企業功能。 [透過企業微信聯絡](https://xinference.cn/images/WeCom.jpg)
或 [提交表單](https://w8v6grm432.feishu.cn/share/base/form/shrcn9u1EBXQxmGMqILEjguuGoh) 討論企業需求。

## 保持領先

在 GitHub 上為 Xinference 點讚，並立即收到新版本的通知。

![star-us](assets/stay_ahead.gif)

## 入門指南

* [文件](https://inference.readthedocs.io/zh-cn/latest/index.html)
* [內建模型](https://inference.readthedocs.io/zh-cn/latest/models/builtin/index.html)
* [自訂模型](https://inference.readthedocs.io/zh-cn/latest/models/custom.html)
* [部署文件](https://inference.readthedocs.io/zh-cn/latest/getting_started/using_xinference.html)
* [範例與教學](https://inference.readthedocs.io/zh-cn/latest/examples/index.html)

### Jupyter Notebook

體驗 Xinference 最輕量的方式是使用我們在 [Google Colab 的 Jupyter Notebook](https://colab.research.google.com/github/xorbitsai/inference/blob/main/examples/Xinference_Quick_Start.ipynb)。

### Docker

NVIDIA GPU 使用者可以使用 [Xinference Docker 映像](https://inference.readthedocs.io/zh-cn/latest/getting_started/using_docker_image.html) 啟動 Xinference 伺服器。在執行安裝指令之前，請確保你的系統中已經安裝了 [Docker](https://docs.docker.com/get-docker/) 與 [CUDA](https://developer.nvidia.com/cuda-downloads)。

### Kubernetes

請確保你的 Kubernetes 叢集已開啟 GPU 支援，然後透過 `helm` 以下列方式安裝。

```
# 新增 xinference 倉庫
helm repo add xinference https://xorbitsai.github.io/xinference-helm-charts

# 更新倉庫，查詢可安裝的版本
helm repo update xinference
helm search repo xinference/xinference --devel --versions

# 在 K8s 中安裝 xinference
helm install xinference xinference/xinference -n xinference --version 0.0.1-v<xinference_release_version>
```

更多客製化安裝方式，請參考[文件](https://inference.readthedocs.io/en/latest/getting_started/using_kubernetes.html)。

### 快速開始

使用 pip 安裝 Xinference，操作如下。（更多選項，請參閱[安裝頁面](https://inference.readthedocs.io/zh-cn/latest/getting_started/installation.html)。）

```bash
pip install "xinference[all]"
```

要啟動一個本地的 Xinference 實例，請執行下列命令：

```bash
xinference-local
```

一旦 Xinference 運行起來，你可以透過多種方式試用：透過網頁介面、使用 cURL、命令列或透過 Xinference 的 Python 用戶端。更多指南，請參閱我們的[文件](https://inference.readthedocs.io/zh-cn/latest/getting_started/using_xinference.html#run-xinference-locally)。

![網頁介面](assets/screenshot.png)

## 參與其中

| 平台                                                                                              | 用途                   |
|-------------------------------------------------------------------------------------------------|----------------------|
| [Github Issues](https://github.com/xorbitsai/inference/issues)                                      | 回報錯誤與提出功能請求。         |
| [Discord](https://discord.gg/Xw9tszSkr5) | 與其他 Xinference 使用者合作。 |
| [Twitter](https://twitter.com/xorbitsio)                                                        | 即時了解新功能。             |
| [微信社群](https://xinference.cn/images/WeCom.jpg)                                     | 與其他 Xinference 使用者交流。 |
| [Telegram](https://t.me/+nCNpwmySwk9iYmI1)                                                       | 加入 Telegram 群組，與其他 Xinference 使用者交流。 |
| [知乎](https://zhihu.com/org/xorbits)                                                             | 了解團隊最新進展。           |

## 引用

如果您覺得本專案有幫助，請用下列格式引用我們：

```bibtex
@inproceedings{lu2024xinference,
    title = "Xinference: Making Large Model Serving Easy",
    author = "Lu, Weizheng and Xiong, Lingfeng and Zhang, Feng and Qin, Xuye and Chen, Yueguo",
    booktitle = "Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing: System Demonstrations",
    month = nov,
    year = "2024",
    address = "Miami, Florida, USA",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.emnlp-demo.30",
    pages = "291--300",
}
```

## 合作

* [琶洲實驗室 | 黃埔](https://www.pazhoulab-huangpu.com/#/)

## 貢獻者

<a href="https://github.com/xorbitsai/inference/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=xorbitsai/inference" />
</a>

## Star 歷史

[![Star History Chart](https://api.star-history.com/svg?repos=xorbitsai/inference&type=Date)](https://star-history.com/#xorbitsai/inference&Date)
```
