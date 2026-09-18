<p align="center">
  <img src="./assets/figures/prokda_font.png" alt="ProKDA" width="640" />
</p>

<table>
  <tr>
    <td width="110" align="center" valign="middle">
      <img src="./assets/figures/prokda_logo.png" alt="ProKDA Logo" width="70" />
    </td>
    <td valign="middle">
      <h2><em>Learn Before You Judge: Progressive Knowledge-to-Decision Alignment for Explainable Hateful Meme Detection</em></h2>
    </td>
  </tr>
</table>


<p align="center">
  <a href="https://arxiv.org/abs/2609.19778">
    <img src="https://img.shields.io/badge/arXiv-2609.19778-b31b1b.svg" alt="arXiv" />
  </a>
  <a href="https://meizhiyuan88666.github.io/prokda/">
    <img src="https://img.shields.io/badge/Project-Page-0052D9.svg" alt="Project Page" />
  </a>
  <a href="https://github.com/MeiZhiyuan88666/ProKDA-Source">
    <img src="https://img.shields.io/badge/GitHub-Code-181717.svg?logo=github" alt="GitHub" />
  </a>
  <a href="https://github.com/MeiZhiyuan88666/ProKDA-Source/stargazers">
    <img src="https://img.shields.io/github/stars/MeiZhiyuan88666/ProKDA-Source?style=flat&logo=github" alt="GitHub stars" />
  </a>
  <a href="https://github.com/MeiZhiyuan88666/ProKDA-Source/forks">
    <img src="https://img.shields.io/github/forks/MeiZhiyuan88666/ProKDA-Source?style=flat&logo=github" alt="GitHub forks" />
  </a>
</p>

## <img src="assets/icons/overview.png" width="40" align="absmiddle"> Overview

Hateful memes often express abusive or discriminatory meanings through subtle interactions between visual content, text, and external background knowledge, making hatefulness difficult to determine from the meme alone. Existing explain-then-detect methods jointly optimize explanation generation and label prediction, which may introduce task interference and degrade detection performance. To address this, we propose **ProKDA**, which separates knowledge acquisition from decision learning and progressively transforms background knowledge into reliable hatefulness judgments.

<p align="center">
  <img src="assets/figures/introduction.png" width="70%" alt="Overview of ProKDA" />
</p>

The core idea of ProKDA can be summarized as:

> **Learn relevant knowledge first, and make the hatefulness judgment afterwards.**

This progressive formulation enables the model to exploit external knowledge while reducing the interference between explanation generation and label prediction.

## <img src="assets/icons/method.png" width="40" align="absmiddle"> Method

ProKDA combines **agentic background knowledge construction** with **progressive knowledge-to-decision alignment**. It first builds meme-specific background knowledge through an agentic pipeline that identifies external knowledge needs, retrieves relevant evidence, and organizes it into textual, visual, and multimodal knowledge. Based on this knowledge, ProKDA progressively trains the multimodal model through **background knowledge learning**, **hatefulness detection learning**, and **hatefulness boundary alignment**, gradually transforming external knowledge into reliable hatefulness decisions while reducing interference between explanation generation and label prediction.

<p align="center">
  <img src="assets/figures/method.png" width="65%" alt="ProKDA method" />
</p>

## <img src="assets/icons/result.png" width="40" align="absmiddle"> Results

We evaluate ProKDA on three widely used hateful meme benchmarks:

- **HMC**
- **MAMI**
- **PrideMM**

ProKDA consistently improves hateful meme detection across different datasets and model scales. In particular, the Qwen2.5-VL-7B based ProKDA achieves strong performance across all three benchmarks, demonstrating the effectiveness of progressive knowledge-to-decision alignment.

Compared with conventional **direct detection**, **explain-then-detect**, and **DPO-based** baselines, ProKDA shows that explicitly separating knowledge learning from decision learning provides a more effective way to incorporate external knowledge into hateful meme detection.

<p align="center">
  <img src="assets/figures/result.png" width="70%" alt="Main results" />
</p>

## <img src="assets/icons/example.png" width="40" align="absmiddle"> Qualitative Examples

The following qualitative examples illustrate how ProKDA leverages relevant background knowledge to understand implicit hateful meanings and support its final decisions.

#### Implicit Hateful Meaning

ProKDA identifies implicit hateful intent by connecting visual and textual cues with relevant background knowledge.

<p align="center">
  <img src="assets/figures/case1.png" width="50%" alt="Implicit hateful meaning example" />
</p>

#### Background Knowledge Matters

External knowledge helps ProKDA resolve references beyond the meme image and text alone.

<p align="center">
  <img src="assets/figures/case4.png" width="50%" alt="Background knowledge example" />
</p>

#### Evidence-Supported Decision

ProKDA aligns background knowledge with final decisions, enabling more reliable explanations.

<p align="center">
  <img src="assets/figures/case6.png" width="50%" alt="Evidence-supported decision example" />
</p>

## <img src="assets/icons/cite.png" width="40" align="absmiddle"> Citation

If you find **ProKDA** useful in your research, please consider citing our work:

```bibtex
@article{prokda2026,
  title   = {Learn Before You Judge: Progressive Knowledge-to-Decision Alignment for Explainable Hateful Meme Detection},
  author  = {Bo Xu and Chenyuan Wang and Xinyu Chen and Quanhao Zhu and Rui Lin and Liang Zhao and Hongfei Lin and Feng Xia},
  journal = {arXiv preprint arXiv:2609.19778},
  year    = {2026}
}
```

## <img src="assets/icons/acknowledgement.png" width="50" align="absmiddle"> Acknowledgements

We thank the authors and maintainers of the datasets, models, and open-source projects that made this work possible.
