# NLP Crash Course - Reddit Shower Thoughts Generator!

This project leverages the GPT 2 model to generate "showerthoughts" similar to the content of the subreddit "r/ShowerThoughts"

## Dataset 

Using the `pmaw`module in python, 170k subreddit posts were scraped from the  "r/ShowerThoughts" subreddit from dates 1st Jan 2022 to 19th May 2022. 


## The Model 

A fintuned GPT 2 model was first implemented. However,since the GPT2 model in itself was trained on longer form texts , the results of the finetuned model was less than ideal with a lower BLEU score. So a custom tokenizer was trained and a new model was implemented which gave a better bleu score and favourable results. 



## Deployment 

The model was deployed as a flask app and hosted on the cocalc server. 

![Main Page](https://github.com/ghoshdebapratim1/shower-thoughts-generator/blob/main/app/static/img/main1.PNG)
![Project Features ](https://github.com/ghoshdebapratim1/shower-thoughts-generator/blob/main/app/static/img/main2.PNG)
![Team](https://github.com/ghoshdebapratim1/shower-thoughts-generator/blob/main/app/static/img/main3.PNG)
![Model](https://github.com/ghoshdebapratim1/shower-thoughts-generator/blob/main/app/static/img/model1.PNG)

### File Structure


- .gitignore
- config.py
- Dockerfile
- READMD.md
- entrypoint.sh
- nginx_host
- host_config
- app/
     - **main.py**
     - *requirements.txt*
     - **utils.py**
     - templates/
          - **writer_home.html**
          - **Write-your-story-with-AI.html**
     - static/
          - **img/** 
          - **js/**
          - **css/**
          - favicon.ico  
     - model/
          - **TODO.txt** <- delete this file after following the directions. Important to note that you will only need an aitextgen.tokenizer.json file if you are custom training your own tokenizer and model.

## To Execute the Model 

In order to execute the model, you need to save the files given in https://drive.google.com/drive/folders/1C9cumPolIOWsmmkJy_gJAOAj7_ak4UsM?usp=sharing in the model folder. 
Run main.py in the project directory and then go to the hosted link. 

## Note 

This project was done as part of the NLP crash course for AI Camp

