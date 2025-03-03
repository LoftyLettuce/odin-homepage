# git-homepage
Problem: control svg as a background
Solution: Viewbox of svg can't style with css and don't know how to 
stretch the path element so using div with clip-path as an alternatives

Problem: clip-path doesn't cast shadow
Solution: the shadow already be hidden by clip-path itself, so you 
have to use clip-path on div:after and drop-shadow on div. More 
details: https://css-tricks.com/using-box-shadows-and-clip-path-together/. Turn out
the filter: drop-shadow drop shadow on the visible part of an element no matter its its child or not.

Problem: image stop shrinking at certain width for no reason
Explanation: image have their own min-width, so you have to overide them

Problem: width work with image but flex-basis does not
Explanation: the css priotize width of the content before flex-basis, and the flex-basis cannot be smaller than the width of the content