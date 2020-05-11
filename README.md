# Privately Application Project

## I - General information

This project consists in fine-tuning a MobileNetV2 model to do a classification task with 6 labels.
The dataset used in the context of this project is the Intel Image Classification dataset, downloaded from the following link : https://www.kaggle.com/puneet6060/intel-image-classification

The project was carried out using *Keras* framework.

In order to run the whole notebook, the following libraries are needed:
- *keras*
- *numpy*
- *pandas*
- *sklearn*
- *matplotlib*
- *plotly*
- *itertools*
- *shutil*
- *os*
- *csv*

Moreover, to run the notebook, it is required to download the dataset and extract it in the **same folder** as the notebook and the *grid_search.csv* file.
Unfortunately, to visualize the interactive plots made with *Plotly*, it is required to run the notebook on a jupyter environment. The plots cannot be visualized through the notebook on *Github*.

Due to insufficient computational power, the dataset was shrunk by a factor of 4 for the context of this project. **Do not run** the cell which calls the shrink() function if you have sufficient computational power. With the train data shrunk by a factor of 4 and using a GPU for the computations, a single training over 30 epochs took almost 10 minutes, and the implemented grid-search algorithm took over 3 hours to run.

## II - Final performance

The final model managed to attain a validation accuracy of 87%. All of the steps that were taken in order to achieve this are shown in the notebook, with comments and observations. The *grid_search.csv* file shows the histories of trainings generated during the execution of the grid-search algorithm.

## III - Prospects for improvement

More computational power would have allowed to run a more complex grid-search over more epochs. Empirical tests were carried out to choose the set of values for each hyper-parameters for the grid-search algorithm. It seems like an even smaller learning rate over more epochs may have resulted in a better model. Moreover, it would have been more accurate to run the grid-search algorithm combined with a cross-validation for the hyper-parameter tuning. However, due to the lack of time and computational power, these weren't performed in the context of this project.

Another prospect for improvement would be to train not only the last layer but the ones preceding it as well. This could lead to a better fitting. 