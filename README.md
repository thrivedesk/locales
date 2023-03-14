# How to update your translation string
***NB: You need thrivedesk access to Crowdin***

First go to [Crowdin](https://crowdin.com/project/thrivedesk-app/sources/strings)

[![N|Solid](https://www.pngitem.com/pimgs/m/573-5730232_crowdin-logo-hd-png-download.png)](https://crowdin.com/project/thrivedesk-app/sources/strings)

Update the english language file:
- Press Add String from left
- Check the option called - master(locals/master)
- Add string, identifier, context
  - String = "This is your tranlation"
  - Identifier = "this-is-your-translation"
  - Context = "this-is-your-translation"
  - ![translation](https://img001.prntscr.com/file/img001/miXiOBPyQ_ehh1ZM1HiU3g.png)
- Press the Add button at the bottom

Update other language files:
- First go to [All String ](https://crowdin.com/translate/thrivedesk-app/all/en-fr?filter=basic&value=0)
- You will see all you previously added string on the left hand side
- Select the **Untranslated** text, which will be highlighted with a **Red dot** on top of the list
- You will find translation suggestions in the middle section
  - ![translation](https://img001.prntscr.com/file/img001/agm81_oqTImVJRQuvpNBmw.png)
- Choose a suggestion with 100% match & save

Now it's time to sync out GitHub. Usually Crowdin will auto sync everything once a hour.
But if you want to sync everything immediately than follow these steps
- Go to [integration](https://crowdin.com/project/thrivedesk-app/apps)
- Press and goto Gihub. Scroll down a bit and press **Sync**
- If there are any wanring or error message regarding `source`
  - Go to [locals repository](https://github.com/thrivedesk/locales/pulls) on thrivedesk and merge any active PR
  - ![Sync](https://img001.prntscr.com/file/img001/D6nHJSVhQBq3KCe-ADAhEA.png)
- You will get a green check indicating that everything went well

#### How to get get this updates on `app-frontend`?
Run this command on front end: `yarn run fetch:locals`

