# AXPO_TRADING

---

### Clone repo from GitHub:
1. **Git Bash**:
- 1.1 git clone https://github.com/dkaszynski/AXPO_TRADING.git
- 1.2 cd AXPO TRADING

### Create conda environment:
2. **Anaconda prompt**:
- 2.1 conda create -n axpo_trading python=3.8
- 2.2 conda activate axpo_trading

### Create project in PyCharm with configured conda environment
3. **PyCharm**:
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

### Install packages in conda environment
4. **Anaconda prompt**
- 4.1 cd ../AXPO TRADING
- 4.2 conda install --file requirements.txt

### Branches structure:
5.1 - Main - production branch
5.2 - Dev - development branch
5.3 - Feature - feature branch (name format: {developer_name}_{branch_id}_{feature_description} e.g. adam_1_pse_data_scrapper 
5.4 Feature -> Dev -> Main

### Commits in Git Bash/ PyCharm:
6.1 commit add .
6.2 git commit -m "commit description" # meaningfull commit's description; "wip/./sth" not accepted!
6.3 git push origin feature branch e.g. git push origin adam_1_pse_data_scrapper 

### Pull Requests:
7.1. PR description as point list required
7.2. Assign Adam Nowacki as required reviewer, rest developers optional
7.3. Merge from Feature into Dev accepted when PR received approve vote and all comments/threads are resolved

### Usefull conda commands:
conda list - display installed packages in environment