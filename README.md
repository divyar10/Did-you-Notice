# Reminder-for-Unread-Notices
An application that sends an e-mail to a registered list of users whenever a new notice is uploaded on NSUT IMS website. Built using a python script that scrapes notices from IMS website and is deployed on an AWS backend. The mails are sent using SendGrid API and the script is made to run daily with the help of cron job (scheduled task).

# Requirements
   - An AWS account
   - SendGrid API
   - Install putty for SSH and Filezilla for FTP to your server instance

# Installations

    pip install pandas numpy sendgrid bs4 lxml xlrd --user 

    - Pandas and Numpy are modules to handle data
    - SendGrid is an API to send e-mails.
    - bs4 or beautiful soup 4 is a package in python used to extract information from various data formats
    - lxml is a data format
    - xlrd is used to handle excel files ( The attenders list is an excel file.)
    -  "--user" grants the privilege to make permanent changes to the server.

    Now the script is scheduled to run daily with the help of crontab.

# To edit crontab

    crontab -e

    After scheduling the tasks save the changes and exit. The emails would be recieved at the scheduled time every day.