---
layout: post
title: Week 2 Project: Create an OSM store
---

The aim of the project was to create an online management store that would manage online stores and allow for OSM administrator, OSM customers (creater of stores) and customers of stores to create stores, have an inventory, add customers and buy items

### My reflection and thoughts on project

    The toughest part of this project was understading classes, instances and attributes, once i mastered the project was easy. You will notice I do not def any attributes until my 'store' class and only pass it the type. Everything is a global variable defined in OSM class and then inherited or a variable called and returned in the methods

    The biggest success I had was understading that I could store class instances in a dictionary and pull them using a key and then call atrributes from each instance

    I used a new function for a dic called "iteritems()" allowing me to iterate through the items in a dictionary"

    I reasearch from the internet how to print out a list of items in a table format

    The project is 90% complete in my mind. It is a minimum viable product
    However i would like to: 
            -clean up the user interface
            -develop option 2 to have the user select from a list of created stores
            -extend the looping so you can continue running throuhg the program and selecting different options
            -create a method to modify the existing inventory to show chnages made by customers
            -create a mehtode to show all purchases by price, quantity, customer for each store
            -clean excessive variable use

     These might occur in the next version

    
    I did not add or need to overide any of the built in methodes such as __repr__ . I understand that this method can be useful for when you want your class to return a specific format or modify __add__ or __eq__ to allow for adding or equaling variables and types that would normaly throw and error or not equal. I will add this next time

##Diagram Of Project

![an image alt text]({{ site.baseurl }}/images/Diafgram_project2.png "an image title")



## Program Structure

* Class osm
    - Class store  (inherits from OSM class)
    - Class Customer (inherits from Customer class)

### These are the Functions found under each class with what they do, functions they call and attributes

* Class osm
    *Attributes  (Global)
      -storeowners      list
      -storeownerlist   dict
      -storelist        list
      -storetemplate    dict of stores and their items
      -Fakecustomers    list of fake customers

    *Methods
    - def createonlinestore   (creates instance of class store)
    - def createownername     (gets user to add their name )           
    - def createfakelist      (creates fake list of stores and owners )


* Class store
    * inherits global attributes from OSM
    -def__init__(self, type1) type 1  inherited from OSM

   * Methods
    -def createproducts       produces list of products for a particular store type
    -def getinventory         creates a fake inventory using random_int and list of products from createproducts
    -def namestore            gets the user to add a name to their store
    -def createfakecustomers  creates a list of fakecustomers for admin purposes
    -def addcustomer          allows the user to add a customer

* Class Customer
    * Attributes
    - inherits from store which inherits from OSM

    * Methods
    -def pickastore  allows a customer of the store to get a list of stores in the systems and then a list of items for that store with prices

### Flow of Intialization
        User prompted:
        **"Select 1 for New Store, 2 for returning Store owner, 3 for OSM administrator, 4 To Shop Stores")**

        - 1 allows the user to create a new store by initialzing OSM then calling methode createonlinestore()

                returns name of store, type of store and inentory

        - 2 would allow a user to pick an existing list of stores (THIS IS NOT AVAILABLE!!! 
            not enought time! wait for next version

        - 3 * allows a user to be the OSM administrator 

            prompted **"Select 1 to view number of stores in system, select 2 to get a list of owners and stores"**
            
            
            *  1 allows a user to be the OSM administrator and the number of stores in the system created using         createfakelist method and storing the instances of each class store in a dictionary

            *  2 also allows to pull a list of owners with their respective stores using the above dictionary

        - 4 allows  user to act as a customer and get

            intializes osm, store and customer classes creating a fakelist of stores with fake inventory
            
            allows a user to pick a store from a list then select items from that store with a fake price created by random_int

    




        













    


