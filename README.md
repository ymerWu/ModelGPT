<div align='center'>

<h2><a href="https://arxiv.org/abs/2402.12408">ModelGPT: Unleashing LLM's Capabilities for Tailored Model Generation</a></h2>

[Zihao Tang](https://github.com/IshiKura-a/)<sup>1</sup>, [Zheqi Lv](https://github.com/HelloZicky)<sup>1</sup>, [Shengyu Zhang](https://shengyuzhang.github.io/)<sup>1</sup>，[Fei Wu](https://mypage.zju.edu.cn/wufei)<sup>1</sup>, [Kun Kuang](https://kunkuang.github.io/)<sup>1</sup>
 
<sup>1</sup>[Zhejiang University](https://www.zju.edu.cn/english/)
</div>
Official Pytorch Implementation for the research paper titled "ModelGPT: Unleashing LLM's Capabilities for Tailored Model Generation".

## 安装 Installation
Clone this repository and install the required packages:
```shell
git clone https://github.com/IshiKura-a/ModelGPT.git
cd ModelGPT

conda create -n ModelGPT python=3.8
conda activate ModelGPT
conda install pytorch torchvision torchaudio pytorch-cuda=12.0 -c pytorch -c nvidia

pip install -r requirements.txt
```
Download datasets:
* [Office-31](https://www.cc.gatech.edu/~judy/domainadapt/)
* GLUE Benchmark: already installed by pip requirements
* Tabular Datasets: already installed by pip requirements

## 基线 Baseline
对于基线，只需运行基线文件夹中的文件。例如，要运行nlp的基线，请运行：\
For baseline, simply run the file in the folder `baseline`. For example, to run baseline for nlp, run:
```shell
python -m baseline.glue
```

## 训练 Train
要复制我们的结果，请分别对nlp、cv和表格数据集运行main_lora_nlp.py、main_img_cls.py、main_tabular.py，如下所示：\
To replicate our results, run `main_lora_nlp.py`, `main_img_cls.py`, `main_tabular.py` for nlp, cv and tabular datasets individually, like:
```shell
python main_lora_nlp.py
```
超参数设置嵌入到这些文件中。读者还可以参考附录A。\
Hyperparameter settings are embedded into these files. Readers can also refer to Appendix A.

## 引用 Citation
We warmly welcome any discussion in this emerging field! If you are interested in our work, you can star our project and cite our paper:
```bib
@article{tang2024modelgpt,
  title={ModelGPT: Unleashing LLM's Capabilities for Tailored Model Generation},
  author={Tang, Zihao and Lv, Zheqi and Zhang, Shengyu and Wu, Fei and Kuang, Kun},
  journal={arXiv preprint arXiv:2402.12408},
  year={2024}
}
```
