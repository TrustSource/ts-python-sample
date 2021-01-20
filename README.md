![Supported Versions](https://img.shields.io/badge/Python-3.6,%203.7,%203.8,%203.9-blue) 
![License](https://img.shields.io/badge/License-Apache--2.0-green)

# TrustSource Python sample project 

Sample [TrustSource](https://app.trustsource.io/) integration of a minimal Python application based on the popular web application framework [Flask](https://flask.palletsprojects.com).  

# Getting started / set up

The minimal application is created using the official Flask tutorial available at [Quickstart - A Minimal Application](https://flask.palletsprojects.com/en/1.1.x/quickstart/#a-minimal-application).

This example is based on Python 3, we recommend to use at least python 3.6. For package management we use pip together with virtual environments.  

```
# clone a repo
git clone https://github.com/trustsource/ts-python-sample
cd ts-python-sample
```

Now we create a virtual envorinment for the project and activate it:

```
# create a virtual environment
python3 -m venv ./venv
# activate the newly created environment
source venv/bin/activate
```

Install required software:

```
# install Flask and the TrustSource scanner
pip install -r requirements.txt
```

Ensure that the web application works (press CTRL-C to terminate the application):

```
# run web application
export FLASK_APP=hello.py 
python -m flask run
```


# Scan and dependency analysis

Now, we can scan the application for licenses used by all depenedcies. To scan the application using the TrustSource scanner execute the following command:

```
# scan application
ts-pip-plugin ./
```

The scan results will be printed into the console. To submit the results to the [TrustSource](https://app.trustsource.io/) and execute analysis you need to register in the application first, generate and API-key and create a project. Please visit [TrustSource](https://app.trustsource.io/) for more details. 

To submit result, please, create a TrustSource project file **ts-plugin.json** in the current directory with the following content:

```
{
  "project" : "your project name",
  "apiKey" : "your API key",
  "skipTransfer" : false
}
```

Now you can execute the scan again using the command:

```
# scan application
ts-pip-plugin ./
```

Now if everything is set correct you can see a message "Transfer success!". Open the web application to see results and execute analysis.

# Contribution, Contact and Support
Feel free to reach out to the [TrustSource Team](https://support.trustsource.io/hc/en-us/requests/new "TrustSource Knowledgebase") by dropping us a message or providing [issues](/org/ts-deepscan/issues). We 'ld love o hear your feedback to learn and improve.
Contributions are welcome. Just clone, create your branch and send a pull request. Please make sure to agree to the [contribution agreement](/org/ContributionAgreeemnt.md "Contribution Agreement") and the [coding guidelines](/org/CodingGuidelines.md "Coding Guidelines").

If you like the tool and want to support our further work, feel free to support us with donations or sign a API-usage agreement.
Thank you & best regards!
