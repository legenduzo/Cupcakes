Cupcake app
===========

Starter code for this application can be found at https://github.com/google-developer-training/android-basics-kotlin-cupcake-app/tree/starter

This app contains a 4-fragment order flow for cupcakes with options for quantity, flavor, and pickup date.
The order details get displayed on an order summary screen which is the last screen and can be shared to another app to
send the order.

This app demonstrates how to use multiple fragments in an activity, a shared ViewModel is used across fragments,
Databinding and LiveData are used to bind the app's logic to the UI and update the information within the app, 
and the Jetpack Navigation component controls the app flow.


## Screenshots

![Cupcake App screens](https://user-images.githubusercontent.com/71154576/145666162-8e5043ba-1116-46e2-8dd7-6d941b05665c.jpg)

1. The entry point of the application. This allows the user to select the number of cupcakes they will like to order. 
The options are limited to 1, 6, and 12.

2. The user picks what favor they want from the options provided. The user can also cancel the order at this stage and will be taken to the 
start screen.

3. Here, the user picks when they want the order delivered. Same day delivery attracts a fee of 3 extra units. 
The application is customised to fetch the user's local currency through their device's locale, 
hence presenting them with the money figures in that currency.

LiveData is used here to automatically update the total figure if the user wants same day delivery which is the default, or would accept
delivery at a later date. If they would accept delivery later, LiveData automatically deducts the 3 extra units for same day delivery from 
the total cost.

A cancel button also allows you to go from this screen to the first screen.

4. The final screen is the summary screen. This screen shows the user the information of all they have chosen and gives them the option to 
send it to another application.

The 'Up' and 'Back' buttons can allow them to go back and change certain things they do not want. They can also totally cancel the order and
go back to the Start screen. This is made possible by the navigation popUp and popUpInclusive attribute within the nav_graph.

![Navigation overview](https://user-images.githubusercontent.com/71154576/145666820-486e6528-b9c1-42b0-b886-942a0421d3d7.png)

