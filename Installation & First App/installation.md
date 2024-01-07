# Installation & Run First Time FastAPI project

To initialize a FastAPI project we need Python installed in our operating system. So we need to check first whether Python is installed in our OS or not.
To check the it we've to run the following command:

```
python --version
# OR
python3 --version
```

If Python is installed in our OS, then we need to check the PIP package manager is installed or not, and also need to check python-venv is installed or not.

```
# To check PIP package manager
pip --version
# OR
pip3 --version
```

If pip or python venv is not installed:

```
sudo apt update # in ubuntu or debian
sudo apt install python3-pip
# OR
sudo apt install python-pip

sudo apt install python-venv
```

After that we need to create our project folder. And continue with the following steps:

1. Go to the project folder and run the following command

   ```
   python3 -m venv .venv
   # OR
   python -m venv .venv
   ```

2. Now we need to activate the virtual environment

   ```
   source project-directory/.venv/bin/activate
   ```

3. After activating the virtual environment, we need to install fastapi and uvicorn

   ```
   pip3 install fastapi uvicorn
   # OR
   pip install fastapi uvicorn
   ```

4. So we've installed our necessary packages for our FastAPI application. Now we need to create our main/index file.

   ```
   touch main.py
   ```

5. Let's code a bit

   ```
   from fastapi import FastAPI

   app = FastAPI()

   @app.get('/')
   def __index__():
   return "Hello from Our First FastAPI project"
   ```

6. Run the project

   ```
   uvicorn main:app
   # OR in watch mode (it'll restart the server with updates automatically)
   uvicorn main:app --reload
   ```

**Note:** Every time to run again the project (server) after closing the IDE or restarting our OS, we need to repeat the step no 2 and step no 6. That is first we need to activate the virtual environment and then we've run the project.

That's it. We've learned how we can start with FastAPI for backend programming.

**#Happy_Learning**
