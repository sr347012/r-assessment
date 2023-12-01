# r-assessment
Assessment for coursera

library(caret);
library(kernlab);

library (ggplot2);
# import and store the dataset in data1
testingData <- read.csv("pml-testing.csv", header=T);

# import and store the dataset in data1
trainingData <- read.csv("pml-training.csv", header=T);


modFit <- train(trainingData ~., method="rpart", data="training")

predict(modFit, newData=testingData)
