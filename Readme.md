# TECHIN 510 Lab 1

A personal website for TECHIN 510 Lab 1.

## How to Run

Open the terminal and run the following commands:

```
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## What's Included

- `app.py`: The main Flask application

## Lessons Learned
- Write gitignore file in the directory
- How to install virtual environment
  - there might be many errors and wierd bugs(for windows, we need to use gitbash as terminal. In addition, check the python version you installed)
- How to use Streamlit to create a simple website
  - card with image and texts
  - insert emoji
- How to use requirements.txt to manage Python dependencies
  - type streamlit in `requirements.txt`
- How to use GitHub Actions to deploy a website to Azure App Service
  - build and deploy (if there is any error, retry the jobs in github)
  - configuration on azure (link the account and repository) 

## Questions / Uncertainties

- What if I want to make the profile picture round?
  - We can use `<style>` tag defines CSS rules within the Streamlit app, applying properties like width, height, and border-radius to create a circular container with a subtle box shadow.

- How to use a two column layout?
  - We can use the function `st.columns(2)` in each section to make two column layout. For example:
   ```
   col1, col2 = st.columns(2)
   ```