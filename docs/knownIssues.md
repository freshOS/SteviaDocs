## Expression was to complex to be solved in reasonable time

*"Expression was to complex to be solved in reasonable time"* can happen in Stevia, since the swift compiler has a hard time finding the right `-` operator overload. However it usually only happens with very long horizontal layouts with multiple margins.

Here are three valid solutions for avoiding this annoying compiler error. All of them aim at making it easier for the compiler to find the right `-` operator version.

```swift
// Solution 1
// Putting margins in separate variables
let m:CGFloat = 15
let m2:CGFloat = 20
|-m-avatarImageView-m-userNameLabel-""-likeButton-m2-|

// Or Provide the type for margins to help the compiler
|-CGFloat(15)-avatarImageView-CGFloat(15)-userNameLabel-""-likeButton-CGFloat(20)-|

// Solution 2
// Breaking it into smaller layouts
|-15-avatarImageView-15-userNameLabel
likeButton-20-|

// Solution 3
// Using a double dash `--` version so that the compiler doesn't have to go through
// all the existing `-` operator overloads defined by UIKit/Foundation
|-15--avatarImageView--15--userNameLabel--""--likeButton--20-|
```
