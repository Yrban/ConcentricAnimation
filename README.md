# ConcentricAnimation
A simple View that wraps a view and returns an animation using that view that has multiple copies of the view growing larger over time.

Creating this type of animation is not intuitive. Most try to make each view animate the entire way, from 0% to 100%. However, the best way this type of animation is to have the different views only animate a portion of the way where the next view takes over. This creates a smoother, more pleasing effect. This view wraps another view and animates the scale of the wrapped view, as well as optionally reducing the opacity so it simple disappears at 100% of size.

As a word of caution, using a scaleEffect on text can lead to blurring of the text. The better way to animate the size of text is to animate the size of the font. Of course, .font() is not animatable straight out of the box. It needs to be extended with an AnimatableModifier to get it working properly.
