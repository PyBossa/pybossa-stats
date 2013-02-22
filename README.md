# PyBossa Stats

This small script uses the *pybossa-client* to create a static web page
with some stats about a given project.

# Requirements

You need to install some libs before using it. The best way to do it is using a *virtual environment*:

```bash
  virtualenv env
  .  env/bin/activate
  pip install -r requirements.txt
```

Once the libs have been installed, you are ready to generate the page with the
data.

# Generating some stats and charts

Now you are ready to create the static web page. In order to do it, you
only need to run the following command:

```bash
  python projectStats.py -s PYBOSSA-SERVER -k API-KEY -a APP-SHORTNAME
```

It may take some time to generate the page, as it needs to get all the data
from the server. Once the data has been obtained and processed you will
find the results in a folder with the same name as the application short 
name.

You can anonymize the data if you want, by using the -p (--private) argument.

If you want to see a live example of the results, [check this one](http://pybossa.github.com/pybossa-stats/)

# Generating some stats and charts for a list of apps

If you want to generate the stats for a given list of applications, you could
do it by providing a file with an app short name per line:

```
  flickrperson
  urbanparks
  ...
```

Then, run the following command:

 ```bash
  python projectStats.py -s PYBOSSA-SERVER -k API-KEY --list-apps filename
```

And the script will generate the stats for the given list, providing an
index.html file with an index for the apps.

