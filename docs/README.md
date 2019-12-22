# Getting started

Add Talkative to your web app in less than 5 minutes

1. Login to [Talkative](https://meettalkative.com) and click Create an app
2. Copy the code snippet you see in the Install page in to `<head>` of every page of your site where you might want to reach a user. The snippet should look like this:

```
<!-- Start of async Talkative snippet -->
  <script async src="https://meettalkative.com/resources/talkative.min.js"></script>
  <script>
    document.addEventListener("DOMContentLoaded", function(event) {
      talkative.load(YOUR_APP_ID});
    });
  </script>
```

where `YOUR_APP_ID` is the Talkative App ID of your app that you can find in the Install page

You can reach your users on any page which has the above snippet. You'll see them online in your dashboard and can call them at any time.

# Advanced

## Tracking events
Track and segment users you want to talk to by actions they've taken

By default, if you have the Talkative snippet installed on a page, you can see which pages your users are visiting. You can also track more granular events like completeing onboarding, pressing a Submit button or trying a new feature. Simply call `talkative.track(EVENT_NAME)`. 

## Identifying users
Identify users by email to figure out who to reach out to for user interviews

1. If you want to identify users with their email address, you can call `talkative.identify(YOUR_USERS_EMAIL)` on any page that has the Talkative snippet from above. As soon as you call this function, the unidentified user on your page will be labeled with `YOUR_USERS_EMAIL` going forward. 

2. When logging out your user, call `talkative.logout()` so that we no longer associate new users visiting your page in the same browser.

