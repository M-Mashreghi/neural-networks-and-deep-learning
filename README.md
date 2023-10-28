# neural-networks-and-deep-learning

<h1>HW1</h1> <h1>Question 1</h1> <p> - The DFA state transition table was converted to a state description table suitable for implementing a neural network. The table specified the current state (0-3), input (0 or 1), next state (0-3), and whether the state is an accepting state (0 or 1). </p> <p> - Three separate networks were drawn to represent the transitions: <ul> <li>A 2-4-2 network for next state. Inputs are current state and input, outputs are next state.</li> <li>A 2-3-1 network for accepted state. Input is just current state, output is accept or not.</li> <li>A 3-4-3 combined network with inputs as current state, input and accepted state. Outputs are next state and accepted state.</li> </ul> </p> <p> - The networks were optimized to have the minimal neurons and threshold. The combined network with 3 inputs, 3 hidden neurons and threshold of 2 was optimal. </p> <p> - The combined network was implemented in Python. A loop tested all input combinations, printing the next state and accepted values. The results matched the DFA, validating the network works. </p> <h1>Question 2</h1> <p> - Two sample datasets were defined, each with 100 points: <ul> <li>Set 1 had x ~ N(0, 0.1) and y ~ N(0, 0.4)</li> <li>Set 2 had x ~ N(1, 0.2) and y ~ N(1, 0.2)</li> </ul> </p> <p> - The scatter plot showed two distinct clusters centered at (0,0) and (1,1). </p> <p> - An Adaline network was trained to separate the datasets. The mean squared error decreased smoothly, indicating good separation. </p> <p> - The variance of the datasets was then increased. The data overlapped more and the Adaline did not separate as cleanly. </p> <h1>Question 3</h1> <p> - The MNIST dataset was loaded using TensorFlow/Keras and some sample images visualized. </p> <p> - The data was normalized to the range [0,1]. The number of images per digit class was visualized. </p> <p> - An autoencoder was built with encoder and decoder components. It was trained and the loss curves showed steady decrease. </p> <p> - The 30-neuron encoder output was used as features for a simple 2 layer classifier. Accuracy and loss curves were plotted during training. </p> <p> - The classifier achieved 97% test accuracy. The confusion matrix showed some errors between similar digits like 4/9. </p> <h1>Question 4</h1> <p> - The car price dataset was loaded into Pandas and exploratory analysis done: <ul> <li>Checked and handled missing values</li> <li>Extracted company name from car names</li> <li>Converted categorical features to numerical</li> <li>Identified mileage as most correlated with price</li> <li>Plotted price distribution and vs mileage</li> </ul> </p> <p> - Data was split into train/test and normalized </p> <p> - 3 MLPs were built with varying layers and compared. 3 layers performed best with lowest validation loss. </p> <p> - The hyperparameters of the 3 layer MLP were tuned. Adam optimizer and MSE loss worked best. </p> <p> - Made price predictions on test set. Compared to true values to calculate error. </p>


<h1>HW2</h1> <h2>Question 1:</h2> <ul> <li>Preprocess MNIST, CIFAR-10, and Fashion-MNIST datasets as described in the paper</li> <li>Explain the different layers used in the proposed shallow CNN architecture</li> <li>Implement the proposed architectures with hyperparameters from paper</li> <li>Plot test accuracy curves and report test accuracy like Figures 2,3,4 and Table 1 in paper</li> <li>Plot train loss and accuracy curves</li> </ul> <h2>Question 2:</h2> <ul> <li>Explain data preprocessing and augmentation techniques used in the paper</li> <li>Preprocess chest x-ray pneumonia dataset into train, test, validation splits</li> <li>Explain layers of EfficientNet architecture and why it was chosen</li> <li>Implement EfficientNet model from paper</li> <li>Report accuracy, precision, F1-score after training and evaluating on dataset</li> <li>Plot loss, accuracy, ROC curve, confusion matrix</li> <li>Interpret and analyze the results</li> </ul>



<h1>HW3</h1> <h2>Question 1 - Transfer Learning</h2> <ul> <li>You will be assigned a transfer learning paper based on the last digits of your student IDs. Read and summarize the key points of your assigned paper.</li> <li>Explain the network architecture used in the paper, along with any pros/cons.</li> <li>Describe what data preprocessing is needed for the input images.</li> <li>What types of images can the network classify? What if a new image is not in the classes it was trained on?</li> <li>Obtain the dataset indicated in the table for your assigned network.</li> <li>Implement the network architecture from the paper.</li> <li>Train the network on the dataset and report accuracy, loss, confusion matrix, precision, and f1-score on the test set.</li> </ul> <h2>Question 2 - Object Detection</h2> <ul> <li>Briefly explain how the Faster R-CNN architecture works for object detection.</li> <li>You will retrain a pre-trained Faster R-CNN model on a provided dataset of images containing humans, bikes, cars, motorcycles and airplanes.</li> <li>Retrain the model on the new dataset using the training code provided.</li> <li>Run inference on 3 test images to detect and count the objects present.</li> <li>Your output detected images should match the example provided in terms of bounding boxes and object labels.</li> </ul> <p>The key things are studying your assigned paper, implementing the network architecture, training on the indicated dataset, evaluating on the test set, and analyzing the results.</p>



<h1>HW4</h1><h2>Question 1 - Image Captioning</h2> <ul> <li>Download and preprocess the Flickr8k dataset - extract the images and captions text file.</li> <li>Tokenize the captions and build a vocabulary dictionary mapping words to indices.</li> <li>Pad captions to a fixed length and preprocess - convert to embedded vectors using PyTorch Embedding layer.</li> <li>Load a pretrained ResNet18 model and extract image features from the CNN.</li> <li>Feed the image features and caption embeddings to an LSTM decoder to generate captions.</li> <li>Train the model end-to-end, plot training and test loss/accuracy over epochs.</li> <li>During inference, feed an image and generate a caption using the trained model.</li> <li>Report generated captions on 3 test set images.</li> </ul> <h2>Question 2 - Intent Classification</h2> <ul> <li>Explain how LSTM architectures improve over simple RNNs for sequence tasks.</li> <li>Explain the concept of word embeddings, how they are created, and benefits.</li> <li>Preprocess the TREC question intent dataset - tokenize, normalize text.</li> <li>Implement two models from the paper for intent classification - one predicting top level intent and one predicting top level + sub level.</li> <li>Train the models on the training set, plot accuracy and loss curves.</li> <li>Evaluate the models by reporting accuracy, loss, confusion matrix, precision, recall, F1-score on the test set.</li> <li>Implement the Responder model which generates relevant but not necessarily correct answers.</li> </ul>


<h1>HW5</h1> <h2>Question 1 - Extractive QA System</h2> <ul> <li>Read the BERT paper to understand its architecture, input representations, and pretraining objectives. Explain the key components like the transformer architecture and self-attention.</li> <li>Describe the overall QA model architecture you will design using BERT. Explain the inputs, outputs, loss functions, and what the model will learn.</li> <li>Preprocess the PQuAD dataset - tokenize text, convert words to IDs, pad sequences, etc. Report dataset statistics.</li> <li>Implement the model using ParsBERT and ALBERT pretrained models. Cannot use AutoModelForQA classes.</li> <li>Handle exceptions during inference like long context texts. Report exceptions encountered.</li> <li>Evaluate the models on test set using exact match and F1 scores. Compare to results in the paper.</li> </ul> <h2>Question 2 - Vision Transformer Image Classification</h2> <ul> <li>Explain vision transformers and how they have recently gained popularity over CNNs for vision tasks.</li> <li>Load and preprocess CIFAR-10 dataset.</li> <li>Fine-tune a CNN model by unfreezing specified layers as described in the paper. Report validation accuracy and loss.</li> <li>Fine-tune a ViT model by unfreezing specified layers. Report validation accuracy and loss.</li> <li>Compare your ViT and CNN fine-tuning results to the paper.</li> </ul>







