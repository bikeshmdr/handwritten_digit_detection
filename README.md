<h1>Dataset Source</h1>
    <p>This dataset is sourced from <a href =https://storage.googleapis.com/tensorflow/tf-keras-datasets/mnist.npz>mnist provided dataset<a>

<h1>Model Training</h1>
    <p>Neural network base <b>LeNet-5 model</b> and machine learning based <b>Random Forest Classifier</b> were trained for handwritten digit identification.</p>
    <ol>
        <li>LeNet-5 model</li>
            <ul>
                <li>After loading the dataset, images were reshaped to size of 28*28 with addition of channel dimension.</li>
                <li>Images were normalized to have pixel values between 0 and 1.</li>
                <li>Target digits are one hot encoded because it provides a clear, non-ordinal representation of classes that is well-suited for classification algorithms.</li>
                <li>Model is defined whose summary is shown below.</li>
                <img src= "documentation\images\summary.png" alt = "Model Summary" width = "600">
                <p>Model is trained using <b>adam</b> as optimizer <b>categorical_crossentropy</b> as loss function with implementation of <b>learning rate reduction and early stopping</b> to prevent model for overfitting. The training loss plot is shown below.<br>
                    <img src = "documentation\image\loss_accuracy_plot.png" alt = "Training loss and accuracy plot" width = "600">
                    Similarly, the confusion matrix during testing can also be observed below.
                    <img src = "documentation\images\confusion_matrix.png" alt = "Confusion matrix" width= "600">
                </p>
            </ul>
        <li>Random Forest Classifier</li>
            <ul>
                <li>After loading the dataset, images were flattened form 2d to 1d for random forest classifier</li>
                <li>Images were normalized to have pixel values between 0 and 1.</li>
                <li>Model was trained in loop with different n_estimators from the list [10, 50, 100, 200, 300]</li>
                <li>For comparison of model performance with different n_estimators training and testing accuracy were observed for each n_estimator, the graph can be observed below.</li>
                <image src = "documentation\images\accuracy.png" alt = "Model performance with different n_estimator" width = "500">
            </ul>
            <p>The saved model was also reimported and evaluation were performed.
    </ol>

<h1>Model Comparison</h1>
    <p>Various evaluation parameters were used to evaluate the models as shown below.</p>


<h1>Model Deployment</h1>
<p>The link to streamlit code is <a href =https://github.com/bikeshmdr/hand_written_digit_recognization_deployment.git>github.com<a></p>
<p>The deployed link for streamlit is <a href =https://handwrittendigitrecognizationdeployment-tvxd6hdgxq7nmpfw9tdpgf.streamlit.app>streamlit.io<a></p>


