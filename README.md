# Python Trading Robot

## Table of Contents

- [Overview](#overview)
- [Setup](#setup)
- [Usage](#usage)


## Overview

Current Version: **0.1.1**


The bot is designed to mimic a few common scenarios:
   
 1.  The Python-coded trading robot is capable of executing automated strategies using technical analysis, and is designed to emulate a variety of common situations. One such situation involves managing a portfolio of multiple financial instruments, with the Portfolio feature providing risk metrics and real-time feedback during trades.

2. Another feature, the Trade object, enables the definition of both simple and complex orders using Python, thus simplifying common scenarios like the simultaneous definition of take profit and stop loss orders.

3. The bot also incorporates a real-time data table that contains historical and updated prices. The StockFrame feature facilitates the storage and retrieval of financial data for analysis purposes.

4. Finally, the Indicator feature enables the definition and calculation of indicators based on both historical and real-time prices. It provides an easy means of specifying input, performing calculations, and updating values as new prices become available. All of these features work together to create an efficient trading tool.




Regenerate response

## Setup

**Setup - Local Install:**

If you are planning to make modifications to this project or you would like to access it
before it has been indexed on `PyPi`. I would recommend you either install this project
in `editable` mode or do a `local install`. For those of you, who want to make modifications
to this project. I would recommend you install the library in `editable` mode.

If you want to install the library in `editable` mode, make sure to run the `setup.py`
file, so you can install any dependencies you may need. To run the `setup.py` file,
run the following command in your terminal.

```console
pip install -e .
```

If you don't plan to make any modifications to the project but still want to use it across
your different projects, then do a local install.

```console
pip install .
```

This will install all the dependencies listed in the `setup.py` file. Once done
you can use the library wherever you want.

**Setup - PyPi Install:**

The project can be found at PyPI, if you'd like to view the project please use this
[link](https://pypi.org/project/python-trading-robot/). To **install** the library,
run the following command from the terminal.

```bash
pip install python-trading-robot
```

**Setup - PyPi Upgrade:**

To **upgrade** the library, run the following command from the terminal.

```bash
pip install --upgrade python-trading-robot
```

## Usage

To run the robot, you will need to provide a few pieces of information from your TD Ameritrade Developer account.
The following items are need for authentication:

- Client ID: Also, called your consumer key, this was provided when you registered an app with the TD Ameritrade
  Developer platform. An example of a client ID could look like the following `MMMMYYYYYA6444VXXXXBBJC3DOOOO`.

- Redirect URI: Also called the callbakc URL or redirect URL, this was specified by you when you regiestered your app with
  the TD Ameritrade Developer platform. Here is an example of a redirect URI <https://localhost/mycallback>

- Credentials Path: This is a file path that will point to a JSON file where your state info will be saved. Keep in mind
  that it is okay if it points to a non-existing file as once you run the script the file will be auto generated. For example,
  if I want my state info to be saved to my desktop, then it would look like the following: `C:\Users\Desktop\ts_state.json`

Once you've identfied those pieces of info, you can run the robot. Here is a simple example that will create a new instance
of it:

```python
from pyrobot.robot import PyRobot

# Initialize the robot
trading_robot = PyRobot(
    client_id='XXXXXX111111YYYY22',
    redirect_uri='https://localhost/mycallback',
    credentials_path='path/to/td_state.json'
)
```

For more detailed examples, go to the `trading_robot.py` file to see an example of how to use the library along with all
the different objects inside.


