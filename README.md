# app_template

app_template is a template django app, which can be added to an existing 
django project with a simple pip or setup.py install. You can also copy 
the app_template module into your project.

## Quick start

1. Install the app in your project environment using
    
    python setup.py sdist
    pip install --user ./dist/app_template-<version>.tar.gz
    
or
    
    python setup.py install

2. Add "app_template" to your project's INSTALLED_APPS setting in 
 <project_name>/settings.py like this::

    INSTALLED_APPS = [
        ...
        'app_template',
    ]

3. Include the app_template URLconf in your project urls.py like this::

    url(r'^app_template/', include('app_template.urls')),

4. Run `python manage.py migrate` to create the app_template models.

