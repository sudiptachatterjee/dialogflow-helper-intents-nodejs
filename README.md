# Actions on Google: Helper Intents Examples using Node.js and Cloud Functions for Firebase

A sample app for the Google Assistant that show examples of the available helper intent elements

## Setup Instructions

See the developer guide and release notes at [https://developers.google.com/actions/](https://developers.google.com/actions/) for more details.

### Steps
1. Use the [Actions on Google Console](https://console.actions.google.com) to add a new project with a name of your choosing and click *Create Project*.
1. Scroll down to the *More Options* section, and click on the *Conversational* card.
1. On the left navigation menu under *BUILD*, click on *Actions*. Click on *Add Your First Action* and choose your app's language(s).
1. Select *Custom intent*, click *BUILD*. This will open a Dialogflow console. Click *CREATE*.
1. Click on the gear icon to see the project settings.
1. Select *Export and Import*.
1. Select *Restore from zip*. Follow the directions to restore from the `HelperIntentsExamples.zip` file in this repo.
1. Deploy the fulfillment webhook provided in the `functions` folder using [Google Cloud Functions for Firebase](https://firebase.google.com/docs/functions/):
    1. Follow the instructions to [set up and initialize Firebase SDK for Cloud Functions](https://firebase.google.com/docs/functions/get-started#set_up_and_initialize_functions_sdk). Make sure to select the project that you have previously generated in the Actions on Google Console and to reply `N` when asked to overwrite existing files by the Firebase CLI.
    1. Run `firebase deploy --only functions` and take note of the endpoint where the fulfillment webhook has been published. It should look like `Function URL (helperIntentExamples): https://${REGION}-${PROJECT}.cloudfunctions.net/helperIntentExamples`
1. Go back to the Dialogflow console and select *Fulfillment* from the left navigation menu. Enable *Webhook*, set the value of *URL* to the `Function URL` from the previous step, then click *Save*.
1. Select *Integrations* from the left navigation menu and open the *Integration Settings* menu for Actions on Google.
1. Enable *Auto-preview changes* and Click *Test*. This will open the Actions on Google simulator.
1. Type `Talk to my test app` in the simulator, or say `OK Google, talk to my test app` to any Actions on Google enabled device signed into your developer account.

For more detailed information on deployment, see the [documentation](https://developers.google.com/actions/dialogflow/deploy-fulfillment).



## References and How to report bugs
* Actions on Google documentation: [https://developers.google.com/actions/](https://developers.google.com/actions/).
* If you find any issues, please open a bug here on GitHub.
* Questions are answered on [StackOverflow](https://stackoverflow.com/questions/tagged/actions-on-google).

## How to make contributions?
Please read and follow the steps in the [CONTRIBUTING.md](CONTRIBUTING.md).

## License
See [LICENSE](LICENSE).

## Terms
Your use of this sample is subject to, and by using or downloading the sample files you agree to comply with, the [Google APIs Terms of Service](https://developers.google.com/terms/).

## Google+
Actions on Google Developers Community on Google+ [https://g.co/actionsdev](https://g.co/actionsdev).

