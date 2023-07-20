# snakeAI
This model classifies an image of either a prairie rattlesnake, which has a venomous bite, or a plains garter snake, which is generally not harmful to humans. Both snakes can be found in the same habitat in areas such as North America. This model may be especially helpful to those who are hiking/outdoors to identify a veonomous prairie rattlesnake.

# The Algorithm
This re-trained ResNet-18 model was created on Jetson Nano and trained on a dataset of Prairie rattlesnake images and Plains garter snake images. It runs on an imagenet.py program that will classify the snake as either species.

# Running This Project
1. Make sure that both the Jetson Inference library and Python3 are installed on your Jetson Nano.
2. And download the resnet18.onnx and labels.txt.
3. Open the terminal and navigate to the classification directory: cd jetson-inference/python/training/classification$
4. Process a Snake Image:
     $ NET=models/snake3
     $ DATASET=data/snake3
     $ imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/rattle/rattle5.jpg snake3.jpg 

View a video explanation here: (video link)
