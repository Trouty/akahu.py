Introduction
============

Getting Your Tokens
-------------------
First you need to obtain an app and user token from Akahu. You can do this by heading to 
`this page <https://developers.akahu.nz/docs/personal-apps#prerequisites>`_ and following the steps detailed. Once
you have obtained these tokens you can move on to installing akahu.py

.. note::
    If you would like to make payments or transfers with Akahu, you **must** enable the payment and transfers permission.
    To do this refer to this `page. <https://developers.akahu.nz/docs/personal-apps-advanced#limiting-permissions>`_

Installation
------------
Place holder

A Simple Example
----------------
Once you have all that house keeping out of the way we can get into the fun stuff! In the following script we:

1. Initialize an Akahu connection
2. Grab all the accounts you have connected to Akahu
3. Loop through them to find the `Chequing` and `Savings` accounts
4. Transfer $100 from the `Chequing` account to the `Savings` account

.. code-block:: python
    :caption: main.py

    from akahu import akahu

    akahu_client = akahu.Client("app_token", "user_token")

    # Grabs all clients connected to your account
    accounts = akahu_client.get_all_accounts()

    # Look for chequing and savings accounts
    for account in accounts:
        if account.name == "Chequing":
            chequing = account
        elif account.name == "Savings":
            savings = account

    # Transfer money from chequing to savings
    transfer = chequing.make_transfer(account.id, 100)

.. warning::
    It is **highly recommended** that you use environment variables to store your user and app token accounts because
    anyone with these tokens will be able to control your Akahu account and all the accounts connected to it.
    Check out :doc:`the safety section </safety>` for more security tips. **BE HYPER VIGILANT** 