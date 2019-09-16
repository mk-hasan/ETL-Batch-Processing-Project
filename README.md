# Project Summary

1. Apply transformations to flight delays data using **spark-sql**
   * Upload csv or json data files into Bigquery partition tables from bucket
   * Create dataproc cluster 
   > gcloud dataproc clusters create spark-etl \
   > --scope=default,sql-admin
   > --initialization-actions=gs://dataproc-initialization-actions/jupyter/jupyter.sh,gs://dataproc-initialization-      actions/kafka/kafka.sh,gs://dataproc-initialization-actions/zookeeper/zookeeper.sh \
   > --master-machine-type n1-standard-2 \
   >   --num-workers 2 \
   > --worker-macine-type n1-standard-2 \
   > --worker-boot-disk-size 200 \
   > --image-version 1.2
   
   * Add actions like **Zookeeper** , **Kafka** and **Jupyter Notebook** to the cluster
   * Use jupyter notebook to transform the data using various spark sql query
2. Save the transformed data into Google **Bigquery** partitioned tables
3. Use **Google workflow** templates to automate the spark **ETL** batch processing jobs.
4. Use **Apache Airflow** to create DAG & automate batch processin

