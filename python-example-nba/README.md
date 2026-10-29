## NBA dashboard app and shinyloadtest

Example from: <https://github.com/posit-dev/py-shiny-templates/tree/main/nba-dashboard>

### About `recording.log`

The recording was made again on 2026-10-29 with the Node.js `shinyloadtest` (`shinyloadtest@next`, version 2.0.0-alpha.6) against Posit Connect 2026.07.0. It replays with no errors using one and three workers.

A recording stores the URLs of the app's asset files, and those URLs contain package versions. A recording only replays against an app that uses the same versions. This recording matches `shiny` 1.5.1 and `shinywidgets` 0.7.1. Add `shiny==1.5.1` and `shinywidgets==0.7.1` to `requirements.txt` before you deploy, or record the app again.

The `# target_url:` header is a placeholder. Give the URL of your deployed app to `shinyloadtest replay`. The `run1` folder and the report come from an earlier recording and were not made again.

Install from requirements.txt using uv: 

```bash
uv pip install -r requirements.txt
```

You might need to create a uv environment first: 

```bash
# Check what python versions you have access to
ls -1d /opt/python/*

# Create the uv project, this example declares the python version to use explicitly. Make sure this matches a version you have access to.
uv init --app --python 3.10.16
```

Activate the virtual environment

```bash
source .venv/bin/activate
```

After changing anything be sure to run `uv sync`.

Run the application:

```bash
uv run app-core.py
uv run shiny run --reload app-core.py
```


