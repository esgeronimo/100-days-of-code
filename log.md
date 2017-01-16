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
