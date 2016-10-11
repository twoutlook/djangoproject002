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

## git tag
https://git-scm.com/book/en/v2/Git-Basics-Tagging
    
    
    git tag
    
    -a as add
    git tag -a v0.1 -m "part1, done"
    
    -d as del
    git tag -d v0.1
    
    git tag
    git show v0.1
    git push origin v0.1    
    git push -u origin master

## git add and commit    
    git add .
    git commit -m"xxx"
    
## del remote tag    
http://stackoverflow.com/questions/5480258/how-to-delete-a-remote-tag    
    
    git push --delete origin v0.1
    
## list remote tags    
http://stackoverflow.com/questions/6294224/check-if-pushed-tag-is-on-the-git-remote

    git ls-remote --tags origin