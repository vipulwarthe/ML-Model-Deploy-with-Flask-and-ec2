## ML Model Deployment with Flask and AWS EC2 Instance
This is a demo project to better understand and build proficiency on how machine learning models can be deployed on production using Flask API and AWS EC2 Instance

This [article](https://usman186168.hashnode.dev/step-by-step-guide-to-deploying-ml-models-on-flask-web-application-with-aws-ec2-instance) is a well-detailed and self-explanatory on the deployment of the project, Kindly comment, like and share.

![](Life_expectancy_flask_frame_work.PNG)

### Introduction/Objectives
<p><strong>Life Expectancy.</strong>
<p>Life expectancy refers to the number of years a person is expected to live based on the statistical average. Life expectancy varies by geographical area and by era. In the Bronze age, for example, life expectancy was 26 years, while in 2010, it was 67 years. </p>
<p>The life expectancy for a particular person or population group depends on several variables such as their lifestyle, access to healthcare, diet, economical status and the relevant mortality and morbidity data.</p>
<p>However, as life expectancy is calculated based on averages, a person may live for many years more or less than expected. </p>



### Methodologies
1.	Data Cleaning.
2.	Exploratory data analysis
3.	Feature Engineering
4.	Machine Learning Pipeline with Algorithm
5.  Choosing the best ML Algorithm
6.  Pickle and dumping the model in the model folder
5.	Conclusion and visualization with Dash

### Environment, Tools and Libraries:
1.	Pandas for data manipulation <img src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white">
2.	Numpy for mathematical calculation and analysis <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white">
3.	Seaborn and Matplotlib for visualization and insights
4.	Python 3.9 Environment <img src="https://img.shields.io/badge/python-%2314354C.svg?style=for-the-badge&logo=python&logoColor=white">
5.	Jupyter and Microsoft Excel as tools <img src="https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white"> <img src="https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white" >
6. Sklearn for Machine Learning and preprocessing  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white">

### Project Structure
This project has six major parts :
1.  Data - This folder contains the training data used for building the Machine learning model
2.  model - This folder contains the pickle file for our Machine Learning model to predict life expectancy of a country based on training data in Data folder.
3. app.py - This contains Flask APIs that receives life expectancy details through GUI or API calls, computes the predicted value based on our model and returns it.
4. request.py - This uses requests module to call APIs already defined in app.py and dispalys the returned value.
5. static - This folder contains the CSS- styling sheets that is used to adjust content size, spacing, color and/pr add decorative features such as animations
6. templates - This folder contains the HTML template to allow user to enter life expectancy features and displays the predicted average life expectancy.


![](prediction.PNG)


## Create one ec2 instance with ubuntu 22.04/t2.medium/all-traffic/20gb storage and connect with vs code and run below commands:

## Update the required packages:

      sudo apt-get update && sudo apt-get upgrade -y
      
## Install python environment and activate the env      

      sudo apt install python3-venv -y
      python3 -m venv mlpro
      source mlpro/bin/activate

 ## Clone the GITHUB repository:
 
      git clone https://github.com/vipulwarthe/ML-Model-Deploy-with-Flask-and-ec2.git
      ls
      cd ML-Model-Deploy-with-Flask-and-ec2/
      
 ## Run the requirement file:     
 
      pip install -r requirement.txt 
      pip install chart-studio
      pip install catboost
      pip install xgboost
      sudo apt-get install libgomp1

## Run ipynb file and then run app.py file     

      python3 app.py
      
## you will connect your app with your instance DNS along with port 8080 on browser (paste below format in browser)

     ec2-34-202-233-140.compute-1.amazonaws.com:8080
