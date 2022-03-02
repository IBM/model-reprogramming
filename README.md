# Model Reprogramming Repository

Survey paper: [Model Reprogramming: Resource-Efficient Cross-Domain Machine Learning](https://arxiv.org/abs/2202.10629)

All mentioned references can be found in the survey paper

# What is model reprogramming? 
Model reprogramming enables resource-efficient cross-domain machine learning by repurposing and reusing a well-developed pre-trained model from a source domain to solve tasks in a target domain **without** model finetuning, where the source and target domains can be vastly different. In many applications, model reprogramming outperforms transfer learning and training from scratch.

The general rationale behind model reprogramming lies in repurposing and reusing a well-developed pre-trained model from a source domain to solve new tasks in a target domain without model finetuning. Instead, model reprogramming introduces an input transformation layer and an output mapping layer to the pre-trained source model to empower cross-domain machine learning. Model reprogramming is favorable to the resource-limited setting because it 
* Enables the reuse of pre-trained models from data-rich and well-studied domains (e.g., vision, language, and speech)
* Attains data efficiency by only training the added input transformation and output mapping layers
* Reuses available models and spares model development from scratch

![](https://i.imgur.com/KURlKKq.png)

The figure above illusrates the model reprogramming framework (top) and  some  examples  of  cross-domain  machine  learning  via  modelreprogramming  (bottom).    Model  reprogramming  enables  cross-domain machine learning by adding two modules, an input transfor-mation layer (blue box) and an output mapping layer (green box), to a pre-trained model selected from a source domain.   When reprogrammed  to  solve  target-domain  tasks,  the  pre-trained  sourcemodel is frozen and its model parameters are unchanged. Some ex-amples of cross-domain machine learning including reprogramming speech models for time-series [Yanget al., 2021], language models for molecules [Vinodet al., 2020], and general imaging models for bio-medical measurements [Tsaiet al., 2020].

# Existing works and use cases 



| Reference                                    | Source domain        | Source model   | Target domain                 | Highlights                            |
|----------------------------------------------|----------------------|----------------|-------------------------------|---------------------------------------|
| Elsayed et al., 2019                | General image        | ImageNet       | CIFAR-10/MNIST/counting       | first work; mediocre accuracy         |
| Neekhara et al., 2019               | Text                 | LSTM/CNN       | Character/Word level tasks    | context-based vocabulary mapping      |
| Tsai et al., 2020                     | General image        | ImageNet/API   | Bio-medical measurement/image | black-box reprogramming; new SOTA     |
| Vinod et al., 2020                | Text                 | BERT/LSTM      | Biochemical sequence          | vocabulary embedding mapping          |
| Kloberdanz et al., 2021              | General image        | ImageNet       | Caltech 101/256 (reduced)     | trainable input \&                     output layers                        |
| Lee et al., 2020; Dinh et al., 2022 | Image/Spectrogram    | GAN            | Image/Spectrogram             | reprogram GAN to conditional GAN      |
| Randazzo et al., 2021              | MNIST/lizard pattern | Neural CA      | MNIST/Lizard pattern          | stable out-of-training configurations |
| Hambardzumyan et al., 2021                | Text                 | BERT \&         variants                      | GLUE/SuperGLUE                        | trainable tokens and data efficiency |
| Yang et al., 2021                | Speech               | VGGish         | Univariate time series        | new/same SOTA on 19/30 datasets       |
| Yen et al., 2021                         | Speech               | Acoustic model | Low-resource speech           | new SOTA; reprogramming+finetuning    |
| Chen et al., 2021                  | General image        | ImageNet       | Financial transaction         | overlay image and transaction feature |
| Neekhara et al., 2022                     | General image        | ViT/Imagenet   | Sequence                      | text sentences and DNA sequences      |


##### LSTM means long short-term memory, CNN means convolutional neural network, API means application programming interface, and SOTA means state of the art. BERT stands for bidirectional encoder representations from transformers. GLUE stands for the general language understanding evaluation benchmark. GAN stands for generative adversarial network. CA stands for cellular automata. ViT stands for vision transformer. 

## Adding your work to this table
Please create an issue with the following information
> Paper title:
> 
> Author list:
> 
> Publication venue (arxiv is fine) and year:
> 
> Bibtex citation format:
> 
> Source domain:
> 
> Source model:
> 
> Target domain:
> 
> Highlights:

# Citation

```
@article{chen2022model,
  title={Model Reprogramming: Resource-Efficient Cross-Domain Machine Learning},
  author={Chen, Pin-Yu},
  journal={arXiv preprint arXiv:2202.10629},
  year={2022}
}
```


