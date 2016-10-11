# Practice djangoproject tutorial
## part 1
https://docs.djangoproject.com/en/1.10/intro/tutorial01/

    python -m django --version
    django-admin startproject mysite
    python manage.py runserver
    python manage.py startapp polls

### polls/urls.py
    urlpatterns = [
        url(r'^$', views.index, name='index'),
    ]

### mysite/urls.py
    urlpatterns = [
        url(r'^polls/', include('polls.urls')),
        url(r'^admin/', admin.site.urls),
    ]

# c9.io blank project
## install python3.5
    sudo apt-get install python3.5 python3.5-venv -y

## setup and activate virtual environment
    python3.5 -m venv myvenv
    
    source myvenv/bin/activate
    
## install django  
    pip install django
    
## upgrade pip
    pip install --upgrade pip

## pip freeze
    (myvenv) twoutlook:~/workspace $ pip freeze
    Django==1.10.2
    

## runserver
    (myvenv) twoutlook:~/workspace/mysite $ ./manage.py runserver $IP:$PORT                                     
    Performing system checks...
    
    System check identified no issues (0 silenced).
    
    You have 13 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
    Run 'python manage.py migrate' to apply them.
    
    October 11, 2016 - 07:17:31
    Django version 1.10.2, using settings 'mysite.settings'
    Starting development server at http://0.0.0.0:8080/
    Quit the server with CONTROL-C.
    [11/Oct/2016 07:17:37] "GET / HTTP/1.1" 200 1767

## Github project
    echo "# djangoproject002" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin git@github.com:twoutlook/djangoproject002.git
    git push -u origin master



