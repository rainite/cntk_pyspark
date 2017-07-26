
# Walkthrough: Scoring a trained CNTK model with PySpark


This notebook demonstrates how a trained [Microsoft Cognitive Toolkit (CNTK)](https://github.com/Microsoft/CNTK/wiki) deep learning model can be applied to files in a distributed and scalable fashion using the [Spark Python API](http://spark.apache.org/docs/2.1.0/programming-guide.html) (PySpark). An image classification model pretrained on the [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html) dataset is applied to 10,000 withheld images. A sample of the images is shown below along with their classes:

<img src="https://cntk.ai/jup/201/cifar-10.png" width=500 height=500>



## Source code

Please see the file 'CNTK_model_scoring_on_Spark_walkthrough.ipynb'.

## Docker hub link

https://hub.docker.com/r/rainite/cntk_with_spark_final/

This docker has installed all of the required models and can execute on a built-in jupyter notebook.
After instance, type these 2 set-up command lines to run the jupyter notebook.
```shell
docker run -d -p 8888:8888 --name cntk-jupyter-notebooks -t cntk_with_spark_final  
```
```shell
docker exec -it cntk-jupyter-notebooks bash -c "source /cntk/activate-cntk && jupyter-notebook --no-browser --port=8888 --ip=0.0.0.0 --notebook-dir=/cntk/Tutorials --allow-root"
```

