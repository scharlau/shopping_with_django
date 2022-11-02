# Shopping with Django
A shopping site done in Django to show the basics of an ecommerce site. This is a remake of an older application, which tried to do too much. This one focuses on the shopping part, with support for testing.

After you clone or download the repository use these commands to set things up:

    pyenv local 3.10.7 # this sets the local version of python to 3.10.7
    python3 -m venv .venv # this creates the virtual environment for you
    source .venv/bin/activate # this activates the virtual environment
    pip install --upgrade pip [ this is optional]  # this installs pip, and upgrades it if required.
    pip install django
    pip install faker
    python3 manage.py migrate

This app uses Faker to generate customer and product details in the 'shop/management/commands/populate_tables.py' file. Go to https://faker.readthedocs.io/en/stable/providers.html and look through the options for Standard Providers to see if you want to change any details in values used.

You should now be able to populate the tables with the command:

        python3 manage.py populate_tables

Then you can start the server to see it running. 

You will need to create a superuser as well if you want to work with the admin features. You can do that with the command:

        python3 manage.py createsuperuser

Otherwise each customer created is also a user with a default password set in the management/commands/populate_tables.py file.

You can launch django with the usual command:

        python3 manage.py runserver

As you go around the site notice what's working, what's bare-bones, and other issues. This is not finished, but a work in progress to illustrate how you might build a shopping application.

### The Payment System 
This uses sessions to put items into a basket, which can be seen via 'Basket' link, and then shifted to 'Purchase' with the user details. This is based in part on the example at https://github.com/PacktPublishing/Django-3-by-Example/tree/master/Chapter08 from a book of the same name.

A key for the basket is set in settings.py, which will be unique for each shopper.
A person needs an account before they can see the payment page.

