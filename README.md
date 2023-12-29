## NIMA: Neural IMage Assessment



This is a Paddle implementation of the paper [NIMA: Neural IMage Assessment](https://arxiv.org/abs/1709.05424) (accepted at [IEEE Transactions on Image Processing](https://ieeexplore.ieee.org/document/8352823)) by Hossein Talebi and Peyman Milanfar. You can learn more from [this post at Google Research Blog](https://research.googleblog.com/2017/12/introducing-nima-neural-image-assessment.html).



## Usage

To start training on the AVA dataset, first download the dataset from the link above and decompress which should create a directory named ```images/```. Then download the curated annotation CSVs below
which already splits the dataset (You can create your own split of course). Then do

```python
python main.py --img_path /path/to/images/ --train --train_csv_file /path/to/train_labels.csv --val_csv_file /path/to/val_labels.csv --conv_base_lr 5e-4 --dense_lr 5e-3 --decay --ckpt_path /path/to/ckpts --epochs 100 --early_stoppping_patience 10
```

For inference, do

```python
python -W ignore test.py --model /path/to/your_model --test_csv /path/to/test_labels.csv --test_images /path/to/images --predictions /path/to/save/predictions
```

See ```predictions/``` for dumped predictions as an example.


## Pretrained Model

Pretrained Model is in ckpts/epoch-82.pdiparams

## Annotation CSV Files
[Train](https://drive.google.com/file/d/1IBXPXPkCiTz04wWcoReJv4Nk06VsjSkI/view?usp=sharing) [Validation](https://drive.google.com/file/d/1tJfO1zFBoQYzd8kUo5PKeHTcdzBL7115/view?usp=sharing) [Test](https://drive.google.com/file/d/105UGnkglpKuusPhJaPnFSa2JlQV3du9O/view?usp=sharing)


