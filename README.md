---

# AXPO_TRADING

---

## Environment configuration:

### 1. **Git Bash** - clone repo from GitHub:
- 1.1 git clone https://github.com/dkaszynski/AXPO_TRADING.git
- 1.2 cd AXPO TRADING

### 2. **Anaconda prompt** - create conda environment:
- 2.1 conda create -n axpo_trading python=3.8
- 2.2 conda activate axpo_trading

### 3. **PyCharm** - create project in PyCharm with configured conda environment:
- 3.1 File
- 3.2 New Project
- 3.3 Set location e.g. D:\GitHub\AXPO_TRADING
- 3.4 Previously configured interpreter
- 3.5 Conda Environment
- 3.6 ...\axpo_trading\python.exe
- 3.7 Ok 
- 3.8 Create
- 3.9 Create from existing sources
- 3.10 This window

### 4. **Anaconda prompt** - install packages in conda environment:
- 4.1 cd ../AXPO TRADING
- 4.2 conda install --file requirements.txt

---

## Repository:

### 5. **GitHub** - branches structure:
- 5.1 - Main - production branch
- 5.2 - Dev - development branch
- 5.3 - Feature - feature branch (name format: {*developer_name.title()*}_{*branch_developer_id*}_{*feature_description*} e.g. *Adam_1_pse_data_scrapper* 
- 5.4 Branches dependencies: Feature -> Dev -> Main
- 5.5 create new branch from Dev branch: 
  - git checkout -b brach_name
- 5.6 rebase branch: 
  - git fetch origin Dev:Dev
  - git rebase Dev
  - code version selection
  - git add .
  - git rebase --continue
  - code version selection
  - git add .
  - git push -f origin branch_name

### 6. **Git Bash/ PyCharm** - commits:
- 6.1 commit add .
- 6.2 git commit -m "commit description" # meaningful commit's description; "wip/./sth" not accepted!
- 6.3 git push origin feature branch e.g. git push origin adam_1_pse_data_scrapper 

### 7. **GitHub** - pull Requests:
- 7.1. PR description as point list required
- 7.2. Assign *Adam Nowacki* as **required reviewer**, rest developers as **optional reviewers**
- 7.3. Merge from Feature into Dev accepted when PR received approve vote and all comments/threads are resolved

---

## Python:

### 8. **PyCharm** - docstring format:
- 8.1 Function:
```
def function(x, y, z):
    """
    Function calculates weighted rolling mean
    Arguments:
        x: pd.DataFrame
        y: int
        z: str
    Returns:
        Function returns pd.DataFrame with calculated weighted rolling means
    """
    
    # code block
    
    return ...
```
- 8.2 Class:
```
class Class:
    """
    Class builds Pyomo optimization model
    Arguments:
        x: pd.DataFrame
        y: int
        z: str
    """
    
    def __init__(self, ...):
        self.x = x
        self.y = y
        self.z = z
        
    def method(self, sense, solver):
        """
        Method starts Mixed Integer Linear Programming optimization model 
        Arguments:
            sense: str ["minimize", "maximize"]
            solver: str ["glpk", "cbc", "cplex", "ipopt"]
        Returns:
            Optimized transportation delivery schedule
        """
        
        # code block
        
        return ...
```

### 9. **PyCharm** - typing:
- 9.1 Build-in types
- 9.2 Package *typing*
```
def function(tbl: pd.DataFrame,
             n: int, 
             type: str) -> pd.DataFrame:
    """
    docstring
    """
    
    # code block
    
    return tbl
```

### 9. **PyCharm** - logging:
```
def function():
    """
    docstring
    """

    logging.info("")    
    logging.warning("")
    logging.debug("")
    logging.error("")
    logging.critical("")
    
    # code block
    
    return ...
```

---

## Other:

### 10. **Anaconda prompt** - useful conda commands:
- 10.1 conda list - display installed packages in environment

### 11. **PyCharm** - useful tips:
- 11.1 ```# !TODO(AN)``` - to do author notes in code
- 11.2 Reformat .py file according to PEP-8: ctrl+A -> ctrl+shift+alt+L -> enter

---
