# Hack ED 2016 Jobber API
#### https://getjobber.com
#### http://docs.jobber.apiary.io



# THE RULES
Jobber's API is not a publically available API.

You are being given access to our API, which is currently only available to Jobber and a small handful or partners.

It is not hardened against malicious use.  If you try to break it you will most likely be successful, and we will be very unimpressed.

If you break it by accident there are no hard feelings!

Access will be removed 3 days from when it was granted.



# What you'll need
A Jobber Test Account and Access Token
Postman REST Client
The Jobber API Docs



# Jobber Test Account


# Creating an account
* Go to [https://getjobber.com](https://getjobber.com)
* Click "Free Trial" in the top right
* Fill in your details


# Getting account setup as a tester
* Find *me*, or e-mail ben@getjobber.com with your signup email
* I will:
  * Generate seed data on your account
  * Flag it as a tester account so our sales guys don't try and sell you Jobber.
  * Generate an access token for the API



# Postman REST CLient
Incredibly useful tool for developing against *any* API


# Installing Postman
Go to [https://www.getpostman.com/](https://www.getpostman.com/)

Install the Chrome App or Mac App


# Download and import the Jobber sample collection
Download our sample API requests from [here](/assets/JobberAPISampleRequests.postman_collection)

Click on "Import" in postman and drop in the collection file

![Import in postman](/img/import_into_postman.png)


# Setup Postman
Click on the "eye" icon in the top right, and then "edit" next to globals

![Import in postman](/img/edit_globals.png)

Add DOMAIN (with https://api.getjobber.com) and ACCESS_TOKEN (with your access token) variables

![Postman vars](/img/postman_variables.png)


# Setup Postman
Test using the "Fetch Current User" request

![Test request](/img/test_request.png)



# USING JOBBER API DOCS
[docs.jobber.apiary.io](docs.jobber.apiary.io)


# HEADERS ARE VERY IMPORTANT
You *must* use the version and side loading headers with your request:

X-API-VERSION: 2.2.0

X-API-SIDE-LOADING-ENABLED: true


# IGNORE THE OAUTH 2 SECTIONS
We will generate long lived access tokens for your accounts directly so you're not wasting time on OAuth flows or implementing Refresh Token flows.

Just add the access token we give you to the "Authorization" header as shown in the sample postman requests.


# OMISSIONS AND ERRORS
We attempt to keep our API documentation up to date for our partners, but we do not guarantee 100% alignment.  You may find some areas missing details, or where the responses differ slightly from the documentation.



## GETTING STARTED
Once you have the above all setup, here's some tips to getting started.


## Do a basic flow using postman:
Create a client

Read back that client

Create a job on that client

Read back that job

Create a visit on that job

Read back the visits on that job


## Now do the same flow using code
Implement the API in your programming language of choice

Ruby [httparty](https://github.com/jnunemaker/httparty)
Python [requests](http://docs.python-requests.org/en/latest/)
Javascript [request](https://github.com/request/request)


## Getting help
Look for Jobber shirts
We'll try and find ourselves a table or space where we'll have someone available
