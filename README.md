# Arabic-Image-Captioning
Generate Arabic captions for images using Deep Learning

Paper: [here](https://www.insticc.org/Primoris/Resources/PaperPdf.ashx?idPaper=88812)

Dataset: [kaggle](https://www.kaggle.com/datasets/kanishkme/flicker-8k-image-dataset-captionstxt)

documentation: [here](https://github.com/NaNo211/Arabic-Image-Captioning/blob/main/ARABIC_CAPTIONING_DOCUMENTATION.pdf)

## Introduction
Image Captioning refers to the art of describing the content of an image by computers. It is a well-known problem in CV and NLP. It has many applications, such as improved information retrieval, early childhood education, for visually impaired persons, for social media, and so on. Although remarkable work has been accomplished recently for English, and due to the lack of large and publicly available dataset, the progress on Arabic Image Captioning is still lagging. Therefore, we developed our own dataset based on Flickr8K. It can be found under **data/Flickr8k_text/** folder, named **Flickr8k.arabic.full.txt**. It has the exact same format as the original Flickr8K.

## Model
Inspired by recent advances in neural machine translation, the sequence-to-sequence encoder-decoder approach was adopted here.
seq2seq encoder-decoder using GRU:
[image](https://github.com/NaNo211/Arabic-Image-Captioning/blob/main/images/seq2seq_no_dropout_3.png)
Merge Model:
[image](https://github.com/NaNo211/Arabic-Image-Captioning/blob/main/images/merge_model.png)
![seq2seq-image-captioning-arabic](https://user-images.githubusercontent.com/9033365/50055387-e3ab9980-0156-11e9-859f-dce71314777a.png)
For mode details, please check the paper.

## Results
Good example:
![good_examples](https://user-images.githubusercontent.com/9033365/50055400-181f5580-0157-11e9-8a00-1d7af672b49f.png)
<br /> <br />
Bad example:
![bad_examples](https://user-images.githubusercontent.com/9033365/50055408-2a998f00-0157-11e9-9d63-2b40e46a78f7.png)

Results show that developing language specific datasets and end-to-end models outperforms translating English generated captions to a destination language as the later may accumulate both models errors: image captioning and translation.

![6](https://user-images.githubusercontent.com/9033365/76162680-71f3ad00-6159-11ea-9b19-e8957435336b.PNG)

## Citation
Please cite [this paper](https://www.insticc.org/Primoris/Resources/PaperPdf.ashx?idPaper=88812):

```
@conference{visapp20,
author={Obeida ElJundi. and Mohamad Dhaybi. and Kotaiba Mokadam. and Hazem Hajj. and Daniel Asmar.},
title={Resources and End-to-End Neural Network Models for Arabic Image Captioning},
booktitle={Proceedings of the 15th International Joint Conference on Computer Vision, Imaging and Computer Graphics Theory and Applications - Volume 5: VISAPP,},
year={2020},
pages={233-241},
publisher={SciTePress},
organization={INSTICC},
doi={10.5220/0008881202330241},
isbn={978-989-758-402-2},
}
```


