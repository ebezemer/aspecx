#Release Notes
##1.2.3
###Bug Fixes
* Email addresses are now stored lowercase to always match invitations

###New Features
* Removed "ticks" in Dashboard Charts for x and y axis for better readability

##1.2.2
###Framework Changes
* Upgrade to angularfire2 2.0.0.-beta.7
* Upgrade to Firebase 3.6.5

###Bug Fixes
* Forgot password displays now Firebase error message, if invalid email is entered
* Group page now correctly wraps invitation text
* Several data access optimizations (unsubscribe lists where possible)
* Android: show splash screen
* Android: show link for download app in inivation email

###New Features
* Added settings page for display duration and add to calendar
* Optionally add rating dates to calendar as a reminder
 * If option is set Calendar entries are created 
  * on group creation for administrator
  * on accept invitation for raters
* Groups can now be renamed
  * Existing ratings will still show to the user the  group name that existed at the rating time
  * Existing calendar entries will not be renamed
