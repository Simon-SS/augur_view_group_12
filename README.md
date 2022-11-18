# Filter Features
## Will have filter 'modules' that you can compound on top of each other
Press add filter button, will then create a new empty filter on screen showing lower-bound filter_option upper-bound and an two piece button that works like a light switch, either asc or des
These blanks are for inputting data ranges based on the filter option selected
Filters can be stacked on top of eachother, making a logical OR when using multiple of the same type of filter, and a logical AND when using multiple different filters. They also always require one bound to be filled
You can also add one orderer, which will sort the repos matching your filtered criteria. These orderers can be reversed using acs/des
### Filter Options
- Can filter for data in a time range
  - 10/01/20 timeframe_filter 12/01/20 will filter by data between 10/01/20 and 12/01/20
- Can filter by number of commits
  - 10 commits_filter 50 will filter by repos between 10 and 50 commits
- Can filter by number of pulls
  - 15 pulls_filter 200 will filter by repos between 15 and 200 pulls
- Can filter by number of issues
  - issues_filter 5 will filter by repos with less than 5 active issues
- Can filter by number of resolved issues
  - 20 resolved_filter will filter by repos with more than 20 resolved issues
- Can filter by number of contributors
  - 15 contributors_filter will filter by repos with more than 15 contributors
### Order Options
- Can order by most recent: commit latest_commit
- Can order by most commits: most_commits
- Can order by most pulls: most_pulls
- Can order by most issues: most_issues
- Can order by most issues resolved: most_resolved
- Can order by most contributors : most_contributors
#### Add more filters/orders as they're thought of

# augur_view

HTML frontend for Chaoss/Augur, written with Bootstrap and served by Flask

## To run as a local development instance:

1. [setup a virtual environment](https://docs.python.org/3/library/venv.html#module-venv)
    - `python3 -m venv env`
    - `source env/bin/activate`
2. Make sure you have the requirements installed
    - `pip3 install -r requirements.txt`
3. Run the app
    - `./run.sh`

Once the server is running, you can change the default `serving` url in `config.yml` and either restart the app or navigate to `[approot]/settings/reload` in the browser to connect to the desired augur instance. For example, if you are serving from http://new.augurlabs.io you would enter the url: http://new.augurlabs.io/settings/reload.

## Quick start with Docker

Acquire the [Dockerfile](Dockerfile), and run the following commands in the terminal:
```bash
docker build -t augur-view .
```

```bash
docker run -p 8000:8000 augur-view
```

Note that the port configuration for the -p argument is `[host]:[container]`, in case you want to adjust the port mappings.

## Proxy and service installation

For installation instructions on a server, and information on setting up a proxy, see [installing](installing.md).

## Contributing

To get started with developing for augur_view, see [modules](modules.md).

Copyright 2021 University of Missouri, and University of Nebraska-Omaha
