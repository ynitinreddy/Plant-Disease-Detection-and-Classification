# Plant-Disease-Detection-and-Classification
This project involves the use of CNN to identify and classify plant diseases. 

We also create a website and a server to use the model.

The credit for building the entire project goes to the youtube channel "codebasics".

Setup for Python:
Install Python (Setup instructions)

Install Python packages

pip3 install -r training/requirements.txt
pip3 install -r api/requirements.txt
Install Tensorflow Serving (Setup instructions)
Setup for ReactJS
Install Nodejs (Setup instructions)
Install NPM (Setup instructions)
Install dependencies
cd frontend
npm install --from-lock-json
npm audit fix
Copy .env.example as .env.

Change API url in .env.

Setup for React-Native app
Go to the React Native environment setup, then select React Native CLI Quickstart tab.

Install dependencies

cd mobile-app
yarn install
2.1 Only for mac users
cd ios && pod install && cd ../
Copy .env.example as .env.

Change API url in .env.

Training the Model
Download the data from kaggle.
Only keep folders related to Potatoes.
Run Jupyter Notebook in Browser.
jupyter notebook
Open training/potato-disease-training.ipynb in Jupyter Notebook.
In cell #2, update the path to dataset.
Run all the Cells one by one.
Copy the model generated and save it with the version number in the models folder.
Running the API
Using FastAPI
Get inside api folder
cd api
Run the FastAPI Server using uvicorn
uvicorn main:app --reload --host 0.0.0.0
Your API is now running at 0.0.0.0:8000
Using FastAPI & TF Serve
Get inside api folder
cd api
Copy the models.config.example as models.config and update the paths in file.
Run the FastAPI Server using uvicorn For this you can directly run it from your main.py or main-tf-serving.py using pycharm run option (as shown in the video tutorial) OR you can run it from command prompt as shown below,
uvicorn main-tf-serving:app --reload --host 0.0.0.0
Your API is now running at 0.0.0.0:8000
Running the Frontend
Get inside api folder
cd frontend
Copy the .env.example as .env and update REACT_APP_API_URL to API URL if needed.
Run the frontend
npm run start
