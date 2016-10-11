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

 
# djangoproject002
