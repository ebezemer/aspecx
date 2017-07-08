# Release Notes
## 1.6.61
### Changes
* Refactoring Constructor to OnInit, Keyboard on Web
* Removed Calendar

## 1.6.6
### Changes
* Refactored Observable Subscribtions to unsubscribe on logout. Code is more stable, but nothing is visibile to the user

### Bug Fixes
* [#140](https://github.com/xamplo/aspecx/issues/140) Fixed writing to wrong Firebase node for user-ratings
* Fixed: clear badge on logout

## 1.6.5
Test Releae

## 1.6.42
### New Features
* Logout de-registers push notifications. Logged out users don't receive push notifications anymore.

## 1.6.4
### New Features
* Adding Push Notifications using FCM (firebase cloud messaging)
 * Notification on new Invitation
 * Notification if a rating "open date" corresponds to the current day. In order to check and notify users in the test environment, a firebase http trigger action must be called https://us-central1-......cloudfunctions.net/onCron.....?key=.......
 * Current limitation: FCM registers a device (not a user). So notifications will be received for any aspecx user, who used that device. NOT the CURRENTLY logged in user. Could be a feature, because the device owner receives a notification for whatever account he ever used.
 
## 1.6.3
### Framework Changes
* Upgrade to ionic-cli 3.3.0
* Upgrade to ionic-angular 3.3.0
* Upgrade to native plugins 3.10.2
* Upgrade to angularefire2 4.0-rc1
* Upgrade to firebase 4.1.1

## 1.6.2
### Bug Fixes
* Fix click-registration-delay of ionic 3.0

## 1.6.1
### Framework Changes
* Upgrade to Angular 4.0.0
* Upgrade to ionic-angular 3.0.1
* Upgrade to ionic-native 3.4.2

### New Features
* Smaller bundle size (now 1.8 MB, before 2.9 MB)

**Breaking Changes**

The ionic-native package 3 is not compatible with version 2. Hence, all native plugins must be tested.
* Keyboard: account, aspect, group, login, rater, register
* File: groups
* SocialSharing: groups, rater, raters
* Calendar: settings, startup, group, inivitation
* Statusbar: startup
* Splashscreen: startup

## 1.6.0
### New Features
* Added Account Page. Users can now update their usernames, email addresses and change their password.
 * Note: changing the username does currently not update the "invited by name" field for open/accpeted/rejected invitations
 * Note: changing the email address does currently not update the "invited by email" field for open/accepted/rejected invitations. 

## 1.5.0
Production Release
 
## 1.4.8
### Framework Changes
* Upgrade to ionic-angular 2.3.0
* Upgrade to ionic/native 2.9.0
 
## 1.4.7
### Bug Fixes
* Fix Permission denied for Android Email Attachment 
 
## 1.4.6
### New Features
* Rotating x-axis labels for timeseries charts for better readability

### Changes
* Removed shifting for data labels of 2nd axis
* Removed action menu in Groups-List and showing details page automatically on tapping a group
* Renamed "Manage Groups" Action Menu Items "Edit Aspects" / "Edit Raters" to "Manage Aspects" / "Manage Raters"
 
## 1.4.5
### New Features
* [#122](https://github.com/xamplo/aspecx/issues/122) Direct Navigation from Groups Page to Ratings Page via Pop-up Menu
* [#118](https://github.com/xamplo/aspecx/issues/118) Slightly shifted data lables for 2nd axis (raters)

### Bug Fixes
* Temporary fix for centered items
* [#75](https://github.com/xamplo/aspecx/issues/75) Changed Text to "Rater with this email is already invited"
 
## 1.4.4
### New Features
* Added Split Pane Support for Menu. Menu now remains open on screens > 768px
* Added new segment (tab) "missed" on the ratings page

### Framework Changes
* Upgrade to ionic-angular 2.2.0
* Upgrade to ionic/app-scripts 1.1.4
* Upgrade to ionic/storage 2.0.0
* Upgrade to sw-toolbox 3.4.0

## 1.4.3
### Framework Changes
* Upgrade to angular 2.4.8
* Upgrade to rxjs 5.0.1
* Upgrade to zone 0.7.2
* Upgrade to ionic-angular 2.0.1
* Upgrade to ionic/app-scripts 1.1.3
* Upgrade to ionic/storage 1.1.9
* Upgrade to angularfire2 2.0.0.-beta.8
* Upgrade to firebase 3.6.9

### New Features
* Change Export Date-Format to be fixed dd.mm.yyyy
* Change Export Filename to contain Groupname and export date
 
## 1.4.0
### New Features
* Administrator can export and mail Rating Statistics for a Group in "Manage Groups"
* iOS: Lightgray color for input-labels for better readability

## 1.3.0
Production Release

## 1.2.8
### Bug Fixes
* Removing [disabled] attribute in Edit-Groupname after ionic fix. All attributes but groupname should remain non-editable.
* Checking for Cordova availabilty before using email or calendar plugins for better web-app support

### New Features
* Adding userinfo in settings page


## 1.2.5
### New Features
Android: Calendar Entry as all-day event

## 1.2.4
New Packaging for Android

## 1.2.3
### Framework Changes
* Upgrade to ionic 2.2.1
* Upgrade to ionic/storage 1.1.7
* Upgrade to ionic-angular 2.0.0   !! Production !!
* Upgrade to ionic-native 2.4.1
* Upgrade to ionic-/appscripts 1.0.0
* Upgrade to Firebase 3.6.6

No relevant breaking changes documented, so everything should continue to work

### Bug Fixes
* [#107](https://github.com/xamplo/aspecx/issues/107) Email addresses are now stored lowercase to always match invitations
* [#104](https://github.com/xamplo/aspecx/issues/104) Add calendar entry without options for non AOSP phones

### New Features
* Removed "ticks" in Dashboard Charts for x and y axis for better readability
* Put Groupname in double quotes ("") in action-sheet for joining groups and joining groups from rejected invitations for better readability
* [#93](https://github.com/xamplo/aspecx/issues/93) List done ratings in reverse order

## 1.2.2
### Framework Changes
* Upgrade to angularfire2 2.0.0.-beta.7
* Upgrade to Firebase 3.6.5

No breaking changes documented, so everything should continue to work

### Bug Fixes
* Forgot password displays now Firebase error message, if invalid email is entered
* Group page now correctly wraps invitation text
* Several data access optimizations (unsubscribe lists where possible)
* [#89](https://github.com/xamplo/aspecx/issues/89) Android: show splash screen
* [#103](https://github.com/xamplo/aspecx/issues/103) Android: show link for download app in invitation email

### New Features
* Added settings page for display duration and add to calendar
* Optionally add rating dates to calendar as a reminder
 * If option is set Calendar entries are created 
  * on group creation for administrator
  * on accept invitation for raters
* [#71](https://github.com/xamplo/aspecx/issues/71) Groups can now be renamed
  * Existing ratings will still show to the user the  group name that existed at the rating time
  * Existing calendar entries will not be renamed
