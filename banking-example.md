| ID   | User Story                                                                                     | Weight (Story Points) | Acceptance Criteria                                                                                                                        |

| ---- | ---------------------------------------------------------------------------------------------- | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |

| US1  | As a user, I want to \*\*create a new bank account\*\* so that I can start using banking services. | 5                     | - User can input person| ID   | User Story                                                                                     | Weight (Story Points) | Acceptance Criteria                                                                                                                        |

| ---- | ---------------------------------------------------------------------------------------------- | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |

| US1  | As a user, I want to \*\*create a new bank account\*\* so that I can start using banking services. | 5                     | - User can input personal info and account type<br>- Account number is generated uniquely<br>- Initial balance can be set or default to $0 |

| US2  | As a user, I want to \*\*login into my account\*\* so that I can access my banking features.       | 3                     | - User enters account number and password<br>- Invalid credentials show an error<br>- Successful login redirects to account dashboard      |

| US3  | As a user, I want to \*\*deposit money\*\* into my account so that my balance increases.           | 2                     | - Deposit amount must be positive<br>- Balance updates correctly<br>- Transaction is recorded                                              |

| US4  | As a user, I want to \*\*withdraw money\*\* from my account so that I can use cash when needed.    | 3                     | - Cannot withdraw more than balance<br>- Withdrawal amount > 0<br>- Transaction is recorded                                                |

| US5  | As a user, I want to \*\*check my account balance\*\* so that I know how much money I have.        | 1                     | - Shows current balance accurately<br>- Updates after deposits/withdrawals                                                                 |

| US6  | As a user, I want to \*\*transfer money to another account\*\* so that I can pay others.           | 5                     | - Must input valid target account<br>- Cannot transfer more than balance<br>- Transaction is recorded in both accounts                     |

| US7  | As a user, I want to \*\*view transaction history\*\* so that I can track all account activities.  | 3                     | - Lists all deposits, withdrawals, transfers with timestamps<br>- Shows balance after each transaction                                     |

| US8  | As a user, I want to \*\*apply for a loan\*\* so that I can get funds for personal needs.          | 8                     | - Can input loan amount, term<br>- System checks eligibility<br>- Approval or rejection is returned with reason                            |

| US9  | As a user, I want to \*\*repay my loan\*\* so that I can clear my liabilities.                     | 4                     | - Can repay full or partial<br>- Balance deducted<br>- Loan balance updated<br>- Transaction recorded                                      |

| US10 | As a user, I want to \*\*generate monthly statements\*\* so that I can see my financial summary.   | 5                     | - Generates PDF or text statement<br>- Includes transactions, balance, loans<br>- Statement shows start and end date                       |

| US11 | As a user, I want to \*\*update my personal information\*\* so that my account is up-to-date.      | 2                     | - Can update phone, email, address<br>- Cannot change account number<br>- Changes reflected immediately                                    |

| US12 | As a user, I want to \*\*close my account\*\* so that I can stop using banking services.           | 5                     | - Only allowed if balance is 0 and loans cleared<br>- Confirmation required<br>- Account marked closed                                     |

| US13 | As an admin, I want to \*\*view all accounts\*\* so that I can manage the bank.                    | 5                     | - Admin can see list of accounts, balances, status<br>- Can search/filter accounts                                                         |

| US14 | As an admin, I want to \*\*approve or reject loans\*\* so that risk is managed.                    | 8                     | - Admin sees pending loans<br>- Can approve/reject with comments<br>- Loan status updated                                                  |

| US15 | As a user, I want to \*\*set up recurring payments\*\* so that I can pay bills automatically.      | 6                     | - User can input payee, amount, frequency<br>- Payment triggers automatically<br>- Transaction recorded                                    |















| Priority | User Story                 | Story Points | Notes                           |

| -------- | -------------------------- | ------------ | ------------------------------- |

| 1        | US1 - Create Account       | 5            | Foundational feature            |

| 2        | US2 - Login                | 3            | Needed to access features       |

| 3        | US3 - Deposit              | 2            | Basic banking functionality     |

| 4        | US4 - Withdraw             | 3            | Basic banking functionality     |

| 5        | US5 - Check Balance        | 1            | Essential for users             |

| 6        | US7 - Transaction History  | 3            | After deposit/withdraw          |

| 7        | US6 - Transfer Money       | 5            | Requires deposit/withdraw logic |

| 8        | US8 - Apply for Loan       | 8            | Loan feature                    |

| 9        | US9 - Repay Loan           | 4            | Requires US8                    |

| 10       | US10 - Generate Statement  | 5            | Requires transaction history    |

| 11       | US11 - Update Info         | 2            | Optional but useful             |

| 12       | US12 - Close Account       | 5            | Requires balance 0 and no loan  |

| 13       | US13 - Admin View Accounts | 5            | Admin feature                   |

| 14       | US14 - Admin Loan Approval | 8            | Admin handles loans             |

| 15       | US15 - Recurring Payments  | 6            | Advanced feature                |

&nbsp; 







System Design Concepts



Classes:



UserAccount – Stores personal info, balance, loans, transactions.



BankSystem – Handles accounts, admin, transactions.



Loan – Stores loan info, status, repayment.



Transaction – Stores details of deposit, withdraw, transfer, loan payments.



Relationships:



BankSystem → UserAccount (1-to-many)



UserAccount → Loan (1-to-many)



UserAccount → Transaction (1-to-many)



Functional Features:



CRUD for accounts



Deposit/Withdraw/Transfer



Loan management



Account statements



Admin approvals



&nbsp; 





al info and account type<br>- Account number is generated uniquely<br>- Initial balance can be set or default to $0 |

| US2  | As a user, I want to \*\*login into my account\*\* so that I can access my banking features.       | 3                     | - User enters account number and password<br>- Invalid credentials show an error<br>- Successful login redirects to account dashboard      |

| US3  | As a user, I want to \*\*deposit money\*\* into my account so that my balance increases.           | 2                     | - Deposit amount must be positive<br>- Balance updates correctly<br>- Transaction is recorded                                              |

| US4  | As a user, I want to \*\*withdraw money\*\* from my account so that I can use cash when needed.    | 3                     | - Cannot withdraw more than balance<br>- Withdrawal amount > 0<br>- Transaction is recorded                                                |

| US5  | As a user, I want to \*\*check my account balance\*\* so that I know how much money I have.        | 1                     | - Shows current balance accurately<br>- Updates after deposits/withdrawals                                                                 |

| US6  | As a user, I want to \*\*transfer money to another account\*\* so that I can pay others.           | 5                     | - Must input valid target account<br>- Cannot transfer more than balance<br>- Transaction is recorded in both accounts                     |

| US7  | As a user, I want to \*\*view transaction history\*\* so that I can track all account activities.  | 3                     | - Lists all deposits, withdrawals, transfers with timestamps<br>- Shows balance after each transaction                                     |

| US8  | As a user, I want to \*\*apply for a loan\*\* so that I can get funds for personal needs.          | 8                     | - Can input loan amount, term<br>- System checks eligibility<br>- Approval or rejection is returned with reason                            |

| US9  | As a user, I want to \*\*repay my loan\*\* so that I can clear my liabilities.                     | 4                     | - Can repay full or partial<br>- Balance deducted<br>- Loan balance updated<br>- Transaction recorded                                      |

| US10 | As a user, I want to \*\*generate monthly statements\*\* so that I can see my financial summary.   | 5                     | - Generates PDF or text statement<br>- Includes transactions, balance, loans<br>- Statement shows start and end date                       |

| US11 | As a user, I want to \*\*update my personal information\*\* so that my account is up-to-date.      | 2                     | - Can update phone, email, address<br>- Cannot change account number<br>- Changes reflected immediately                                    |

| US12 | As a user, I want to \*\*close my account\*\* so that I can stop using banking services.           | 5                     | - Only allowed if balance is 0 and loans cleared<br>- Confirmation required<br>- Account marked closed                                     |

| US13 | As an admin, I want to \*\*view all accounts\*\* so that I can manage the bank.                    | 5                     | - Admin can see list of accounts, balances, status<br>- Can search/filter accounts                                                         |

| US14 | As an admin, I want to \*\*approve or reject loans\*\* so that risk is managed.                    | 8                     | - Admin sees pending loans<br>- Can approve/reject with comments<br>- Loan status updated                                                  |

| US15 | As a user, I want to \*\*set up recurring payments\*\* so that I can pay bills automatically.      | 6                     | - User can input payee, amount, frequency<br>- Payment triggers automatically<br>- Transaction recorded                                    |















| Priority | User Story                 | Story Points | Notes                           |

| -------- | -------------------------- | ------------ | ------------------------------- |

| 1        | US1 - Create Account       | 5            | Foundational feature            |

| 2        | US2 - Login                | 3            | Needed to access features       |

| 3        | US3 - Deposit              | 2            | Basic banking functionality     |

| 4        | US4 - Withdraw             | 3            | Basic banking functionality     |

| 5        | US5 - Check Balance        | 1            | Essential for users             |

| 6        | US7 - Transaction History  | 3            | After deposit/withdraw          |

| 7        | US6 - Transfer Money       | 5            | Requires deposit/withdraw logic |

| 8        | US8 - Apply for Loan       | 8            | Loan feature                    |

| 9        | US9 - Repay Loan           | 4            | Requires US8                    |

| 10       | US10 - Generate Statement  | 5            | Requires transaction history    |

| 11       | US11 - Update Info         | 2            | Optional but useful             |

| 12       | US12 - Close Account       | 5            | Requires balance 0 and no loan  |

| 13       | US13 - Admin View Accounts | 5            | Admin feature                   |

| 14       | US14 - Admin Loan Approval | 8            | Admin handles loans             |

| 15       | US15 - Recurring Payments  | 6            | Advanced feature                |

&nbsp; 







System Design Concepts



Classes:



UserAccount – Stores personal info, balance, loans, transactions.



BankSystem – Handles accounts, admin, transactions.



Loan – Stores loan info, status, repayment.



Transaction – Stores details of deposit, withdraw, transfer, loan payments.



Relationships:



BankSystem → UserAccount (1-to-many)



UserAccount → Loan (1-to-many)



UserAccount → Transaction (1-to-many)



Functional Features:



CRUD for accounts



Deposit/Withdraw/Transfer



Loan management



Account statements



Admin approvals



&nbsp; 







