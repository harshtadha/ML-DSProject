End to End Data Sciene Project

+ create folder and open folder in vs code 
(option - Cookiecutter  : without creating folder just go to vs code and run command
"cookiecutter https://github.com/audreyfeldroy/cookiecutter-pypackage"
 )

+ create virtual environment ( conda create -p venv python==3.9 ) and active it with ( conda activate venv/ )

+ create repo on git and follow step from there

+ go to git again and create .gitignore file from there , select for python so it automatically create .gitignore fille for python project and add (venv/) in that file.

+ create requirements.txt file --> pip install -r requiremnts.txt [ handle = ]

+ create setup.py --> copy paste from here and alter it ( handle there --> HYPEN_E_DOT='-e .' cz we add -e. in requirements.txt)

+ create template.py --> copy paste from folter and alter it (rename Project_name ) and run the command every time where you add and file or change something --> python template.py 

+ create logger.py --> copy paste from folter ( Generic code )

+ create exception.py --> copy paste from folter ( Generic code )

NOW START WITH DATA INJECTION

+ create database and table in MySql server
+ create a connection with database in Utils.py and also set credentials in .env
+ now create configs for Data_injection or in separate config file. ( create three atrifacts like raw , train, test )
+ initialize Data_injection from data_injection.py file. ( read and fetch data from database and fill data to csv in thoese three artifacts file - raw_data, train_data, test_data)

+++ DVC ( Data versoning control)- tracking the large datasets , working same as git but we git push only artifacts file in dvc , but pushing artifacts/raw.scv.dvc , artifacts/train.csv.dvc,  artifacts/test.csv.dvc which contains key of every datasets and key changes with dataset change so can track using key from git but track data using dvc.

pip install dvc
dvc init -> create two files around raw.csv (push dvc) , raw.csv.dvc(push git), .gitignore(push git)
dvc add artifacts/raw_csv
dvc commit -m 'raw data csv updated'   
git log --> every push of dvc can be found with push id 
git checkout push_id --> to redirect previous push
dvc checkout --> to come back to recent latest


+++ Data Exploration Analysis - EDA
- pd.read_csv()
- numeric and categorical data
- missing data / duplicate / unique count in column / check data types/ check statistic of data/ check various cate. in diff category column














Here is how to set it up step-by-step:

Option 1: Using Conda (Recommended by the Project)
The project documentation specifically mentions using Conda with Python 3.9. Open your terminal inside the project folder and run:

Create the environment:
conda create -p venv python==3.9 -y

Activate it:
conda activate venv/

Option 2: Using Standard Python (venv)
If you don't use Anaconda/Conda, you can use the built-in Python module:

Create the environment:
python -m venv venv

Activate it:

Windows: .\venv\Scripts\activate

Mac/Linux: source venv/bin/activate

Next Step: Install Dependencies
Once your environment is active (you should see (venv) in your terminal prompt), you need to install the libraries required for this specific project:

Update pip:
python -m pip install --upgrade pip

Install from requirements:
pip install -r requirements.txt

Note: The setup.py in this repo is designed to work alongside requirements.txt. By running the install command above, it will trigger setup.py (because of the -e . line usually found in these templates) and install the project itself as an editable package.





