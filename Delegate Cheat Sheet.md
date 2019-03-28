# Delegate Cheat Sheet

Version 1.0. 2019-03-21.

## Checklist to enable delegate.

1. Extend delegate protocol.
2. Point UIView delegate attribute to View Controller.
3. Implement methods from delegate.

## Common UIView with Delegate

- UITextFieldDelegate
- UITextViewDelegate
- UITableViewDelegate
- UITableViewDataSource
- UICollectionViewDelegate
- UICollectionDataSource
- UIScrollViewDelegate

## English Phrase

- `should` return true/false
- `will` informs that action will perform
- `did` informs that action was completed
- others returns what it is asking.

## UITextFieldDelegate

```swift
func textFieldShouldBeginEditing(_ textField: UITextField) -> Bool

func textFieldDidBeginEditing(_ textField: UITextField)

func textFieldShouldEndEditing(_ textField: UITextField) -> Bool

func textFieldDidEndEditing(_ textField: UITextField)

func textFieldDidEndEditing(_ textField: UITextField, reason: UITextField.DidEndEditingReason)

func textField(_ textField: UITextField, shouldChangeCharactersIn range: NSRange, replacementString string: String) -> Bool

func textFieldShouldClear(_ textField: UITextField) -> Bool

func textFieldShouldReturn(_ textField: UITextField) -> Bool
```

## UITableViewDataSource

```swift
override func numberOfSections(in tableView: UITableView) -> Int {
  // #warning Incomplete implementation, return the number of sections
  return 0
}

override func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
  // #warning Incomplete implementation, return the number of rows
  return 0
}

override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
  let cell = tableView.dequeueReusableCell(withIdentifier: "reuseIdentifier", for: indexPath)

  // Configure the cell...

  return cell
}
```

## UICollectionViewDataSource

```swift
override func numberOfSections(in collectionView: UICollectionView) -> Int {
  // #warning Incomplete implementation, return the number of sections
  return 0
}


override func collectionView(_ collectionView: UICollectionView, numberOfItemsInSection section: Int) -> Int {
  // #warning Incomplete implementation, return the number of items
  return 0
}

override func collectionView(_ collectionView: UICollectionView, cellForItemAt indexPath: IndexPath) -> UICollectionViewCell {
  let cell = collectionView.dequeueReusableCell(withReuseIdentifier: reuseIdentifier, for: indexPath)

  // Configure the cell

  return cell
}
```
