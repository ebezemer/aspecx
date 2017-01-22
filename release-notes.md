#Release Notes
##1.2.3
###Framework Changes
* Upgrade to ionic 2.2.1
* Upgrade to ionic/storage 1.1.7
* Upgrade to ionic-angular 2.0.0-rc.5
* Upgrade to ionic-/appscripts 1.0.0
* Upgrade to Firebase 3.6.6

No breaking changes documented, so everything should continue to work

###Bug Fixes
* Email addresses are now stored lowercase to always match invitations

###New Features
* Removed "ticks" in Dashboard Charts for x and y axis for better readability
* Put Groupname in double quotes ("") in action-sheet for joining groups and joining groups from rejected invitations for better readability
* List done ratings in reverse order, issue [#93](https://github.com/xamplo/aspecx/issues/93)

##1.2.2
###Framework Changes
* Upgrade to angularfire2 2.0.0.-beta.7
* Upgrade to Firebase 3.6.5

###Bug Fixes
* Forgot password displays now Firebase error message, if invalid email is entered
* Group page now correctly wraps invitation text
* Several data access optimizations (unsubscribe lists where possible)
* Android: show splash screen, fixes [#89](https://github.com/xamplo/aspecx/issues/89)
* Android: show link for download app in invitation email, fixes [#103](https://github.com/xamplo/aspecx/issues/103)

###New Features
* Added settings page for display duration and add to calendar
* Optionally add rating dates to calendar as a reminder
 * If option is set Calendar entries are created 
  * on group creation for administrator
  * on accept invitation for raters
* Groups can now be renamed, fixes [#71](https://github.com/xamplo/aspecx/issues/71)
  * Existing ratings will still show to the user the  group name that existed at the rating time
  * Existing calendar entries will not be renamed
