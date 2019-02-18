aticle:
https://robopress.robotsandpencils.com/build-your-own-image-classifier-in-less-time-than-it-takes-to-bake-a-pizza-9a7b898264de
https://www.tensorflow.org/hub/tutorials/image_retraining



prerequered:
python 3.6 (+ pip)

install:
pip install numpy
pip install tensorflow
pip install tensorflow_hub

add images:
training_data
-Red Apple
--xxxx
--xxxx
--xxxx
-Red Ball
--xxxx
--xxxx
--xxxx
test_data
--xxxx
--xxxx
--xxxx

run:
python retrain.py --how_many_training_steps 500 -- output_graph=./retrained_graph.pb --output_labels=./retrained_labels.txt --image_dir=./training_data



python label_image.py --graph=./retrained_graph.pb --labels=./retrained_labels.txt --input_layer=Placeholder --output_layer=final_result --image=E:/workspace/cnn/tensorflow_test1/tensorflow/examples/image_retraining/test_data/ra101.jpg

python label_image_V2.py --graph=./retrained_graph.pb --labels=./retrained_labels.txt --input_layer=Placeholder --output_layer=final_result --image_dir=E:/workspace/cnn/test_data
