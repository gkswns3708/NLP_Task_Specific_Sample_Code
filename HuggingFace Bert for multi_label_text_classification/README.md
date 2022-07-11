# HuggingFace Bert for multi_label_text_classification

[CLS] 토큰을 이용해 Multilabel-Classification Task를 수행해 보았습니다.

먼저 Multi-label Classification은 2가지 방법론으로 구현될 수 있는데,
1. 모든 조합을 Sigle Category로 만들어서 단일 Classification으로 만드는 방법
2. 각각의 Class에 대한 Confidence Score를 계산한 뒤, 임계값(Threshold)를 넘는지 확인해 Prediction을 얻는 방법.

1번의 경우 많은 Class가 많아짐에 따라 num_label = k일때, $2^{k}$ 의 Class가 생기게 됩니다. 
너무 많은 Class에 대해서 Prediction하는 것은 성능이 안 좋아질 수 있고,
현재 목표하고자 하는 Project의 경우 Class가 약 60개이므로 본 Code 또한 2번 방법론으로 진행되었습니다.

또한 Naive 구현이 아닌 HuggingFace API를 이용해 구현되었습니다.

- Reference
  - [🤗 HuggingFace bert-base-multilingual-cased](https://huggingface.co/bert-base-multilingual-cased)
  - [🤗 HuggingFace](https://huggingface.co/)
