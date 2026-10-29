## NBA dashboard app and shinyloadtest

Example from: <https://github.com/posit-dev/py-shiny-templates/tree/main/nba-dashboard>

### About `recording.log`

A recording stores the URLs of the app's asset files, and those URLs contain package versions. A recording only replays against an app that uses the same versions. This recording matches `shiny` 1.5.1, so `requirements.txt` pins that version. If you change the `shiny` version, record the app again.

The `requires-python` value in `pyproject.toml` is `>=3.12`. Change it to match the Python version on your Connect server.

Install from requirements.txt using uv: 

```bash
uv pip install -r requirements.txt
```

You might need to create a uv environment first: 

```bash
# Check what python versions you have access to
ls -1d /opt/python/*

# Create the uv project, this example declares the python version to use explicitly. Make sure this matches a version you have access to.
uv init --app --python 3.12.11
```

Activate the virtual environment

```bash
source .venv/bin/activate
```

After changing anything be sure to run `uv sync`.

Run the application:

```bash
uv run app.py
uv run shiny run --reload app-core.py
```


