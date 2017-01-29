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
