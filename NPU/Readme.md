# NPU

在 MediaTek 中 NPU 的使用＆學習：[官網](https://neuropilot.mediatek.com/)

Main Board : MediaTek Genio 720 EVK

Notice : 無 NDA access 也可以使用，用的是 [NeuroPilot Public](https://neuropilot-developer.mediatek.com)

---

### 簡介

很多文獻跟參考資料大部都會稱 MTK 的 NPU 為 APU，但是在 Genio 720 開始後統稱 NPU 了，MTK 提供的開發工具為  [NeuroPilot](https://neuropilot-developer.mediatek.com/sphinx/neuropilot-8-public/html/l1_introduction/l2_sw_ecosystem/sw_ecosystem.html)，NeuroPilot 是一套開發者工具和API集合，幫助使用者在聯發科平台上有效開發 AI 應用，使用者可以極其有效地在邊緣設備上開發和部署 AI 應用。

</br>

---

</br>

開始前先搞清楚一些名詞

### NPU (Neural Processing Unit):

- NPU 作為聯發科人工智慧硬體加速器的正式名稱。
- NPU 指 MDLA 和 MVPU 兩個組成部分的總稱。

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

</br>


# G720

[G720 Documentation](https://neuropilot-developer.mediatek.com/sphinx/g720-public/html/)

</br>

### Supported Operations
- [TFLite Operations](https://neuropilot-developer.mediatek.com/sphinx/g720-public/html/l1_supported_operations/l2_supported_operations/l3_supported_ops/supported_operations_public.html)

- [CPU Guidelines](https://neuropilot-developer.mediatek.com/sphinx/g720-public/html/l1_supported_operations/l2_supported_operations/l3_cpu_guide/cpu_64bit_fp16_guidelines.html)

- [GPU Guidelines](https://neuropilot-developer.mediatek.com/sphinx/g720-public/html/l1_supported_operations/l2_supported_operations/l3_gpu_guide/gpu_guidelines.html)

- [MDLA 5.3 Guidelines](https://neuropilot-developer.mediatek.com/sphinx/g720-public/html/l1_supported_operations/l2_supported_operations/l3_mdla_guide/mdla_guidelines_5_3_public.html)

MTK 提供很多跑 Edge AI 的方法，可以針對自己的需求進行開發。

每一項裡面都有詳系列出支援的 Data Type 與模型。

</br>

# NeuroPilot

這邊介紹與筆記 NeuroPilot 的使用與開發。

</br>

首先先確定 [NeuroPilot Versions](https://neuropilot-developer.mediatek.com/sphinx/neuropilot-8-public/html/l1_introduction/l2_np_versions/neuropilot_versions.html)，我們是做使用與應用重點不是完整開發這顆 NPU，所以不用 NDA 也足夠。

</br>

Public 的功能：

| Feature | Type | Description |
| :------ | :--- | :---------- |
| 轉換工具 | 命令列工具 | 預先訓練和最佳化的 PyTorch 或 TensorFlow 模型轉換為 TensorFlow Lite 模型，並執行訓練後量化 | 
| TFLite Shim API | API | TFLite Shim API 是一個便利 API，它封裝了 TensorFlow Lite 的原生 C++ API |

</br>

## NeuroPilot Tools

