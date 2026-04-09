# MVDA Tutorial 3

This project contains the work for Tutorial 3 of the Multivariate Data Analysis (MVDA) course.

It uses a Jupyter notebook (`Tutorial3_MVDA.ipynb`) to analyze a movie box office dataset and generate clustering visualizations. The notebook was converted to a static HTML dashboard (`dashboard/templates/dashboard.html`) and served through a simple Django app.

## What is included

- `Tutorial3_MVDA.ipynb` — original notebook with the clustering analysis and visualizations
- `dashboard/templates/dashboard.html` — static HTML dashboard generated from the notebook, with images embedded
- `dashboard/views.py` — Django view that renders the dashboard template
- `dashboard/urls.py` — app URL configuration
- `myproject/urls.py` — project URL configuration to expose `/dashboard/`
- `myproject/settings.py` — Django settings with `dashboard` app added
- `manage.py` — Django project management script

## How to run the project

1. Activate the virtual environment:

   ```powershell
   .\.venv\Scripts\Activate.ps1
   ```

2. Install requirements if needed:

   ```powershell
   python -m pip install django
   ```

3. Apply migrations (only needed once or if the database changes):

   ```powershell
   python manage.py migrate
   ```

4. Start the Django development server:

   ```powershell
   python manage.py runserver
   ```

5. Open your browser and visit:

   ```text
   http://127.0.0.1:8000/dashboard/
   ```

## Notes

- The dashboard page is a static rendering of the notebook output, with only graphs and headings visible.
- All notebook figures are embedded in the HTML so they are displayed without external image files.
- The project is intended for local development and demonstration purposes.
