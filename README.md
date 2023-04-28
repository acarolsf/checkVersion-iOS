# Check Update iOS

Code to check if there is a new version on AppStore.

This code is a version based on [@anupgupta-arg](https://github.com/anupgupta-arg/iOS-Swift-ArgAppUpdater)'s code.

## Usage

You can force the update by calling

```
CheckUpdate.shared.showUpdate(withConfirmation: false)
```

Or the user can choose if they want to update now or later by calling

```
CheckUpdate.shared.showUpdate(withConfirmation: true)
```

But, if you want to check if there is a new TestFlight version to update, you can try:
```
CheckUpdate.shared.showUpdate(withConfirmation: true, isTestFlight: true)
```

## Important

Inside the code has a link from iTunes. There, you should pay attention and put the country where the application is available.
Like this: ``http://itunes.apple.com/<country>/lookup?bundleId=\(identifier)``

*For example:*
- *``let url = URL(string: "http://itunes.apple.com/br/lookup?bundleId=\(identifier)")``* if the application is available in Brazil

And, in this [documentation](https://developer.apple.com/documentation/appstoreconnectapi/list_all_builds_of_an_app) we can use:

``"https://api.appstoreconnect.apple.com/v1/apps/\(identifier)/builds"``

But, we need to generate a JWT Token first.

To learn how to generate an acceptable token, you should use this [documentation](https://developer.apple.com/documentation/appstoreconnectapi/generating_tokens_for_api_requests).

## Screenshots

- If you call this line 
```
CheckUpdate.shared.showUpdate(withConfirmation: true)
```

![img_2968](https://user-images.githubusercontent.com/6472263/43183229-09700046-9002-11e8-8548-1aa1dd446b33.PNG)

- Or if you call this line 
```
CheckUpdate.shared.showUpdate(withConfirmation: false)
```

![img_2969](https://user-images.githubusercontent.com/6472263/43183234-0c248ee2-9002-11e8-8a62-f703477969fd.PNG) 
