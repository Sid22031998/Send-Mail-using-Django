# Send-Mail-using-Django


## Steps:
### 1. django-admin startproject email_automation(anything you want)
### 2. Navigate into the project directory email_automation
### 3. run in cmd : python manage.py runserver //(to check whether app is running or not)
### 4. open settings.py and at the end add :
        EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
        EMAIL_HOST_USER = "abc@gmail.com"
        EMAIL_HOST = 'smtp.gmail.com'
        EMAIL_PORT = 587
        EMAIL_USE_TLS = True
        EMAIL_HOST_PASSWORD = "********"
        
### 5. open abc@gmail.com in gmail then click on Manage Your Account -> Security -> Turn ON 'Less secure app access'
### 6. open cmd and run : python manage.py shell
       Enter:
       from django.core.mail import send_mail
       send_mail('django test mail title', 'django test mail body', 'abc@gmail.com', ['xyz@gmail.com'], fail_silently=False)
       
### 7. check xyz@gmail.com inbox
