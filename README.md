# Update Bank Accounts and Shoe Store Stock Counts using Stored Procedures in SQL
Using stored procedures to update both shoppers and shoe stores bank account balances as well as shoe stores stock count.

Scenario 1:
James buys 4 pairs of trainers from the shoe shop. His account balance is updated as well as the balance of the shoe shop. Then, he attempts to buy a pair of Brogues from the shoe shop. However, his updated balance is $145, which is $5 less than the price of a pair of Brogues, $150. James has insufficient funds to purchase these shoes and the whole transaction fails. Therefore, the entire transaction is rolled back when the stored procedure is called.

Scenario 2: 
Rose buys a pair of boots from the shoe shop. Her account balance is updated as well as the balance of the shoe shop. Then, she attempts to buy a pair of trainers from the shoe shop. However, her updated balance is $100, which is $200 less than the price of a pair of trainers, $300. Rose ha sinsufficient funds to purchase these shows and the whole transaction fails. Therefore, the entire transaction is rolled back when the stored procedure is called.

Since in both scenarios, the transaction fails and is rolled back, there is no change in the shoe shop stock count (as displayed in the ShoeShop table) or either of James' and Rose's bank account balances (as displayed in the BankAccounts table).
