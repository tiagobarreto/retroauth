## 1.0.1 (2015-07-28)

* Bugfix
  * When multiple authenticated requests were called at the same time, and the provided token was invalid at this time, multiple 401's were returned and multiple login activities were opened.
    * when you do multiple authenticated requests, there will be only one executed at one time. This is to avoid multiple 401's and multiple activities to open.
    * when a request has to wait for another one, it'll be executed as soon as the previous one returns.

## 1.0.0 (2015-07-21)

* Bugfixes:
  * There was a major issue causing a crash, when trying to show the account chooser, after creating a new account
  * Unit Tests for the main functionalities
  * Javadocs for all classes

## 0.1.4-beta (2015-07-10)

* Bugfix:
 * Right after the first login, the Token was not correctly appended to the TokenInterceptor
* Lots of documentation

## 0.1.3-beta (2015-07-04)

* Demo App:
 * can have unlimited amount of users (using any username and the password "test"
 * shows the active account in the title

* Bugfix:

    The Token didn't invalidate on `AuthAccountManager#invalidateTokenFromActiveUser`
* Added `AuthAccountManager#getUserData` to get the userdata of an active account, which were setup in `AuthenticationActivity#finalizeAuthentication`

## 0.1.2-beta (2015-07-04)

 * All retrofit request types are supported
  * rxjava
  * blocking
  * async
 * Added AuthAccountManager to simplify the Account handling with retroauth

## 0.1.1-beta (2015-06-30)

  * Multiple Accounts possible

    If the User has multiple accounts setup and an authenticated request is called, the user
    will see an account picker to choose between the accounts or create a new one

## 0.1.0-beta (2015-06-28)

First public release
