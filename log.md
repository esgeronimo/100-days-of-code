# 100 Days Of Code - Log

### Day 0: January 11, 2017

**Today's Progress**: Updated implementation of deleting Order Items

**Thoughts:** Heads up! I've already started this project last Friday. Since it would be a waste not to continue this and think of new things to implement, I decided to add this as part of the challenge. I guess the learning process would be much more important than the project for this one.

I am slightly getting familiar with the basics of React. Did some refactoring of the delete functionality for the Order items.

Next task is to understand how I can implement accessing the page with an initial order item. 

Something like http://ordertaker.com?initOrderId=ABC123. 

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web/commit/8deb43943d0445bce23e1b84f4a7befd57744a79)

### Day 1: January 12, 2017

**Today's Progress**: Updated React setup

**Thoughts:** I used the _webapp_ Yeoman generator for this project which does not have React out of the box. I had a hard time looking on how I can add React to the project and it took several errors and investigation to get it done. Later did I know that there is actually a [recipe](https://github.com/yeoman/generator-webapp/blob/master/docs/recipes/react.md) for adding React to this generator. Well I guess that is the better approach so I decided to create a branch and refactor the current setup. 

Another thing. Some of the changes I did yesterday was not pushed to Github. Luckily it is not that big and I was able to retrieve it on my local repo.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web/commit/7d034a69f48133f3fd699d006958a0570cf91f85)

### Day 2: January 13, 2017

**Today's Progress**: Added initial Menu component and its Bootstrap Modal

**Thoughts:** Lame. I was only able to add a non-functioning Menu component and dealt much time on making Bootstrap modal to work. I initially added the _react-bootstrap_ plugin but later realised that there is no need to put one since the existing Bootstrap content works fine with the current React code. I am starting to think that React is not that flexible with other libraries since there exists this kind of libraries (react-bootstrap) - which is like telling you "Bruh you have many things to do in order for React to work with some random library so I'm doing you a favor by creating a plugin...".

For tomorrow, I will continue and finish the Menu component. Hopefully. :)

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web/commit/7a77db5c91d4a8f57a79982682f05a9aa6ee4b8a)

### Day 3: January 14, 2017

**Today's Progress**: Can now add additional order through Menu list

**Thoughts:** The Menu modal page can now be used to put additional order on the Order list. Main problem is updating the quantity of the order item when user selects a duplicate item from the menu. The Order list should not be adding a new item for this scenario but instead increment the quantity of the duplicated item - and this is currently not working. I was able to make it work by changing the attribute _defaultValue_ of input element specific to rendering the _quantity_ value into _value_ however this make the element uneditable.

For details, please refer to https://github.com/esgeronimo/ordertaker-web/blob/6d28949c04002cf159dc31f33b86f6a9840ecb0f/app/scripts/orderItem.jsx

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 4: January 15, 2017

**Today's Progress**: Add Order Item through Menu list now owrking

**Thoughts:** Was able to progress and finish the menu list. User will now be able to edit quantity of order item or add a new order item through the Menu list modal.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 5: January 16, 2017

**Today's Progress**: Attempt to add React-Router

**Thoughts:** No progress adding the module at all. I am not really sure how I can use it once I did something like this: https://github.com/yeoman/generator-webapp/blob/master/docs/recipes/react-router.md

I also attempted adding it as a component via _bower_ but I am also not sure how to continue with it because the bower just gives me a project that is required to be built first before I can get the required .JS file. Whatever.

Maybe tomorrow I'll just focus on the features rather than wasting a couple of days.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 6: January 17, 2017

**Today's Progress**: Changed task! Created Menu Form

**Thoughts:** Since I am still having trouble understanding how the _react-router_ integration should be used, I focused today's work on creating the _Menu Form_. The menu is a list of items that a _seller_ is selling. Previously, I am just using the menu to show customers all of the available items. I am re-using the _Menu_ component to implement a feature that will let the seller edit the menu. This means adding extra logic on Menu component so that it will either show customer or seller specific elements.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 7: January 18, 2017

**Today's Progress**: Fixed issue on updated menu item during cancel

**Thoughts:** Not sure if its a good practice to separate declare each menu item domain property in a component like what I did here:
https://github.com/esgeronimo/ordertaker-web/commit/09f5426681e3d82a6fae69a35481e22b88bb92f7

Fixed an issue wherein a menu item information is still updated even during trigger of cancel button on Menu Form component. 

I've also add a minor improvement on the menu item list by putting a sub-text below the menu item name that will show the description value.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 8: January 19, 2017 (?)

**Today's Progress**: Refactoring: Stateless MenuForm

**Thoughts:** First of all, this commit is like 12:58 in the morning of January 20. Haha!
Just looking at how I can make the MenuForm "stateless". I've actually reverted back to using an object (menu item) for the MenuForm because I realised that declaring properties individually will become a mess once I manage the states of each information on the parent component. Passing information would be easier if they are grouped together, in this case a _menuItem_ object. 

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 9: January 20, 2017

**Today's Progress**: Refactoring: Stateless MenuForm Part 2

**Thoughts:** Done refactoring MenuForm (also Menu) component. Started doing Customer component that will focus on managing the customer emails where orders will be sent.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 10: January 22, 2017

**Today's Progress**: Customer Component and some Fetch stuff

**Thoughts:** Started creating the customer component along with understanding how the `fetch()` method will work.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 11: January 23, 2017

**Today's Progress**: Integrated React Router

**Thoughts:** I was thinking of implementing something like `ordertaker.com/#/quickorder/{menu_item_id_here}`. 

The original concept has email as the main communication to the customers. The email contains the list of food that can be ordered on the same day. Usually customers would just select an item on the list so it would not be a good idea to show a blank order form. Rather, why not just add a button on each item that will redirect them to the app with the specific item ordered already shown? 

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 12: January 24, 2017

**Today's Progress**: Started implementation of Quick Order Component

**Thoughts:** Started doing stuff for the _quick order_ functionality. Looks like I will need to use a mock API server to continue with the updates.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 13: January 25, 2017

**Today's Progress**: Not much progress

**Thoughts:** Just playing around with the implementation of quick order. Added `preOrderedItems` property to Order component which can be used to support initial list of order items.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 14: January 27, 2017

**Today's Progress**: RESET

**Thoughts:** Having a Bower and Webpack is confusing. I definitely want to use the Webpack because it simply looks better to have all my scripts in a single file during deployment.

So I restarted the project. Well not necessarily a restart because I will be able to consult my old implementation and _possibly_ re-use some code.

The _react-webpack_ Yeoman scaffold provides answers to my problem like:
* Always adding new .JS file on _index.html_
* Grouping my files according to logical separation
* An "import" and not just globally accessing classes

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 15: January 28, 2017

**Today's Progress**: NPM ALL THE THINGS!

**Thoughts:** No more Bower (for now). React and all things related to Bootstrap are already added to my project through NPM.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 16: January 29, 2017

**Today's Progress**: Fix naming of Order components

**Thoughts:** Just want to make sure that Order components are logical, I fixed the component names. _OrderComponent_ no longer points to the single unit of order but instead refers to the entry point of Order. An item of order is now called an _order item_.

Also, Order now handles:
* /order - for empty order page
* /quickorder/:qoid - for order page where a specific order item is already added.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 17: January 30, 2017

**Today's Progress**: Added Product Management

**Thoughts:** Created product management since this will be the starting point for the creation of Menu and Order information.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 18: January 31, 2017

**Today's Progress**: Added Product Details

**Thoughts:** Added product details component. Little by little, I am learning the best practices on implementing React components. I am finally getting used to the container and presentation component approach.

Here are some good resources for learning React patterns and best practices:
* http://reactpatterns.com/
* https://github.com/planningcenter/react-patterns

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 19: February 01, 2017

**Today's Progress**: Continuation of Product Details

**Thoughts:** Implemented a generic `onChange` event handling for the current fields of the product details component. All I need to do is to add `name` attribute to every form field containing the corresponding product property names and basically adding this function as part of _ProductManagementComponent.js_:

`this.handleProductDetailsChange = (event) => {
  this.state.selectedProduct[event.target.name] = event.target.value;
  this.setState(this.state);
}`

Another thing... since I am directly updating the state of `selectedProduct`, I need to clone the selected product so that I will not update the actual product included in the list. Hopefully this is not a bad practice.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 20: February 02, 2017

**Today's Progress**: Still stuck in product

**Thoughts:** Confusing component names and purpose. I need to rethink my implementation.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 21: February 04, 2017

**Today's Progress**: Roaming the magical world of React and Javascript

**Thoughts:** Part of learning and getting familiar with a new stuff is repeating the process until you get comfortable doing it. I haven't progress on this project to be honest but I am learning a lot not just with React but with new Javascript things. I also get to think and design starting with the simplest part of the application. By the end of 100 days, I might not finish any project but I do believe that I will be able to improve my skill as a developer and be in-sync with the current technology and approaches.


**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 22: February 05, 2017

**Today's Progress**: Adding features to input components

**Thoughts:** Will add some features to the input component such as validation. I found this example implementation https://spin.atomicobject.com/2016/10/05/form-validation-react/. 


**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 23: February 06, 2017

**Today's Progress**: Minor updates on Product module

**Thoughts:** Nothing much. Just clean up, introduced an component for price inputs and started re-doing product list components.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 24: February 08, 2017

**Today's Progress**: Product List Updated Implementation

**Thoughts:** I need to redo the product list implementation to make it simpler and readable. I am expecting it to be finished by tomorrow.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 25: February 10, 2017

**Today's Progress**: Product Form Updated Implementation

**Thoughts:** Some minor changes on product form and removed most of the warnings.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 26: February 11, 2017

**Today's Progress**: Fixed PriceInputComponent Issue
**Thoughts:** Fixed issue where PriceInputComponent is returning string instead of number.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 27: February 13, 2017

**Today's Progress**: Server Calls Implemented for Product
**Thoughts:** Using a mock server, I was able to try and start updating the container components by adding async server calls via `fetch`.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 28: February 17, 2017

**Today's Progress**: ProductFormContainer Add/Update Updates
**Thoughts:** This was a busy week for me. I was not able do some improvements on my project.
Today, I just updated implementation of Add/Update service calls for `ProductFormContainer` as well as mock API.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 29: February 20, 2017

**Today's Progress**: Delete Product and initial commit for Menu module
**Thoughts:** Finished with initial implementation of delete for products and started with menu all over again. I believe this time, it would be a lot faster to implement the basic CRUD features since I can base it on the existing product module.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 30: February 22, 2017

**Today's Progress**: Added Menu Component and moved MenuManager Component to a new location
**Thoughts:** User-experience-wise, a menu management screen should be able to easily create a new product if the user was not able to find the product he/she wants to add. Because of this, I moved MenuManager component out of the `menu` directory and create a `manage` directory. The latter will depend on Menu and Product components.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 31: February 25, 2017

**Today's Progress**: Added Modal component and tried out Google Sheet API

**Thoughts:** Added `common/ModalComponent` that uses `bootstrap modal`. I've also tried Google Sheet API and it looks like a better alternative to database for content storage for this kind of app.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 32: February 26, 2017

**Today's Progress**: Product List and Create Menu using Google Sheet API

**Thoughts:** Continued with Google Sheet API integration on the mock server. Product list is now coming from a created Google spreadsheet. Also started creating `Create Menu` which creates a separate sheet on the spreadsheet. This will be used to store a menu along with orders.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 33: March 02, 2017

**Today's Progress**: Create Order Page and Customer Service

**Thoughts:** Started doing the create order page. Re-used implementation of product list components with slight tweaks so that items can be toggle-able. I also started creating the Customer service which, for now, only retrieves the name/email of the customer.

**Link to work:** [Ordertaker App](https://github.com/esgeronimo/ordertaker-web)

### Day 33: March 04, 2017

**Today's Progress**: Created new Repo and Create Menu Implementation

**Thoughts:** I'm planning to move the API and Web projects into a single location so I created the `/ordertaker` repository. 
The API was previously just a mock node server located on my machine but I decided to create the actual API project based on the stuff I made from the mock server source code and that includes the integration to Google Sheet API.

Speaking of Sheet API, I am now able to create a menu and store it as a separate sheet on a Google spreadsheet. The sheet contains list of selected products and customer email addresses.

**Link to work:** 
* [Ordertaker Web](https://github.com/esgeronimo/ordertaker-web)
* [Ordertaker](https://github.com/esgeronimo/ordertaker)
