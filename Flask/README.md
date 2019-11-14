# Bike N' Ride Flask App Template

## Requirements

This repo uses Python 3.6.0. All python packages can be found in the `requirements.txt` file.

To create a new `conda` environment to use this repo, run:
```bash
conda create --name flask-env --file requirements.txt
conda activate flask-env
```

You will likely need to install additional packages to support your deployment, e.g. `scikit-learn`.  With the `flask-env` activated, you can run `conda install <package-name>`.  Once you are ready to deploy, you can generate your own `requirements.txt` for reproducibility purposes with:
```bash
conda list --export > requirements.txt
```
## Running the Flask Application

```bash
export FLASK_ENV=development
env FLASK_APP=app.py flask run
```

## Sending Data From the Backend to the Frontend

Let's get the current time:
```python
from time import strftime
time_str = strftime("%m/%d/%Y %H:%M")
```

Then let's send it to the frontend:
```python
return render_template("index.html", time_info=time_str)
```

Then on the frontend, display it:
```html
<p>
    Current time: {{time_info}}
</p>
```
