# Shopping with Django
A shopping site done in Django to show the basics of an ecommerce site. This is a remake of an older application, which tried to do too much. This one focuses on the shopping part, with support for testing.

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
