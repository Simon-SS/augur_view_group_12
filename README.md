# Group 12 Semester Project
- See Group12 folder for documents
- See issues for sprint updates

# Card Dashboard Feature

- Move table/card view out of dropdown into **toggle button** on page
![ReposDropdownAfter](https://user-images.githubusercontent.com/44858849/202265180-57bf754b-9e0d-4256-9805-70f9b0a14d41.png)
- **Remove empty results** and non-useful results on card view
![CardViewAfter](https://user-images.githubusercontent.com/44858849/202265134-6af1bc64-0572-40df-a317-062fadf27da1.png)
- **Change dashboard view into dropdowns** to view the whole picture better
![DashboardAfter](https://user-images.githubusercontent.com/44858849/202265023-6511e465-949a-43e3-8734-1043114c469d.png)

## Testing
- [ ] Navbar change should be consistent on all views
- [ ] Repos dropdown changed to button
- [ ] Toggle button should function as the dropdown in previous version
- [ ] Empty results should never appear
- [ ] Dashboard dropdowns should still allow for "zoomed in" view (zoom already implemented)
- [ ] Dropdowns should include all data visualizations across all repos

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
