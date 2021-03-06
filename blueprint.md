Blueprint of the Problem

The system has one participant named User. 
There are two assets, ie Property and Property Listing, and 
three transactions, ie createProperty, intentForSale and purchaseProperty.


Let’s take a look at participant first.
Here the User is the participant, who is authorised to buy and sell property in the system.

 
Next are the assets.
There are two assets in the system, namely, ‘Property’ and ‘Property Listing’. 
These assets are stored and managed by the Asset Registry. 
The asset registry is an API that is used to store and manage the assets present in the registry. 
For example, here the asset 'Property' is stored in the ‘Property Asset Registry’ and the property ‘Property Listing’ 
is stored in the the ‘Property Listing Asset Registry’. 
 

The ‘createProperty’ transaction is used to register a new property to the system. For example, 
if a user wants to create a property ‘Prop 1’, then the ‘createProperty’ transaction is invoked. 
This creates the property ‘Prop 1’ in the Property Asset Registry. 

The ‘intentForSale’ transaction is called when a participant wants to list his/her property for sale in the 
‘Property Listing Asset Registry’. 
For example, imagine a user ‘User1’ has registered two properties named ‘prop1’ and ‘prop2’ 
to this ‘Property Registration System’ using the ‘createProperty’ transaction. 
Both these properties will now be stored as assets in the 'Property Asset Registry'. 
Now, if at some point of time 'User1' wishes to put up 'prop1' for sale, 
then he will invoke the ‘intentForSale’ transaction. This transaction will copy 'prop1'
to the 'Property Listing Asset Registry' from the 'Property Asset Registry'. 
Note that 'prop1' will exist simultaenously in the 'Property' and 'PropertyListing' asset registries. 


The 'purchaseProperty' transaction is invoked by a user when he/she wants to buy a property. 
For example, if 'user2', who is a user of the system, wants to buy the property 'prop1' of the user 
'User1', then he will invoke the transaction 'purchaseProperty'. 
Invoking this transaction will transfer the ownership of the property 'prop1' from User1 to User2.

