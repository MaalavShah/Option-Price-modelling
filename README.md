# Option Pricing Models

## Introduction  
This is a repository to use simple models for calculating option prices (European Options). It uses three different methods for option pricing:  
1. Black-Scholes model    
2. Monte Carlo simulation    
3. Binomial model    

Each model has various parameters that user needs to import:  

- Ticker  
- Strike price  
- Expiry date  
- Risk-free rate  
- Volatility  

Option pricing models are implemented in [Python 3.7](https://www.python.org/downloads/release/python-377/). Latest spot price, for specified ticker, is fetched from Yahoo Finance API using [pandas-datareader](https://pandas-datareader.readthedocs.io/en/latest/). Visualization of the models through simple web app is implemented using [streamlit](https://www.streamlit.io/) library.  

When data is fetched from Yahoo Finance API using pandas-datareader, it's cached with [request-cache](https://github.com/reclosedev/requests-cache) library is sqlite db, so any subsequent testing and changes in model parameters with same underlying instrument won't result in duplicated request for fethcing already fetched data.

This implementation was done as project work on the course [Special Functions (Applied Mathematics)](https://www.etf.bg.ac.rs/en/fis/karton_predmeta/13M081SPEF-2013) on Master's degree in Software Engineering.

## Project structure  
In this repository you will find:  

- demo directory - contains .gif files as example of streamlit app.  
- option_pricing package - python package where models are implemented.  
- option_pricing_test.py script - example code for testing option pricing models (without webapp).  
- streamlit_app.py script - web app for testing models using streamlit library.   
- Requirements.txt file - python pip package requirements.  
- Dockerfile file - for running containerized streamlit web app.  
- app.yaml file - for deploying dockerized app on GCP(Google Cloud Platform).  




 



