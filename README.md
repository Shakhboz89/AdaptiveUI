# AdaptiveUI

Description: Make an app that adapts for all screen sizes and orientations with Auto Layout.

Setting up 

In this technique there is no coding. You will primarily use Storyboard to lay out the
user interface components and learn how to use auto layout and size classes to make the
UI adaptive.
First, open up Xcode, and create a new project using the Single View Application template.
Name the project Auto Layout and make sure to select Universal for the device option.
Now, open Main.storyboard. in Interface Builder, you should find a view controller that
has the size of an iPhone 8.

Creating the Project 1

Let's start to design the app UI. Download the image pack http://www.github.com/Shakhboz89/ and import images to Assets.xcassets.
Now go back to the storyboard and drag an image view from the Object Library to the view controller. Set it width to 375 and height to 390. Make sure that you choose image view and go to the Attributes Inspector, set the image to "love" and the mode to "Aspect Fill".
Next, drag a View to the view controller and put it under the image view. This View as a container for other UI components like labels, buttons. In Size Inspector set the width to "375" and height to "277".

// PUT SCREENSHOT HERE //

Let's drag a Label to the View and change the label to "Love is...". Set the font to "Avenir Next" and its size to "25 points". 
// Optional: Press "CMD+=" to resize the label and make it fit.
In the Size Inspector change the value of X to "15" and Y to "15".
Drag another label and place it under the previous label, in Attributes Inspector change the text to "Love encompasses a range of strong and positive emotional and mental states, from the most sublime virtue or good habit, the deepest interpersonal affection and to the simplest pleasure.", then set the font to "Avenir Next" and change the font size to "18" points and the Numbel Of Lines to "0".
Switch to Size Inspector, change the value of X to "15", Y to "58" and set the width to "352", height to "182".
Check that the two labels placed inside the View. If you do everuthing correctly, your screen should look similar to this: 

// PUT SCREENSHOT HERE //

Now your app's UI is perfect for iPhone 8 or  4.7-inch screen. Let' s take a quick test to check out the look and feel of the design on different devices.
You can use the Preview Assistant, which lets you evaluate the resulting design on different size displays at one time.
To use the Preview Assistant open the Assistant pop-up menu > Preview (1), then press and hold the option key, and click Main.storyboard (Preview).

// PUT SCREENSHOT HERE //

Xcode will display a preview of the app' UI in the assistant editor. By default, it shows you the preview of your selected iOS device. You can click the + button at the lower-left corner of the assistant editor to get a preview of an iPhone 8 Plus and other devices. As you can see, the current design doesn't look good on all devices except iPhone 8. We haven't defined any auto layout constraints. This is why the view doesn't fit properly on all devices.

Auto Layout Constraints

Now select the image view and click the Pin Button on the auto layout menu to create spacing constraints. For the left, top and right sides set the value to "0". Make sure the "Constrain to margin" option is unchecked, because we want to set the constraints relative to the super view's edge. Now click the "Add 3 Constraints" button.

// PUT SCREENSHOT HERE //

Open Document Outline and Control-drag from the Image View to the main View. When promted, select "Equal Heights" from the pop-up menu.

// PUT SCREENSHOT HERE //

Now in the Document Outline select Equal Heights constraint, the constraint should appear in the Constraint section and go to the Size Inspector. Here you can edit the value of the constraint to change its definition.

// PUT SCREENSHOT HERE //

Set the First Item to "love.Height" and the Second Item set to "Superview.height". If not, you can click the selection box of the first item and select "Reverse First and Second item". By default the value of the multiplier is set to "1", which means the love image view takes up 100% of the main view. The image view should only take up around 60% of the main view. So change the multiplier from "1" to "0.585". 

Next, select View and click the Pin Button. Select the left, right and bottom sides and set the value to "0". Make sure that the "Constraint to margin" option is unchecked and click the "Add 3 Constraints" button. This adds three spacing constraints for the View.

// PUT SCREENSHOT HERE //

Now let's define the necessary constraints for the two labels.
Select the title label, which is the one with the larger font size. Click the Pin Button. Set the value of the top side to "15", left side to "15" and right side to "15" and make sure the "Constaint to margins" is unchecked and click "Add 3 Constraints".

// PUT SCREENSHOT HERE //

Next, select other label and add spacing constraints fot the 




Here I will show all the adaptive concepts such as size classes by building a universal app, the app supports all available screen sizes and orientations.


![iPhone 8](https://user-images.githubusercontent.com/46559168/54486921-ed0ce500-48b0-11e9-9c5f-99ca5ed185c5.png)

![iPhone 8 Plus Landscape](https://user-images.githubusercontent.com/46559168/54486942-41b06000-48b1-11e9-892f-bdd5f2dd12e8.png)

![iPhone XS Max](https://user-images.githubusercontent.com/46559168/54486946-4543e700-48b1-11e9-90a6-2c9a024cef7f.png)

![iPad Pro 12 9](https://user-images.githubusercontent.com/46559168/54486950-4bd25e80-48b1-11e9-9e77-ba2bd3fc941c.png)

![Five](https://user-images.githubusercontent.com/46559168/54486952-51c83f80-48b1-11e9-8cb1-81c4ddf9d11a.png)



