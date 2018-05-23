1、设置搜索 Logo

```swift
searchbar.setImage(R.image.header_search(), for: UISearchBarIcon.search, state: .normal)
```

2、设置字体

```swift
// 设置字体大小
if let tf = searchbar.value(forKey: "searchField") as? UITextField {
            tf.font = UIFont.PingFangSC(size: 12)
        }
```

