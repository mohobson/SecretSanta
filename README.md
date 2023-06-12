# Secret Santa

This program is designed to automate the name drawing process of Secret Santa, while ensuring that couples cannot pick each other's names.

## Setup

1. Fill out the participants Excel sheet with the names and email addresses of each participant. **Note:** Don't delete the first row. The emails can be used to anonymously notify each participant of what name they received. You can set this up in the next step.

2. If there are any couples within the group that should be excluded from gifting one another, list them in the 'couples' tab of the Excel sheet.

3. To enable the email service, you will need to create an account with [Sendgrid](https://sendgrid.com/resource/setting-up-your-email-infrastructure-with-twilio-sendgrid/). It's quick and easy, see the link to get started!

4. Once you have a Sendgrid API key, you can create an environment variable for the key. In your terminal, type the following command, replacing `x` with your API key.

    ```
    export SENDGRID_API_KEY=x
    ```

5. You will also need to create an environment variable for your email address used to send emails from Sendgrid. Type the following command in the terminal, replacing the fake email address with your own.

    ```
    export fromaddr=fakeemailaddress@gmail.com
    ```

## Running the Program

Now you are all set up! Run the `drawing.py` file and everyone should receive an email with the name they were assigned.
