Using this site:
Create a Feature and Steps file that will test the contact us page on htps://www.one80training.com/scrum-labs/
You should have tests that test for the following positive and negative test cases.

1) Create a @test tag, and add the script the runs it headless=n
2) Create a @prod tag, and add the script the runs it headless=y
3) For all test write a valid regular expression for the email field to validate that the email has an @ symbol and a '.' plus three characters after the dot
4) Write a test to allow for a user to submit a contact form that completes all fields and chooses topic 1.  The form should be submitted successfully
5) Write a test to allow for a user to submit a contact form that completes all fields and chooses topic 2.  The form should be submitted successfully
6) Write a test to allow for a user to submit a contact form that completes all fields and chooses topic 3.  The form should be submitted successfully
7) Write a test to allow for a user to submit a contact form that completes all fields and choose topic 2 that is missing the phone number.  The form should be submitted successfully
8) Write a test to allow for a user to submit a contact form without a name & they complete all fields and choose topic 2.  Validate that you receive the one-screen warning
9) Write a test to allow for a user to submit a contact form without a name or company & they complete all fields and choose topic 1.  Validate that you receive the one-screen warnings
10) Write a test to allow for a user to submit a contact form without message & they complete all fields and choosing topic 3.  Validate that you receive the correct message alert
11) Write a test to allow for a user to submit a contact form without a name or message & they complete all fields and choose topic 1.  Validate that you receive the one-screen warnings and the message alert
12) Write a test to allow for a user to submit a contact form without email and choose topic 3.  Validate that you receive the one-screen warning
