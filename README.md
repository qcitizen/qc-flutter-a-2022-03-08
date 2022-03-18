# qc-flutter-a

We have an existing iOS app which can be found on the iOS store here:

[https://apps.apple.com/ca/app/quantified-citizen/id1485884140](https://apps.apple.com/ca/app/quantified-citizen/id1485884140)

There is also a video of the app being used in the assets folder which can be used for reference.

For the purposes of this trial we would like to see an example of the following tasks being performed:



### Recreate the welcome screens

The welcome screens of the app are a simple slider with 4 screens. We want to see how you would structure a simple ui element like this.

Inside the assets folder of this repository you will find the images and english text needed to complete this task.

- Generate a welcome flow that matches that of the existing iOS app. It doesn't need to be pixel perfect, but should work the same, requiring the user to view all 4 screens before tapping "Sign up".
- This isn't intended to replicate the full functionality of the existing app yet. After the "Sign up" button is tapped have the app immediately display the screen specified below:


### Sign up process

The sign up for the app is a bit unusual. We require that users can create an account anonymously so we don't ask them for an email address or to create a password. Instead we give them a list of 12 randomly selected words.

While the app has nothing to do with bitcoin, we use the wordlist from the BIP39 project which can be found here:

[https://github.com/bitcoin/bips/blob/master/bip-0039/bip-0039-wordlists.md](https://github.com/bitcoin/bips/blob/master/bip-0039/bip-0039-wordlists.md)

- Recreate the Sign up screen as seen in the iOS app (text is in the assets folder)
- Using the english BIP39 wordlist, randomly select 12 words and display them as seen in the iOS app Sign up screen
    - You can choose to either bundle the wordlist in the app and select the words randomly using your own function or use a pre-existing library. Explain how you made your choice in the github issue for this task.

- Require users to click the "I Agree to the Terms and Privacy Policy" radio button before clicking sign up.
- Having the signup POST to the registration server is NOT part of this task for now.
- After the user taps "Sign up" you can have the app simply display a screen that says "successfully signed up".
- These 12 words need to be saved locally on the app so that the user can later view them from within the app. Describe how you would plan to implement this securely in a new Issue on this repository.
- None of this has to be a pixel perfect copy of the iOS app. Make it match the overall design, but make  pragmatic decisions for small graphics, icons, and padding.

### Communicate the need for a new endpoint to the engineering team
Imagine now that you have implemented the screens, you need a `/register` endpoint written in the API to join a study. You don't have to write any code, but send an email to one of our engineers who works on the API; matt@quantifiedcitizen.com. In the email, you should:

- Explain what you need the endpoint to do
- Detail the available parameters you could send to the API. These do not need to be the _real_ parameters, but you can imagine you might have something like a `study_id`, or a `user_id` available. Try to include variables that you think would be required, and explain why you think they are needed.
- Describe how the user would flow through the app to register an account
- If you are unsure about what is required, simply ask questions like you would in a real work situation: this is all part of the development cycle

### Finishing up
That's it. Send a pull request to github user "mattpQC" when you're done.
