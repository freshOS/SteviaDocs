For both tableView cells and UICollectionView cells, `sv` adds the subviews to the `contentView`, as recommended.

## Example

```swift
class FriendCell: UITableViewCell {

    let avatar = UIImageView()
    let name = UILabel()

    required init?(coder aDecoder: NSCoder) { super.init(coder: aDecoder)}
    override init(style: UITableViewCellStyle, reuseIdentifier: String?) {
        super.init(style: style, reuseIdentifier: reuseIdentifier)

        sv(
            avatar,
            name.style(nameStyle)
        )

        avatar.size(50).centerVertically()
        alignHorizontally(|-20-avatar-name-20-|)
    }

    func nameStyle(l:UILabel) {
        l.font = .systemFontOfSize(24)
        l.textColor = .blueColor()
    }
}
```
Then in the viewController you do the usual `register` and `dequeue` :)
```swift
// In viewDidLoad, register your cell for dequeue
tableView.registerClass(FriendCell.self, forCellReuseIdentifier: "FriendCell")

// Later, in cellForRowAtIndexPath
let cell = tableView.dequeueReusableCellWithIdentifier("FriendCell", forIndexPath: indexPath) as! FriendCell
```
