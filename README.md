Caltech Pedestrian Dataset Converter
============================

# Requirements

- OpenCV 3.0+ (with Python binding)
- Python 2.7+, 3.4+, 3.5+
- NumPy 1.10+
- SciPy 0.16+

# Caltech Pedestrian Dataset
- Download dataset
 
Download dataset `data_and_labels.zip` using following [link](https://data.caltech.edu/records/f6rph-90m20). </br>
After unzip,
```
Train/
    Train/seq*/
        Train/seq*/
    Train/seq*/
        Train/seq*/
    .....
Test/
    Test/seq*/
        Test/seq*/seq*/
    .....
annotations/
    annotations/annotations/
        ~~~~
```

- Move dataset

Move dataset under `<rootdir>/data` directory
```
$ bash shells/download.sh (Does not exist anymore -> Do not use this!)
$ python scripts/convert_annotations.py
$ python scripts/convert_seqs.py
```

Each `.seq` movie is separated into `.png` images. Each image's filename is consisted of `{set**}_{V***}_{frame_num}.png`. According to [the official site](http://www.vision.caltech.edu/Image_Datasets/CaltechPedestrians/), `set06`~`set10` are for test dataset, while the rest are for training dataset.

(Number of objects: 346621)

# Draw Bounding Boxes

```
$ python tests/test_plot_annotations.py
```
