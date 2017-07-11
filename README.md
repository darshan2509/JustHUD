# JustHUD
````JustHUD```` is a Swift based clean and easy-to-use HUD meant to display the progress of an ongoing task on iOS

````JustHUD```` is an iOS drop-in class written in Swift that displays a translucent HUD with an indicator and/or labels while work is being done in a background thread.

## Installation
Download the JustHUD.swift file and add it into your project target.

## Usage
- Just the loader 
````swift
JustHUD.shared.showInView(view: view)
````  
![](http://i.imgur.com/Yw3kE6r.png)

- Add title and footer text 
````swift
JustHUD.shared.showInView(view: view, withHeader: "Loading", andFooter: "Please wait...")
````  
![](http://i.imgur.com/pm5J5CI.png)

- Set color to the header, footer, loader or to the background view
````swift
JustHUD.setHeaderColor(color: UIColor.blue)
JustHUD.setFooterColor(color: UIColor.blue)
JustHUD.setLoaderColor(color: UIColor.blue)
JustHUD.setBackgroundColor(color: UIColor.white)
````  
![](http://i.imgur.com/EfzWnxJ.png)

- Customize: Set color the the background view and let header, footer and loader infer a contrast color
````swift
JustHUD.setBackgroundColor(color: UIColor.white, automaticTextColor: true)
````  
![](http://i.imgur.com/4nIV6gW.png)

- Or show in a window
````swift
JustHUD.shared.showInWindow(window: window, withHeader: "Loading", andFooter: "Please wait...")
````  

- Hide the HUD
````swift
JustHUD.shared.hide()
````

- Check if HUD is already being displayed
````swift
if JustHUD.shared.isActive {
    print("Currently showing HUD")
} else {
    print("HUD is currently hidden")
}
````


