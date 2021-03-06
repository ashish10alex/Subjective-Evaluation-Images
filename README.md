# Subjective evaluation comparing images
This repository is inspired from [Webmushra](https://github.com/audiolabs/webMUSHRA) with [Pymushra](https://github.com/nils-werner/pymushra) which provides a python based backend to store results. 

This project has following key modifications from above repository to accomodate it for our AB testing experiments. 
 * Completely port to Flask based development. 
 * No need for separate WebMushra directory -  Javascript dependencies have been added to `static` folder
 * Key entry point for web app assuming `web-drone-project/pymushra/pymushra` as root is  is -> `service.py -> templates/index.html -> static/startup.js` 



##  Setup steps

Please skip to bullet point 2 as I have already generated these meta data files. 


<h3>1.  Meta data Genration </h3> 
To generate `yaml` files have a look at - `meta_data.py`

<h3>2. Run the server locally </h3> 

    ```
    git clone https://github.com/ashish10alex/Subjective-Evaluation-Images.git
    cd Subjective-Evaluation-Images
    python3 -m venv .
    source bin/activate
    pip install -e pymushra
    pymushra server 

    ```
    Then open `http://localhost:5000`

<h3>3.  Database </h3>

* But the main database which we will use for evaluating results is in the root of the repository -  `database_baseline_vs_noisy.csv` and `database_other_model_combinations.csv`

* To view the results for each subset can be viewed by switching btw dropdown menus - [Error handling TBD]
   * `http://localhost:5000/result` 
 

<h2>4.  Monitor Experiments </h2>

* You can monitor the finished and remaining experiments at - `http://localhost:5000/finished`




