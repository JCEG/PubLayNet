# PubLayNet

PubLayNet is a large dataset of document images, of which the layout is annotated with both bounding boxes and polygonal segmentations. The source of the documents is [PubMed Central Open Access Subset (commercial use collection)](https://www.ncbi.nlm.nih.gov/pmc/tools/openftlist/). The annotations are automatically generated by matching the PDF format and the XML format of the articles in the PubMed Central Open Access Subset. More details are available in our paper ["PubLayNet: largest dataset ever for document layout analysis."](https://arxiv.org/abs/1908.07836).

## Headlines

`03/Dev/2019` - Pre-trained Faster-RCNN model and Mask-RCNN model are [released](pre-trained-models).

`25/Nov/2019` - [**PubTabNet**](https://github.com/ibm-aur-nlp/PubTabNet) is released! PubTabNet is a large dataset for image-based table recognition, containing 568k+ images of tabular data annotated with the corresponding HTML representation of the tables. Table regions are identified using the same algorithm that generates PubLayNet.

`01/Nov/2019` - Our paper ["PubLayNet: largest dataset ever for document layout analysis."](https://arxiv.org/abs/1908.07836) receives the [**best paper award** at ICDAR 2019](http://icdar2019.org/award/)!

`31/Oct/2019` - PubLayNet migrates from Box to [**IBM Data Asset eXchange**](https://developer.ibm.com/exchanges/data/all/publaynet/).

## Updates in progress

### Ground truth of test set

The ground truth of test will not be release, as we want to keep it for a competition in the future. We will offer a service for people to submit and evaluate their results soon.

## Getting data

Images and annotations can be downloaded [here](https://developer.ibm.com/exchanges/data/all/publaynet/). The training set is quite large, so two options are offered. We split the training set into 7 batches, which can be separately downloaded. Or you can also download the full set at once.

If direct download in browser is unstable or you want to download the data from the command line, you can use curl or wget to download the data.

```
curl -o <YOUR_TARGET_DIR>/publaynet.tar.gz https://dax.cdn.appdomain.cloud/dax-publaynet/1.0.0/publaynet.tar.gz
```

```
wget -O <YOUR_TARGET_DIR>/publaynet.tar.gz https://dax.cdn.appdomain.cloud/dax-publaynet/1.0.0/publaynet.tar.gz
```

## Annotation format

The annotation files follows the [json format of the Object Detection task of MS COCO](http://cocodataset.org/#format-data)

## Examples

A [Jupyter notebook](./explore_PubLayNet_dataset.ipynb) is provided to generate the following visualization of the annotations of 20 sample pages.

![alt text](./examples/annotations.png "Annotations of 20 sample pages")
