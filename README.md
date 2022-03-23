# Clothing-Classification
In today's ease-oriented society, consumers prefer buying from the comfort of their homes rather than venturing local marketplace. This has made ecommerce a viable alternative for both retailers and consumers. By the day, as e-commerce gains traction, the quantity of goods offered for purchase grows as well. For such continuing demand, manual tagging of clothing articles, which come in so many kinds, has become incredibly hard. This is where an intelligent clothing classifier enters the equation.

## Dataset
The <a href="https://www.kaggle.com/datasets/agrigorev/clothing-dataset-full"> clothing dataset </a> been used for model training has over 5000 images of 20 different classes. However, images of some classes do not appear very often. So a total of 12 out of 20 clothing items are used for model training.

## Model Training
Pre-trained Xception model has been used for classifier training. The training process is initiated on the augmented images in batches of size 32. Each training batch undergoes 265 iterations. Final evaluation results are presented below.
```
266/266 [==============================] - 1326s 5s/step - loss: 0.1076 - accuracy: 0.9681
Training Loss: 0.107
Training Accuracy: 96.816%

23/23 [==============================] - 76s 3s/step - loss: 0.1608 - accuracy: 0.9376
Validation Loss: 0.161
Validation Accuracy: 93.762%
```

## Learning Curves
The training process continues for 20 epochs, each with 265 iterations. The ultimate training accuracy has been found to be 96.82%. It could be observed that the validation process also follows the same curve with an end accuracy of 93.76%. These accuracies have been accomplished with an input image of size 256×256 pixels. With the highest loss of 1.0210 during first epoch, the classifier has managed to minimize it up to 0.1292 at the end of 20th epoch.
<p align="center">
  <img src="https://github.com/rimshasaeed/Clothing-Classification/blob/main/results/performance.jpg", alt="learning curves" width="50%" height="50%">
</p>

## Performance
Model performance on unseen images has been found to be quite impressive.
```
23/23 [==============================] - 111s 5s/step
Test Accuracy: 89.75%
```
<p align="center">
  <img src="https://github.com/rimshasaeed/Clothing-Classification/blob/main/results/classification%20report.jpg", alt="classification report" width="60%" height="60%">
</p>
