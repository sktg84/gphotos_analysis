# gphotos_analysis
Refer: https://medium.com/@najeem/analyzing-my-google-photos-library-with-python-and-pandas-bcb746c2d0f2

IF we see: Error 403: access_denied The developer hasn’t given you access to this app despite a new project being created
Refer: https://stackoverflow.com/questions/65756266/error-403-access-denied-the-developer-hasn-t-given-you-access-to-this-app-despi
* Go to your developer console.
* Go to OAuth consent screen.
* Go to +Add users, under test users.
* Add the users for the test (even the owner email address if not working without it)

If we get: "photoslibrary v1" does not exist within Google's API library error:
Refer: https://stackoverflow.com/questions/66689941/google-photos-api-new-version
* Try adding the parameter static_discovery=False

google_photos = build('photoslibrary', 'v1', credentials=creds, static_discovery=False)

