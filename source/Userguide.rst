**User guide**
===============

Introduction
------------
MSH/HCSM is a key member of the Malaria drug management subcommittee, which is involved in the stockstatus monitoring of Malaria commodities both at the National and County levels.

On a monthly basis, the Malaria Control Unit, drug management committee meets to review the stock status ofmalaria commodities in the country, by analyzing data from various sources including:
	#. Facility and County Level Stock Data from DHIS.
	#. National Level Stock Status data from the Supply Chain Agencies (Central SOH).
	#. Pipeline information based on pending shipments per funding agency.

This data is aggregated and analyzed for the different malaria commodities and a 2 pager report generated that
indicates to management, the months stock status and pipeline monitoring of Malaria commodities. 

.. _`DHIS2`: https://www.dhis2.org/

Getting started
---------------
Purpose of this project is to create a stock status management tool that analyzes data from various sources for purposes of analysis and report generation.

The sources include:

#. Facility and County Level Stock Data from DHIS.
#. National Level Stock Status data from the Supply Chain Agencies (Central SOH).
#. Pipeline information based on pending shipments per funding agency.


System requirements
---------------------
Chrome/Chromium browser is recommended for the application. This is because of the javascript used in the application wil be able to load faster.


.. note::

    Login roles to the stock status management tool are also required inorder to access the application and its functionality.




`Authentication`_ is the process by which clients send login credentials over the HTTP to a web server. The request is 
associated with a specific user, while `authorization`_ determines if the user has permission to perform
the requested operation.

.. _`Authentication`: https://www.dhis2.org/doc/snapshot/en/developer/html/ch01s02.html
.. _`authorization`: https://www.dhis2.org/doc/snapshot/en/developer/html/ch01s02.html


Session Authentication
------------------------
Logging in
~~~~~~~~~~~

For the functionality of the system to be accessed, a user has to login to the application. The users of the system have to provide the *username* and *password*.

.. code-block:: javascript

    {
        "username": "username",
        "password": "password"
    }

.. note::

    A successiful login will lead you to using the application.



Here is a screenshot of the application login as seen by any given user:

 	
	.. figure:: images/login.png

After successiful login, the home page is loaded. 

.. note::

    You do not have to login to DHIS2 to use the application.


Here is the screenshot of application layout as viewed by the admin:

    .. figure:: images/home.png


Here is the screenshot of application layout as viewed by the read only user:

    .. figure:: images/home.png



Logging out
~~~~~~~~~~~~

.. note::
    A given user can logout after using the tool by clicking the logout button located in the header. After logging out, the user is redirected to the login page.



**Permissions**
----------------

Login roles
~~~~~~~~~~~~~
There are various user roles according to the user who is logged in:

    #. **Data Entry Users** who can only enter data into the system and view reports.

    #. **General County** Who can only view county reports.

    #. **General National** Who can only view national and county reports.

    #. **The Admin** who has all access of the functionality of the system. These include:

        - Creation and management of users
        - Updating data that is used to generate reports


**User management**
-------------------
The admin has all privillages and permissions to manage users. The admin has privillages to add new users and edit the existing ones.


**Launching the Application**
-----------------------------

The stock status application is launched as a stand alone application since it is not incorporated in DHIS2. However, the application pulls data from DHIS2.

For the application to be launched, this `link`_  has to be typed in the browser. The link redirects the user to the login page.

.. _`link`: http://41.89.93.232/stock-monitoring/


    .. figure:: images/login.png




**Application Layout**
-----------------------


This is the layout of the application:

The Admin View
~~~~~~~~~~~~~~~~


Header
+++++++
The header of the application has no menu. It has a title:  *Malaria Commodities Stock Monitoring Tool*. It also has the log out icon that enables a user to log out of the system.


Side bar
+++++++++
The side bar of the aplication has an array of links as seen in the menu. The admin of the system can be able to view the following:


Home
^^^^^

This link redirects to the Homepage of the application. The dashboard is the home page of the system.


Stocks
^^^^^^^

This link allows the admin to view a report on the malaria stock. It includes:

    #. Planned procurements
    #. Pending shipments
    #. Received stock
    #. Update stock

Reports
^^^^^^^^

This link is used to query various reports from the system. The reports include:

    #. Central Level MOS
    #. Forecast Data MOS
    #. Facility Level MOS
    #. National Level MOS
    #. County Level MOS
    #. Forecast Variance Tracker
    #. Stocks
    #. Pending Shipments Report
    #. Total Pending Commodities per agencies
    #. Individual Shipments



Settings
^^^^^^^^^

This link enables the admin to manage the following:

    #. Funding agencies
    #. Supply chain agencies
    #. Commodities
    #. Zones
    #. Counties
    #. Forecasts
    #. Manage MOS color codes
    #. Manage Users







**Stocks**
-----------------

Planned procurements
~~~~~~~~~~~~~~~~~~~~~
As the admin, you select the planned procurement date from the drop down and then the report is generated. 

    .. figure:: images/planned-procurement.png

You can also add a new planned procurement by clicking the button "add a new planned procurement":

     .. figure:: images/Add-new-planned-procurement.png




Pending shipments
~~~~~~~~~~~~~~~~~~~
This loads the panel for managing the pending shipments. As the admin, you click an item from the pending stock list given for editing or deleting.

    .. figure:: images/pendingShipment.png

After choosing one of the pending stock, you can edit or delete it.
    .. figure:: images/editPendingStock.png

As the admin, you can also add a new transaction by clicking the button of adding a new transaction.

    .. figure:: images/addPendingStock.png



Received Stock
~~~~~~~~~~~~~~~
This loads the panel for managing the received stock. You clicks an item from the received stock list given for editing or deleting.

    .. figure:: images/receivedStock.png

After choosing one of the current stock commodities, the admin can edit or delete it.
    .. figure:: images/editDeleteCurrentStock.png

A user can also add a new record by clicking the button of adding a new record.

    .. figure:: images/addRecievedStock.png


Update Stock
~~~~~~~~~~~~~
A panel for updating the current stocks. THis panel enables you to view a list of the current stock.
 
    .. figure:: images/current-stock.png

#. You can select an item for editing or deleting from the system:

    .. figure:: images/update-current-stock.png



#. You can also add stock to the system:

    .. figure:: images/current-stock.png





**Reports**
-------------
Reports of the system are generated here.


Central level MOS Report(DHIS2)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
It shows a report on the central level MOS from DHIS2. It reports on the following:

    #. Commodity name
    #. Adjusted Facility AMC
    #. Central Stock on Hand KEMSA
    #. Pending Shipments
    #. Central Level MOS
    #. Pending Shipments MOS

    
    .. figure:: images/centralLevelMOSReport.png

Facility Level MOS
~~~~~~~~~~~~~~~~~~~
A report on facility level MOS. It reports on the following:

    #. Commodity name
    #. Adjusted Facility AMC 
    #. Stock on Hand 
    #. Facility Level Month of Stock(MOS) 

    .. figure:: images/facilityLevelMOSReport.png


National Level MOS
~~~~~~~~~~~~~~~~~~~~
A report on national level MOS. It reports on the following:

    #. Commodity name
    #. Adjusted Facility AMC 
    #. Stock on Hand 
    #. Central Stock on Hand KEMSA
    #. Pending Shipments 
    #. Facility Stock on Hand 
    #. Central Level MOS
    #. Pending Shipments MOS 
    #. Facility Level MOS 
    #. National Level MOS 

    .. figure:: images/nationalLevelMOSforeCast.png


County level MOS Report(DHIS2)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
It generates a report on the county level MOS. It reports on:

    #. Commodity name
    #. Aggregated Adjusted Consumption Totals 
    #. Aggregated Stock on Hand Totals 
    #. County level MOS 

    .. figure:: images/countyLevelMOSReport.png




Forecast Data MOS
~~~~~~~~~~~~~~~~~~~
A report on central level MOS using forecast data. It reports on the following:

    #. Commodity name
    #. Forecast Monthly Consumption
    #. Stock on Hand
    #. Forecast Month of Stock(mos)

    .. figure:: images/forecastMOSforeCast.png


Forecast Variance Tracker
~~~~~~~~~~~~~~~~~~~~~~~~~~
A report that tracks the forecast variance at a particular time.

    .. figure:: images/varianceTracker.png




Stocks
~~~~~~~

This shows a report on the individual available stock at a particular period.
It reports on the following:

    #. Commodity name
    #. Unit
    #. Central SOH
    #. Total
    #. Funding agency totals

    .. figure:: images/stocks-reprt.png


Pending Shipments Report
~~~~~~~~~~~~~~~~~~~~~~~~~
It shows a report on the current pending shipment of commodities. It reports on the following:

    #. Commodity name
    #. Expected Stocks
    #. Expected Shipments Totals

    .. figure:: images/current_pendingCommodities.png
    



Total Pending Commodities per source(Agency)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
This shows total pending commoditities per agency over a given period of time. It reports on:

    #. Commodity name
    #. Source(Source) Totals
    

    .. figure:: images/totalPendingStock.png




Individual shipments
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
This shows a report on the individual shipment of stock as per a given period. It shows the following details:

    #. Commodity
    #. Supporting agency
    #. Quantity
    #. E.T.A Details
    #. Color code

    .. figure:: images/individualPendingStockReport.png


**Settings**
------------


Funding Agencies
~~~~~~~~~~~~~~~~~
This loads the panel for managing the funding agencies. The admin clicks a funding agency from the list given for editing or deleting.


    .. figure:: images/fundingAgency.png


After choosing one of the agencies, the admin can edit or delete it.


    .. figure:: images/manageAgency.png

The admin can also add a funding by clicking the button of adding an agency.


    .. figure:: images/addAgency.png




Supply chain agencies
~~~~~~~~~~~~~~~~~~~~~~
This loads the panel for managing the supply chain agencies. The admin clicks a supply chain agency from the list given for editing or deleting.

    .. figure:: images/supplyChainAgency.png

After choosing one of the supply chain agencies, the admin can edit or delete it.


    .. figure:: images/editSupplyAgency.png


The admin can also add a supply chain agency by clicking the button of adding a supply chain agency.


    .. figure:: images/addSupplyChainAgency.png



Commodities
~~~~~~~~~~~~

This loads the panel for managing the individual commodities. The admin clicks a commodity from the list given for editing or deleting.

    .. figure:: images/commodity.png


The admin can also add a commodity by clicking the button of adding a commodity.

    .. figure:: images/addCommodity.png


Zones
~~~~~
The zones are managed here. The admin is able to view the already existing zones. There is an option for editing or editing the zones:

    .. figure:: images/commodity.png

Editing a zone:
    
     .. figure:: images/editZone.png



The admin can also add a new zone into the system. Here is the screen shot:

    .. figure:: images/addZone.png






Counties
~~~~~~~~~
This loads the panel for viewing and updating counties. The admin clicks a specific county from the list given for updating the details about it.

    .. figure:: images/counties.png

After choosing one of the counties, the admin can edit the zone and/or the comment about it.


    .. figure:: images/updateCounty.png


Forecasts
~~~~~~~~~~
This loads the panel for managing forecast commodity data as per the selected period. The admin clicks an item from the list given for editing or deleting.

    .. figure:: images/forecasts.png

After choosing one of the commodities, the admin can edit or delete it.


    .. figure:: images/editForecasts.png

A user can also add a static parameter by clicking the button of adding a static parameter.

    .. figure:: images/addForecasts.png


Manage MOS color codes
~~~~~~~~~~~~~~~~~~~~~~~
This is the panel for management of the MOS color codes. The admin can view the list of the color codes that have been used in the system.

    .. figure:: images/color-codes.png

Manage Users
~~~~~~~~~~~~~~
 Here, the admin can view the list of the users registered in the system. The admin has the permissions of adding new users and updating their details.

    .. figure:: images/manager-users.png








.. toctree::
    :maxdepth: 4
