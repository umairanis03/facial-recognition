# Validation Dataset preparation

For validation during training and verification purpose, insightface repo requires testing file in the binary format.

The steps to produce this file are given below:
- Firstly convert your custom dataset in the lfw format which is..
> custom_dataset/
>   > >
>   >  firstname_lastname/
>   > > firstname_lastname_0001.jpg
>   > >firstname_lastname_0002.jpg
>   > >firstname_lastname_0003.jpg
>   > >
>   > firstname_lastname/
>   > > firstname_lastname_0001.jpg
>   > >firstname_lastname_0002.jpg
>   > >firstname_lastname_0003.jpg


- After getting your dataset into the correct format use [this](https://github.com/armanrahman22/Facial-Recognition-and-Alignment) repository to make a file called `pairs.txt`
    - Installed the mentioned dependencies
    - Move to `Facial-Recognition-and-Alignment/facenet_sandberg/generate_pairs.py` 
    - Demo `python generate_pairs.py --image_dir /my/datastet --pairs_file_name pairs.txt --num_folds 10 --num_matches_mismatches 300`
    - `pairs.txt` will be prepared in the same folder
- For preparing `lfw.bin`
    - Move to `insightface/src/data/lfw2pack.py`
    - Put `pairs.txt` in your dataset directory
    - `python lfw2pack.py --data-dir /my/datastet --image_size 112,112 --output lfw.bin`
    - `lfw.bin` will be prepared
- For inference on this validation file:
    - Move to `insightface/src/data/eval/verification.py`
    - Before running the validation script group `lfw.py` and `property` file in the same directory say `my/test/`
    -  `python3 verification.py --data-dir ../../my/test --model ../../models/model-r100-ii/model,0 --nfolds 10 --target lfw`


### :thinking_face: Still here, go-train, go-test Man!
 
