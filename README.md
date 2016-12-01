# app_template

app_template is a template django app, which can be added to an existing 
django project with a simple pip or setup.py install. You can also copy 
the app_template module into your project.

## USE AS TEMPLATE

*Delete this in your app*

Create an application using this as a template with 

```bash
    manage.py startapp \
        --template path/to/app_template/module \
        <app_name> <empty_app_directory>
```

## Quick start

- Install the app in your project environment using 

```bash
python setup.py sdist
pip install --user ./dist/app_template-<version>.tar.gz
```
    
or

```bash    
python setup.py install
```

- Add "app_template" to your project's INSTALLED_APPS setting in 
 <project_name>/settings.py like this::

```python
INSTALLED_APPS = [
    ...
    'app_template',
]
```

- Include the app_template URLconf in your project urls.py like this::

```python
url(r'^app_template/', include('app_template.urls')),
```

- Run `python manage.py migrate` to create the app_template models.

