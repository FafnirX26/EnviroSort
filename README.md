# EnviroSort: AI-Driven Waste Management Solution

## How to Use
- Step 1: Open a new Google Colaboratory
- Step 2: Find the code located in 'envirosort.py'
- Step 3: Copy the code cell-by-cell and run them in order
- Step 4: The model should automatically run (give it anywhere from 5-10 mins to fully train and run)
- Optional anytime: Check 'EnviroSort.ipynb' for a sample of what the Colaboratory should like when you are done.

## Inspiration
The inspiration behind EnviroSort stemmed from the pressing waste management issues in our country. The improper disposal of waste leading to overflowing landfills, eutrophication, and pollution of land, water, and air deeply concerned us. The harmful effects of toxic waste consumption by animals highlighted the urgency to find innovative solutions to reduce waste and promote a healthier environment.


## What it does
EnviroSort addresses waste management challenges by automating the waste sorting process using cutting-edge technologies. By utilizing IoT and machine learning, the platform segregates household waste into two classes: organic and recyclable. This automated sorting process significantly reduces the amount of toxic waste ending up in landfills, mitigating the negative environmental impacts associated with improper waste disposal.

## How we built it
Building EnviroSort was a multi-faceted endeavor that involved the innovative use of cutting-edge technologies and the collaboration of a skilled team. Here's an overview of the key components and techniques used:

- **Data Collection and Analysis**: We looked through Kaggle for an appropriate dataset until we found one [here](https://www.kaggle.com/datasets/techsash/waste-classification-data).

- **Convolutional Neural Networks (CNN)**: CNNs are powerful deep learning models for image classification. We employed a pre-trained VGG16 model as the backbone of our waste classification system, leveraging its ability to extract meaningful features from images.

- **Transfer Learning**: To expedite the training process and optimize model performance, we utilized transfer learning. By reusing pre-trained weights from VGG16, we initialized our model with valuable knowledge about image features, enabling us to train on a smaller dataset effectively.

- **Data Augmentation**: To improve model generalization, we applied data augmentation techniques like rotation, shearing, and flipping to artificially expand our training dataset.

- **Model Fine-Tuning**: We fine-tuned the pre-trained VGG16 model on our waste classification task, customizing it to accurately distinguish between organic and recyclable waste items.

- **Model Evaluation**: Rigorous model evaluation using various performance metrics helped me ensure the effectiveness and reliability of EnviroSort.

- **Continuous Testing and Refinement**: Frequent testing and validation allowed me to identify and address potential issues and continually enhance the accuracy and efficiency of EnviroSort.

## Challenges we ran into
Some challenges I ran into while making EnviroSort:

- **Lack of computing resources**: My laptop I have does not have the resources to train the CNN model I used, despite all the cost-cutting I did in terms of computing resources. I even tried to let my laptop GPU be utilized through NVIDA CUDA and cuDNN but TensorFlow, the library I was using for the model, would'nt recognize it despite hours of trying to get it to work. Eventually I gave up working locally and moved to Google Colaboratory, where I had to settle for the GPUs Google would provide for free.

- **Creating and Training the Model**: As mentioned above, this process was very consuming in terms of resources, and therefore meant that I could only run so many tests to debug. Even to make the slightest changes to see what it would do to the model accuracy would take another 10-20 min. This time quickly stacked up, and before long, the process got annoying and frustrating, especially when the running would crash at a halfway point randomly (Google Colab disconnects runtime randomly). 

## Accomplishments that we're proud of
- I am proud that despite facing many challenges, I was able to create, train, and validate a Sequential model (my first time!) that could work on the data set. 

- I am also proud that the model itself did relatively well across the board (85% - 90%) accurate, although I was hoping for a bit more than that. 

## What we learned
- I learned how to create, add layers, train, and validate a Sequential model using the Keras API
- I learned about common machine learning struggles and data scientist debugging strategies

## What's next for EnviroSort
- I hope to mess around with the layers, try to see if I can get a higher accuracy
- I hope to add a physical component (Arduino maybe) so that I can add an actual sorting process where I can test organic and recyclable waste and see how well the algorithm and the physical component work together to create a cohesive sorting mechanism
