# UWP App Visual Assets

## Overview

I created this project to help me understand where the various logos are employed within a Universal Windows Platform app (UWP app). The project contains unique images for each of the different visual assets, with text (where feasible) to indicate which scaling is in use.

### Important note

During the creation and testing of the project it became apparent that Visual Studio didn't always pick up on the changes to visual assets, especially if they're deleted and not replaced with something else. As a consequence, I recommend carrying out a clean build whenever an image is changed. 

## Tiles

Live tiles come in four different sizes: small, medium, wide and large.

### Small

Small lives tiles are created using the **Square 71x71 logo**, as shown below. 100% scaling is typically used on desktop computers, with the larger versions employed on the high-DPI displays found on mobile phones.

![Small live tile](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/VisualAssetsApp/Assets/Square71x71Logo.scale-100.png)

### Medium

Medium live tiles are created using the **Square 150x150 logo**. The **asset names** I'm using here match those shown in the Visual Assets tab of the Visual Studio 2015 package manifest editor.

![Medium live tile](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/VisualAssetsApp/Assets/Square150x150Logo.scale-100.png)

### Wide

Wide live tiles are created using the **Wide 310x150 logo**.

![Wide live tile](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/VisualAssetsApp/Assets/Wide310x150Logo.scale-100.png)

### Large

Large live tiles are created using the **Square 310x310 logo**. In testing this only appears to be available on desktop computers. 

![Large live tile](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/VisualAssetsApp/Assets/Square310x310Logo.scale-100.png)

## Icons

### Windows 10 Start menu

The icons displayed on the more conventional section of the Windows 10 Start menu are created using the **Square 44x44 logo**.

![Start menu icon](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/VisualAssetsApp/Assets/Square44x44Logo.scale-100.png)

Their appearance can be altered by setting the tile background colour. If this is set to `transparent`, the user's accent colour will show through. If a colour is specified, that is used instead. In this project I've specified the background colour to be `yellow`, which results in the following:

![Tile background colour](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/ScreenShots/TileBackgroundColour.png)

The Visual Studio 2015 icon gives an indication of what an icon with a `transparent` background would look like.

### Windows 10 taskbar

The taskbar icons are created using the **target size** versions of the **Square 44x44 logo**. The filename is important here. If you want a border around the icon use `Square44x44Logo.targetsize-xx.png`, where `xx` is 16, 24, 48 or 256:

![Taskbar icon with border](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/VisualAssetsApp/Assets/Square44x44Logo.targetsize-24.png)

If you don't want a border, use `Square44x44Logo.targetsize-xx_altform-unplated.png`:

![Taskbar icon with border](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/VisualAssetsApp/Assets/Square44x44Logo.targetsize-24_altform-unplated.png)

The differences when in use are shown below:

![Taskbar icon comparison](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/ScreenShots/TaskbarIcons.png)

The icon on the left has been shrunk to 16x16, leaving a border around it. The colour of the border is defined by the tile background colour discussed above. The icon on the right is full-size (24x24), with no border. **N.B.** The icon with the border is always scaled down, even if a 16x16 image is supplied.

## Notifications

### Toast notifications

Toast notifications use the **Square 44x44 logo**.

![Tile background colour](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/ScreenShots/ToastNotification.png)

### Lock screen notifications

Lock screen notifications use the **Badge logo**. Visual Studio suggests that these images should only use white or transparent pixels; partially-transparent white pixels are okay too, allowing for antialiasing effects. The image below shows the 24x24 pixel Badge logo on the lock screen. `B1` is the logo, and `64` is the notification value:

![Lock screen notification](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/ScreenShots/LockScreenNotification.png)

## Splash screen

The image displayed when the application launches uses the **Splash screen**.

![Splash screen](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/VisualAssetsApp/Assets/SplashScreen.scale-100.png)

The splash screen background colour can also be specified. In this project it's set to `pink`:

![Splash screen](https://raw.githubusercontent.com/paulthomson64/uwp-visual-assets/master/ScreenShots/SplashScreenBackground.png)
