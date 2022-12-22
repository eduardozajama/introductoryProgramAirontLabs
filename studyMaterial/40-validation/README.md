# 40. Validation
## What is Validation?
Validation is an automatic check to ensure that data entered is sensible and feasible.

Validation cannot ensure data is accurate.

When programming, it is important that you include validation for data inputs. This stops unexpected or abnormal data from crashing your program and prevents you from receiving impossible garbage outputs.
Why is data validation important?
Data validation ensures that incoming data is accurate, complete, and correct ("valid"). Incorrect or incomplete ("invalid") data could result in a flawed analysis or processing of that data. If some data is invalid, all analysis performed on the entire data set may be invalid.

If a user makes a mistake when providing input, the software application should detect the error and ask the user to correct the mistake.
If a user intentionally provided bad input, the fraudulent data should be rejected and never provided to the software's data processing routines.
Data validation can also detect when data is unintentionally corrupted during storage or transit.

## Types of data validation
* Range check - the input must fall within a specified range. This is usually applied to numbers and dates, but can apply to characters. For example, when making a payment to someone, the amount to be entered might be set to be greater than zero and not greater than the funds available.
* Length check - the input must not be too long or too short. For example, a surname will require at least one letter, but is unlikely to require more than 40.
* Presence check - a data value must be entered. For example, entering a quantity when placing an order.
* Format check - the data must be in the correct format, such as entering a date in the format DD/MM/YYYY.
* Type check - the data must be of a specified data type, such as an integer when specifying a quantity.

## Resources
https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation
https://www.bbc.co.uk/bitesize/guides/z4cg4qt/revision/2#:~:text=Validation%20applies%20rules%20to%20inputted,fall%20within%20a%20specified%20range.
https://www.computerhope.com/jargon/d/datavali.htm
https://www.computerscience.gcse.guru/theory/validation

