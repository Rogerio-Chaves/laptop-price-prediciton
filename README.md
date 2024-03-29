# Laptop Price Prediciton

![Laptop Price Prediciton](/imgs/laptop-homepage.jpg "Laptop Price Prediciton")

## Description:

This project aim to predict the laptop price. For this it use the [Laptop Price Dataset](https://www.kaggle.com/datasets/muhammetvarl/laptop-price) available on Kaggle. The dataset contains 1303 instaces with 12 columns (11 features and 1 target).

**Columns:**

`Company:` Laptop Manufacturer</br>
`Product:` Brand and Model</br>
`TypeName:` Type (Notebook, Ultrabook, Gaming, etc.)</br>
`Inches:` Screen Size</br>
`ScreenResolution:` Screen Resolution</br>
`Cpu:` Central Processing Unit (CPU)</br>
`Ram:` Memory RAM</br>
`Memory:` Hard Disk / SSD Memory</br>
`GPU:` Graphics Processing Units (GPU)</br>
`OpSys:` Operating System</br>
`Weight:` Laptop Weight</br>
`Price_euros:` Price (Euro)

**Dataset author:** Muhammet Varli.

## Project Structure:

	├── data <- Folder containing the dataset used in the project.
		└── laptop_price.csv <- full dataset.
		│
		└── test.csv <- Test dataset used in the predict step.
	│ 
	├── imgs <- Folder containing images used in the README file.
	│ 
	├── model <- Folder containing the model files.
		│
		└── cpu_encoder.bin <- CPU label encoder.
		│
		└── gpu_encoder.bin <- GPU label encoder.
		│
		└── memory_encoder.bin <- Memory label encoder.
		│
		└── model.bin <- The trained model.
		│
		└── product_encoder.bin <- Product label encoder.
		│
		└── relevant_columns.bin <- Relevant columns generates of the feature selection step.
		│
		└── resolution_encoder.bin <- Resolution label encoder.
		│
		└── results.txt <- Results of the model training.
		│
		└── typename_encoder.bin <- Typename label encoder.
	│ 
	├── Pipfile <- File for the virtual environment.
	│ 
	├── Pipfile.lock <- File for the virtual environment.
	│ 
	├── README.md
	│ 
	├── notebook.ipynb <- This notebook contains the preprocessing, EDA and model selection.
	│ 
	├── requirements <- This file contains the library dependencies of the project.
	│ 
	├── train.py <- Python script for the training step.


## How to run this project:

### Get the dataset

There are two ways to get the dataset:

- Original is available on the Kaggle in this <a href="https://www.kaggle.com/datasets/muhammetvarl/laptop-price">link</a>.
- Data folder in this repository.

### Activate the virtual environment

Open the terminal in the repository and set the command.

<code>pip3 install pipenv</code>

Install the libraries dependencies.


<code>pipenv lock</code> Get the dependencies of the requirements.txt file.

<code>pipenv install</code> Install the dependencies.

<code>pipenv shell</code> Active virtual environment.

#### Notebook file:

With virtual environment activated, running the following command will create a kernel that can be used to run jupyter notebook commands inside the virtual environment.

<code>ipython kernel install --user --name=venv</code>

Finally, select the <b>venv</b> kernel in the notebook interface.

#### Training Script file:

With virtual environment activated, run the train script using this command <code>python3 train.py</code>

#### Predict web service:

With virtual environment activated, build the dockerfile using this command<code>sudo docker build -t predict .</code>

Finally, run docker with this command <code>sudo docker run -it -p 9696:9696 predict:latest</docker>

## Colaborators:

`Rogerio Chaves`
