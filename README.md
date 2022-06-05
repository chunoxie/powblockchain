**Activate the virtual environment**
```
cd powblockchain
python3 -m venv blockchain-env

source blockchain-env/Scripts/activate - for Windows
source blockchain-env/bin/activate - for Linux
```

**Install all packages**
```
pip3 install -r requirements.txt
```

**Run the tests**
```
Ensure virtual environment is activated
python3 -m pytest backend/tests

If test is giving error esp in Windows, check various python installations 
where python 
(on the cmd to see all installations and go install pytest in those various locations where pip, pip3, etc exist but not py.test and pytest)

You may google how to set environment variables for Python in order to align your Windows package installations and not do multiple installs of same package across wherever Python is
```

**Flask Installation**
```
Ensure to install Flask (with specific version number if required) in the virtual environment
pip3 install Flask

Confirm installations in the virtual environment with 
pip3 freeze

If Flask test is giving error esp in Windows, check various python installations using
where python 
(on the cmd to see all installations and go install Flask in those various locations where pip, pip3, etc exist but not py.test and pytest)
```

**Run the application and API**
Make sure to activate the virtual environment.
```
python3 -m backend.app
```

**Install PubNub**
```
pip3 install pubnub
Remember to have active virtual environment and to sort out Windows issue as usual
```

**Run a peer instance**
Make sure to activate the virtual environment.

```
export PEER=True && python3 -m backend.app
```

**For Testing the backend app**
```
1. change to python-blockchain directory
2. source blockchain-env/Scripts/activate (activate virtual environment)
3. python -m backend.app (start the root app)
4. export PEER=True && python -m backend.app (start one or more peer instances of the app)
5. python -m backend.scripts.test_app (initiate live simulation of entire app across all instances)
6. python -m pytest backend/tests (for unit and functionality integration tests of the app)
```

**Run the frontend**
In the frontend directory:
```
npm run start
```

**Seed the backend with data**
Make sure to activate the virtual environment.
```
export SEED_DATA=True && python -m backend.app
```
