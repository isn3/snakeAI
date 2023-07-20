# snakeAI
This model classifies an image of either a prairie rattlesnake, which has a venomous bite, or a plains garter snake, which is generally not harmful to humans. Both snakes can be found in the same habitat in areas such as North America. This model may be especially helpful to those who are hiking/outdoors to identify a veonomous prairie rattlesnake.

# The Algorithm
This re-trained ResNet-18 model was created on Jetson Nano and trained on a dataset of prairie rattlesnake images and garter snake images. It runs on an imagenet.py program that will classify the snake as either species.

# Running This Project
1. Make sure that both the Jetson Inference library and Python3 are installed on your Jetson Nano.
2. And download the resnet18.onnx.
3. Open the terminal and navigate to the classification directory: cd jetson-inference/python/training/classification$
4. Set the net and data variables as shown below:
```
   $ NET=models/snake
   $ DATASET=data/snake3
```
5. Use this command to process the image:
```
   imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/rattle/rattle4.jpg snake3.jpg
```
6. Finally, view the image output to see the classification as "prairie rattlesnake" or "garter snake."

View a video explanation here: (video link)
