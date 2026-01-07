# NPU

在 MediaTek 中 Neuron Processing Unit (NPU) ，在 MediaTek 中有個 Neuron Studio Profiler 是一個效能分析工具，可協助開發人員分析和最佳化在 NPU 上運行的 AI 模型。

開發上可以參考 Neuron SDK，上面會說可以使用的模型與推論方式。

</br>

[官網](https://neuropilot.mediatek.com/)

可以跟著 [Platforms](https://neuropilot-developer.mediatek.com/sphinx/g720-public/html/) 的部份實做與學習。

</br>

---

</br>

</br>

開始前先搞清楚一些名詞

### NPU (Neural Processing Unit):

- NPU 作為聯發科人工智慧硬體加速器的正式名稱。
- NPU 指MDLA和MVPU兩個組成部分的總稱。

### MDLA (MediaTek Deep Learning Accelerator):

- MDLA 致力於高效率加速卷積神經網路（CNN）工作負載。

### MVPU (MediaTek Vision Processing Unit):

- MVPU 提供通用 DSP 功能，並加速複雜的成像和電腦視覺演算法，包括 AI 模型處理。

### APU(AI Processing Unit):

- APU 是上一代聯發科NPU硬體的術語。
- 對於當前產品和文檔，請使用 NPU 代替 APU。

### AIA (AI Accelerator):

- 向 MDLA 表示，提及「AI 加速器」（AIA）作為聯發科硬體 AI 加速功能的一般描述。


</br>

---

</br>

</br>

# 筆記

根據不同的 Genio Board ，MediaTek 提供不同的 SDK version。

學習成本算高。

</br>

[Genio 720 NeuroPilot](https://neuropilot-developer.mediatek.com/sphinx/neuropilot-8-public/html/)

本文檔詳細介紹了聯發科的 NeuroPilot 軟體工具套件。本節首先概述了本文檔涵蓋的主題，然後介紹了 NeuroPilot 軟體的各種工具、術語和目標。

This documentation is for the following NeuroPilot version and build: 8.0.7 public.

</br>

NeuroPilot 是一套開發者工具和 API 的集合，旨在幫助使用者在聯發科平台上開發高效的 AI 應用。 NeuroPilot 的設計目標是實現“邊緣 AI”，即 AI 處理在設備本地執行，而不是遠端伺服器。借助 NeuroPilot，使用者可以在邊緣設備上有效地開發和部署 AI 應用。這不僅能顯著提升各類 AI 應用的運作速度，還能確保資料隱私安全。

NeuroPilot 的開發者工具支援 TensorFlow、PyTorch 和 TensorFlow Lite (TFLite) 等常用 AI 框架。 NeuroPilot 支援檢查、載入和轉換模型，既可轉換為 MediaTek 最佳化的模型格式，也可轉換為開放框架標準模型格式。

</br>

