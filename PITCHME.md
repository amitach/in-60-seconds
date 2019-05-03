# Let's Get Started

---

## CODING TECHNIQUES

![](assets/img/presentation.png)

---
@title[Customize Slide Layout]
Code review is an opportunity to not only show others the best practices, conventions, and look for correctness and edge cases, but also learn a great deal from them.
An ideal code base is that which looks like it's been developed and maintained by a one developer, in a company of hundreds of developers.
The following code was submitted as part of the pull request by your teammate.
The application is a typical e-commerce app. The controller action is the order creation endpoint for the app.
The application has Products with a price attribute. We have shopping Carts that have many Products through OrderedItems join table. An OrderedItem belongs_to a Cart and a Product. It has a quantity attribute to keep track of the number of products ordered.
The OrderedItem also belongs_to an Order. This association will be made upon checkout when it's associated with an Order.
When a user checks out, the items in the Cart are associated with a new Order. The Order has a total_price attribute that is calculated by adding up the number of OrderedItems' quantity multiplied by their price, plus tax and shipping, and can be paid for using a credit card.
The code seems to be doing many things in the OrdersController#create:
1. Instantiate a new Order object.
2. Add the items from the Cart record to the Order instance.
3. Add shipping and tax to the total_price of the Order instance.
4. Process the user's credit card
5. Instantiate an ActiveMerchant client
6. Using ActiveMerchant check whether the credit card information is valid, if invalid, we stop the transaction and display an error to the user
7. If the credit card is valid, we charge the card via ActiveMerchant, if charge fails, we stop the transaction and display an error to the user
8. Set the Order's status attribute to processed and save the Order
Thoughts:
1. How would you refactor this code to demonstrate your best practices and coding standards to your teammates?

2. How would you organize the code within the application?

3. How would you explain to the author of the pull request the issues with the pull request, and why your approach is better? In such cases, are there any rule of thumbs that you follow that you could give to your teammates so that they can write cleaner code next time?'
@snap[west span-50]
## Customize Slide Content Layout
@snapend

@snap[east span-50]
![](assets/img/presentation.png)
@snapend

---?color=#E58537
@title[Add A Little Imagination]

@snap[north-west]
#### Add a splash of @color[cyan](**color**) and you are ready to start presenting...
@snapend

@snap[west span-55]
@ul[spaced text-white]
- You will be amazed
- What you can achieve
- *With a little imagination...*
- And **GitPitch Markdown**
@ulend
@snapend

@snap[east span-45]
@img[shadow](assets/img/conference.png)
@snapend

---?image=assets/img/presenter.jpg

@snap[north span-100 headline]
## Now It's Your Turn
@snapend

@snap[south span-100 text-06]
[Click here to jump straight into the interactive feature guides in the GitPitch Docs @fa[external-link]](https://gitpitch.com/docs/getting-started/tutorial/)
@snapend
