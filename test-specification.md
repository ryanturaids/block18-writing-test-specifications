# Block 18 Workshop 1 - Writing Test Specifications
## Unit Tests
### 1. A function called `multiplication()` that returns the product of two input numbers.
#### Basic Functionality
  - Expect `multiplication(2, 3)` to be `equal to 6`
  - Expect `multiplication(1, 3)` to be `equal to 3`
  - Expect `multiplication(2, 0)` to be `equal to 0`
  - Expect `multiplication(0, 0)` to be `equal to 0`
  - Expect `multiplication(2, 0.5)` to be `equal to 1`
  - Expect `multiplication(2.5, 3.5)` to be `equal to 8.75`
  - Expect `multiplication(2, multiplication(2, 3))` to be `equal to 12`
#### Result Characteristics
  - Expect `multiplication(2, 3)` to be `a number`
  - Expect `multiplication(2, 3)` to be `a positive number`
  - Expect `multiplication(-2, 3)` to be `a negative number`
  - Expect `multiplication(-2, -3)` to be `a positive number`
#### Special Values
  - Expect `multiplication(2, [1])` to be `equal to 2`
  - Expect `multiplication(2, "3")` to be `equal to 6`
  - Expect `multiplication("2", "3")` to be `equal to 6`
  - Expect `multiplication(2, [])` to be `equal to 0`
  - Expect `multiplication(Infinity, 3)` to be `equal to Infinity`
  - Expect `multiplication(-Infinity, 3)` to be `equal to -Infinity`
  - Expect `multiplication(Infinity, -Infinity)` to be `equal to -Infinity`
#### Error Handling
  - Expect `multiplication(2, "a")` to `raise an error`
  - Expect `multiplication("a", "b")` to `raise an error`
  - Expect `multiplication(2)` to `raise an error`
  - Expect `multiplication(2, undefined)` to `raise an error`
  - Expect `multiplication(2, NaN)` to `raise an error`
  - Expect `multiplication(02, 3)` to `raise an error`
  - Expect `multiplication(02, 03)` to `raise an error`
#### Edge Cases
  - Expect `multiplication(0, Infinity)` to `raise an error`
  - Expect `multiplication(2, [1, 2])` to `raise an error`
  - Expect `multiplication(2, {})` to `raise an error`
  - Expect `multiplication(0, {a: 1})` to `raise an error`

### 2. A function called `concatOdds()` takes two arrays of integers as arguments. It should return a single array that only contains the odd numbers, in ascending order, from both of the arrays.
#### Basic Functionality
  - Expect `concatOdds([1,2,3,4,5],[6,7,8,9,10])` to be `[1,3,5,7,9]`
  - Expect `concatOdds([5,4,3,2,1],[10,9,8,7,6])` to be `[1,3,5,7,9]`
  - Expect `concatOdds([2,4,1,5,3],[9,10,7,6,8])` to be `[1,3,5,7,9]`
  - Expect `concatOdds([1,2,3,4,5],[])` to be `[1,3,5]`
  - Expect `concatOdds([],[6,7,8,9,10])` to be `[7,9]`
  - Expect `concatOdds([-1,-2,-3,-4,-5],[6,7,8,9,10])` to be `[-1,-3,-5,7,9]`
  - Expect `concatOdds([1,2,3,4,5],[-6,-7,-8,-9,-10])` to be `[-9,-7,1,3,5]`
  - Expect `concatOdds([11,12,13,14,15],[16,17,18,19,20])` to be `[11,13,15,17,19]`
  - Expect `concatOdds([0,2,4],[6,8,10])` to be `[]`
  - Expect `concatOdds([1,3,5],[7,9,11])` to be `[1,3,5,7,9,11]`
  - Expect `concatOdds([1,1,1],[1,1,1])` to be `[1,1,1,1,1,1]`
  - Expect `concatOdds([],[])` to be `[]`
#### Result Characteristics
  - Expect `concatOdds([1,2,3,4,5],[6,7,8,9,10]).length` to be `5`
  - Expect `concatOdds([0,2,4],[6,8,10]).length` to be `0`
  - Expect `concatOdds([1,2,3,4,5],[6,7,8,9,10])[0]` to be `1`
  - Expect `concatOdds([1,2,3,4,5],[6,7,8,9,10])[4]` to be `9`
  - Expect `concatOdds([5,4,3,2,1],[10,9,8,7,6])[0]` to be `1`
  - Expect `concatOdds([2,4,1,5,3],[9,10,7,6,8])[0]` to be `1`
  - Expect `concatOdds([1,2,3,4,5],[-6,-7,-8,-9,-10])[0]` to be `-9`
#### Error Handling
  - Expect `concatOdds(12345,[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds("string",[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds([1,2,3,4,5],678910)` to `raise an error`
  - Expect `concatOdds([0.1,0.2,0.3,0.4,0.5],[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds(["a","b","c","d","e"],[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds([1,2,3,4,Infinity],[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds([1,2,3,4,[]],[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds([1,2,3,4,{}],[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds([1,2,3,4,undefined],[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds([1,2,3,4,null],[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds([1,2,3,4,NaN],[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds([1,2,3,4,true],[6,7,8,9,10])` to `raise an error`
  - Expect `concatOdds(["1","2",3,4,5],[6,7,8,9,10])` to `raise an error`
#### Edge Cases
  - Expect `concatOdds([[1,2],[3,4],5],[[6,7],[8,9],10])` to `raise an error`
  - Expect `concatOdds([1,"a",3,{},5],[[6,7],null,9,NaN])` to `raise an error`

## Functional Tests

### 1. A shopping cart checkout feature that allows a user to checkout as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log-in if they checkout as a guest.

#### Creating a cart
  - if `guest user` adds an item to the cart, a prompt will appear offering them to create or log into an account to save their cart selection
#### Adding to cart
  - if `any user` selects an item to add to their cart, the site will add one of that item to the cart
  - if `any user` re-selects an item to add to their cart, the site will increase the quantity of that item in their cart by the number of times it has been re-selected
  - if `any user` changes the quantity of an item in their cart to "0", it will be removed from the cart
#### Continuing to checkout
  - if `any user` selects "checkout" on their cart they will be prompted with a message asking if they are sure they are ready to continue to checkout
  - if `any user   selects "checkout" with an empty cart, they will be prompted with a message letting them know to add items to their cart before continuing
  - if `guest user` selects "checkout" on their cart they will be prompted to create or log into an account to save their checkout information
  - if `guest user` enters checkout, they will see an alternate checkout page than a `registered user`
#### Collecting information
  - `guest user` will see an option to fill out new payment information
  - `registered user` will see an option to select saved payment information or add to their list of saved payment information
  - if `registered user` has no payment information saved, they will only see an option to save new payment information
#### Finalizing Order
  - `guest user` will see a prompt to enter an email to recieve a receipt for their order
  - `guest user` will recieve a prompt after ordering offering them to create an account to keep track of their order or make changes
  - `registered user` will recieve a prompt after order is finalized confirming order and saying a receipt has been sent to their email
  - `any user` should recieve a prompt if they complete checkout with incomplete information
  - `any user` should recieve a prompt if payment fails at checkout
  - order from `registered user` is added to order history
#### Generic Functionality
  - If `guest user` closes the webpage a prompt will appear informing them that their current selection may be lost and to log into or create an account to save it.
  - If `guest user` creates an account items in their cart should transfer to the new `registered user` account
  - If `any user` exits checkout, a prompt will appear asking if they are sure and warning them about losing their saved data in the checkout tab, their cart will stay populated with their current selection
  - `registered user` has access to order history
  - `guest user` will recieve an email after checkout prompting them to create an account to access their order history and manage future orders
#### Edge Cases
  - If `any user` inputs an expired card or incorrect card information they will not be allowed to save payment and recieve a prompt
  - If `guest user` loses connection with website, cart will be stored temporarily for them to reaccess from the same browser and connection
  - Limit cart quantity, don't allow users to input large quantities of product (i.e. 99999)
  - Update order data on final checkout in case user is checking out at the stroke of midnight
  - Error out non-standard characters or `<script>` tags in name, address, and payment fields
  - Save a copy of the order data at final checkout so the system will know if the user changes order after it is placed but before the server finishes processing it