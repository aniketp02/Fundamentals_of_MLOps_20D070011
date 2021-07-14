# Part 1

## GitHub repository:

[MLOps_Assignment](https://github.com/aniketp02/MLOps_Assignment/tree/main)

## Steps for Part 1:

- To initialize the MLOps_Assignment repository as DVC repository
<pre><code>dvc init</code></pre>

- Setting the external_cache folder outside this repo as cache for this repository
<pre><code>dvc cache dir relative/path/to/external_cache</code></pre>

- Enabling dvc tracking for creditcard.csv file
<pre><code>dvc add data/creditcard.csv</code></pre>

- Tracking the .dvc file using git and ignoring the .csv file
<pre>
<code>
git add data/creditcard.csv.dvc data/.gitignore
git commit -m "raw data added"
</code>
</pre>

- Setting the S3 bucket as default for DVC repo
<pre>
<code>
dvc remote add -d storage s3://bucket_name/datastore

git add .dvc/config
git commit -m "configure remote storage"
</code>
</pre>

- Uploading the dataset to datastore folder
<pre><code>dvc push</code></pre>

## Values of Accuracy & Weighted F1 Score

### For Decision Tree Classifier

- #### Accuracy: 99.9104 %
- #### Weighted F1 Score: 99.9102 %

### For Random Forest Classifier

- #### Accuracy: 99.9315 %
- #### Weighted F1 Score: 99.9274 %