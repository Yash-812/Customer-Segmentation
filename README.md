**Customer Segmentation**

Customer Segmentation is the subdivision of a market into discrete customer groups that share similar characteristics. Customer Segmentation can be a powerful means to identify unsatisfied customer needs.

--> Environment and tools

  •	scikit-learn
  
  •	seaborn
  
  •	numpy
  
  •	pandas
  
  •	matplotlib

Here I am using mall customer dataset to understand customer behavior. We are going to build a clustering model on historic data. Using this model we can predict the behavior of the new customer.
Let’s build our model using k-means clustering.
1.	Import Libraries
We need to import all the required libraries
 ![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/9fc33095-7216-49e7-a596-1a525075c3e6)

2. Get the data
![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/a35c1f9c-7f58-41f6-8c3c-e74a016d3891)

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/c49798bc-d16a-4b49-a91d-3a1e9cb6aee3) 
Getting the dataset is not enough. We have to perform exploratory data analysis.

3. Perform Exploratory Data Analysis
I have performed some initial analysis of this data. In this article, we will not more focus on EDA.
![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/b7723d3f-ead3-4fbc-915c-d2b8033dc086)

4. Model Building
Now it’s time to cluster the data. Here we are clustering our data using k-means.
We are clustering our data based on annual income and spending scores. For our dataset, we are using the elbow method to find the optimum number of clusters.

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/0f4fdf8b-768c-4469-b488-d8819a74ffe7)

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/a612bc35-3735-4daf-b62f-52d3b0e2c622)

Based on the elbow method, we could choose k=3 or 5. Let us try k=5 and visualize the clusters.

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/197954a0-5dbb-42fa-9229-b70b0a299ad2)

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/70fd314b-db5c-41e2-a12c-875d39cdacee)

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/d3dae709-06a9-4fcd-9f78-01ea915cb6e7)

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/00a7112d-eaef-4b4d-8f9a-0e459fe85e83)

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/90942ffe-079f-4834-88ab-0cb7421c66d1)

The above plot shows the distribution of the 5 clusters. We can interpret them as the following:

Cluster1: Cluster 1 contains the customers with medium annual income and medium annual spend

Cluster2: Cluster 2 contains the customers with medium to high annual income and low annual spend

Cluster3: Cluster 3 contains the customers with low annual income and low annual spend

Cluster4: Cluster 4 contains the customers with low annual income and high annual spend

Cluster5: Cluster 5 contains the customers with medium to high annual income and high annual spend

5. Model Deployment using Flask
Now our simple k-means model is ready. Convert the python object model into a character string using the pickle module. Any object in Python can be pickled so that it can be saved on disk.
Save the above model as .pkl file

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/ba472a4d-dd89-476c-ab76-db09b493f2b0)
Now our model is saved in the directory where our notebook is stored.

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/b25c63c5-b590-44f0-9be4-3c3c0febe87d)
As of now, we developed a model i.e. model.pkl which can predict the behavior of the customer based on annual income and spending score.

Now as shown in below image, we can predict the cluster by filling the form. 
![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/aefdc746-5f82-451b-af86-b8efbf5637bb)

![image](https://github.com/Yash-812/Customer-Segmentation/assets/125514558/b0104127-6ddd-4397-8979-4d672e9eb175)


 
 


