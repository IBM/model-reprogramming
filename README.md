# Model Reprogramming Repository

Survey paper: [Model Reprogramming: Resource-Efficient Cross-Domain Machine Learning](https://arxiv.org/abs/2202.10629)

# What is model reprogramming? 
Model reprogramming enables resource-efficient cross-domain machine learning by repurposing and reusing a well-developed pre-trained model from a source domain to solve tasks in a target domain **without** model finetuning, where the source and target domains can be vastly different. In many applications, model reprogramming outperforms transfer learning and training from scratch.

The general rationale behind model reprogramming lies in repurposing and reusing a well-developed pre-trained model from a source domain to solve new tasks in a target domain without model finetuning. Instead, model reprogramming introduces an input transformation layer and an output mapping layer to the pre-trained source model to empower cross-domain machine learning. Model reprogramming is favorable to the resource-limited setting because it 
* Enables the reuse of pre-trained models from data-rich and well-studied domains (e.g., vision, language, and speech)
* Attains data efficiency by only training the added input transformation and output mapping layers
* Reuses available models and spares model development from scratch

![](https://i.imgur.com/KURlKKq.png)

The figure above illusrates the model reprogramming framework (top) and  some  examples  of  cross-domain  machine  learning  via  modelreprogramming  (bottom).    Model  reprogramming  enables  cross-domain machine learning by adding two modules, an input transfor-mation layer (blue box) and an output mapping layer (green box), to a pre-trained model selected from a source domain.   When reprogrammed  to  solve  target-domain  tasks,  the  pre-trained  sourcemodel is frozen and its model parameters are unchanged. Some ex-amples of cross-domain machine learning including reprogramming speech models for time-series [Yanget al., 2021], language models for molecules [Vinodet al., 2020], and general imaging models for bio-medical measurements [Tsaiet al., 2020].

# Citation

```
@article{chen2022model,
  title={Model Reprogramming: Resource-Efficient Cross-Domain Machine Learning},
  author={Chen, Pin-Yu},
  journal={arXiv preprint arXiv:2202.10629},
  year={2022}
}
```


