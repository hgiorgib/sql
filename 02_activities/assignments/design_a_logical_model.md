# Assignment 1: Design a Logical Model

## Question 1
Create a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).

ANS:

![Q1.EDR.png](./images/Q1.EDR.png)

## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.

ANS:

![Q2.EDR.png](./images/Q2.EDR.png)

## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?

_Hint, search type 1 vs type 2 slowly changing dimensions._

Bonus: Are there privacy implications to this, why or why not?
```
ANS:

*Type 1: Overide changes*
- customer_id (PK) + (FK): in customer table
- address
- city
- province
- postal code
- country

*Type 2: Retain changes*
- address_id (PK)
- customer _id (FK)
- address
- city
- province
- postal code
- country
- valid_date
- expire_date


## Question 4
Review the AdventureWorks Schema [here](https://imgur.com/a/u0m8fX6)

Highlight at least two differences between it and your ERD. 

ANS:

Differences:
*Complexity: 
- AW schema is a more complex system that composed by 6 sub-schemas for the processes of Sales, Purchasing, Person, production, HR, and DBO. It contains 70 tables in total.
- My schema is a simple design for a physical bookstore composed by 6 tables to store info related to employees, customer, sales, books, orders and dates.

 *Scope:
- AW schema joints the interaction of 6 functional work groups or department that operate a big bookstore with the following scopes: i) international transactions, ii) online and in-store sales, iii) HR management, iv) whole and retail sales, v) offer promotions, and vi) book production.
- My schema was design for a physical retail bookstore that keeps the data of its orders, sales, customers and books.

Would you change anything in yours?

If I had to broaden the scope on my bookstore, I would consider to add some of the tables of the AW schema to offer services such as online sales and international transactions.

# Criteria

[Assignment Rubric](./assignment_rubric.md)

# Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `September 28, 2024`
* The branch name for your repo should be: `model-design`
* What to submit for this assignment:
    * This markdown (design_a_logical_model.md) should be populated.
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `model-design`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-4-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
