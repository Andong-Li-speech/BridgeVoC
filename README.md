# BridgeVoC
This is the repository for the work "BridgeVoC: Revitalizing Neural Vocoder from a Restoration Perspective". Our conference work has been accepted by IJCAI 2025, and the extension is submitted to IEEE Transactions on Pattern Analysis and Machine Intelligence.

### Authors: Andong Li, Tong Lei, Rilin Chen, Kai Li, Meng Yu, Xiaodong Li, Dong Yu, and Chengshi Zheng

## 📌 Key Updates
<details>
  <summary>📅 Full Update History</summary>
  <ul>
    <li><strong>2025.11.03</strong>: Training code released</li>
  </ul>
</details>

## 🔍 Abstract
Despite significant advances in neural vocoders using diffusion models and their variants, these methods, unfortunately, inherently suffer from a performance-inference dilemma, which stems from the iterative nature in the reverse inference
process. This hurdle can heavily hinder the development of this field. To address this challenge, in this paper, we revisit the neural vocoder task through the lens of audio restoration and propose a novel diffusion vocoder called BridgeVoC. Specifically, by rank analysis, we compare the rank characteristics of Mel-spectrum with other common acoustic degradation factors, and cast the vocoder task as a specialized case of audio restoration, where the range-space spectral (RSS) surrogate of the target spectrum serves as the degraded input. Based on that, we introduce the Schrodinger bridge framework for diffusion modeling, which defines the RSS and target spectrum as dual endpoints of the stochastic generation trajectory. Further, to fully utilize the hierarchical prior of subbands in the time-frequency (T-F) domain, we elaborately devise a novel subband-aware convolutional diffusion network as the data predictor, where subbands are divided following an uneven strategy, and convolutional-style attention module is employed with large kernels for efficient T-F contextual modeling. To enable single-step inference, we propose an omnidirectional distillation loss to facilitate effective information transfer from the teacher to student models, and the performance is improved by combining target-related and bijective consistency losses. Comprehensive experiments are conducted on various benchmarks and out-of-distribution datasets. Quantitative and qualitative results show that while enjoying fewer parameters, lower computational cost and competitive inference speed, the proposed BridgeVoC yields state-of-the art performance over existing advanced GAN-, DDPM- and flow-matching-based baselines with only 4 sampling steps. And consistent superiority is still achieved with single-step inference. Training code and demo are available at:
[https://github.com/Andong-Li-speech/BridgeVoC-demo](https://andong-li-speech.github.io/BridgeVoC-demo/).

## 📊 Experimental Results

### Performance Comparison
<div style="margin: 20px 0;">
  <h4>🎯 Bubble Figure on LibriTTS Benchmark</h4>
  <img src="./figure/bubble_figure.png" width="60%" height="auto" style="border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
</div>

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">
  <div>
    <h4>📈 On LibriTTS Benchmark</h4>
    <img src="./figure/performance_libritts.png" width="100%" height="auto" style="border-radius: 8px;">
  </div>
  <div>
    <h4>📈 On LJSpeech Benchmark</h4>
    <img src="./figure/performance_ljs.png" width="50%" height="auto" style="border-radius: 8px;">
  </div>
  <div>
    <h4>📈 On Out-of-Distributions Benchmarks</h4>
    <img src="./figure/performance_otf.png" width="100%" height="auto" style="border-radius: 8px;">
  </div>
</div>



## 📚 Citation
If you find this work helpful, please cite our paper:
```bibtex
@inproceedings{ijcai2025p0903,
  title     = {BridgeVoC: Neural Vocoder with Schrödinger Bridge},
  author    = {Lei, Tong and Zhang, Zhiyu and Chen, Rilin and Yu, Meng and Lu, Jing and Zheng, Chengshi and Yu, Dong and Li, Andong},
  booktitle = {Proceedings of the Thirty-Fourth International Joint Conference on
               Artificial Intelligence, {IJCAI-25}},
  publisher = {International Joint Conferences on Artificial Intelligence Organization},
  editor    = {James Kwok},
  pages     = {8122--8130},
  year      = {2025},
  month     = {8},
  note      = {Main Track},
  doi       = {10.24963/ijcai.2025/903},
  url       = {https://doi.org/10.24963/ijcai.2025/903},
}
```

## 🤝 Contributing
We welcome contributions! Please feel free to submit issues, fork the repository, and send pull requests.
