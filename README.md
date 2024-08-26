Visual Question Answering Application:

Welcome to the Visual Question Answering Application! Below are the steps to install the project and a description of the folder structure.

Before You Begin
Ensure you have the following software installed on your system:
Python 3.x
Git
Virtualenv (optional but recommended)



Create and Activate a Virtual Environment (Optional but Recommended)
On Windows:
python -m venv env09
env09\Scripts\activate

On macOS/Linux:
python3 -m venv env09
source env09/bin/activate


Install Dependencies:
pip install -r requirements.txt
This will install all the required Python packages listed in requirements.txt.


Setting Up Environment Variables
To use the OpenAI API, you'll need to set up an environment variable for your OpenAI API key. Create a file named .env in the root directory of the project and add the following line:

OPENAI_API_KEY=your_openai_api_key_here
Replace your_openai_api_key_here with your actual OpenAI API key.


Run the Application: 

python src/RAG.ipynb
Or open the notebook file in Jupyter Notebook or VS Code and run the cells.

Folder Structure
The project is organized as follows:


projectname/
│
├── env09/                   # Virtual environment folder (optional and not included in source control)
│
├── data/                    # Directory containing input data files
│   ├── Coding_challenge_source_1.pdf   # Source PDF for the coding challenge
│   ├── Coding_challenge_source_2.pdf   # Another source PDF for the coding challenge
│
├── src/                     # Source code for the project
│   └── RAG.ipynb            # Main Jupyter Notebook file for the project
│
├── test/                    # example output 
│
├── .gitignore               # Specifies files and directories to be ignored by Git
├── README.md                # Project overview and installation guide
├── .env                     # Environment file for storing sensitive API keys (not included in source control)
└── requirements.txt         # Python dependencies for the project

Key Directories and Files
env09/: This is the virtual environment directory, which contains all the dependencies installed for the project. It's optional and should not be included in version control.
data/: This directory contains input data files, such as PDFs or datasets, that are used in the project.
src/: Contains the main source code. The RAG.ipynb file is the Jupyter Notebook where the main code is written and executed.
.gitignore: A file specifying which files and directories Git should ignore (e.g., the virtual environment folder and .env file).
README.md: The file you are currently reading, which provides an overview and installation instructions for the project.
.env: This file is used to store environment variables, such as the OpenAI API key. Ensure it is added to your .gitignore.
requirements.txt: Lists all the Python packages required to run the project. Install these dependencies using pip install -r requirements.txt.


Usage
After installation, you can start using the project by running the main Jupyter Notebook (RAG.ipynb). You can modify the paths and parameters as needed based on your requirements.