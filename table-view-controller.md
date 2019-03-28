# Table View Controller

Cheat sheet version 1.0 by Makzan. 2019-03-21.

# Static vs Dynamic

## Static = Setup in Storyboard

- Good for UI building.
- Good for quick prototyping.

## Dynamic = Setup in Code

- Good for displaying records.
- Good for long list.
- Good for detail controlling every aspect.

# Table View Style

- plain
- grouped

## Plain 

- Good for records listing
- e.g. Contact list

## Grouped

- Good for app-like vertical view.
- Section to separate different parts of UI.
- Section header for part header.
- Section footer for 

# Hierarchy

Table view is composed by multiple sections. 
**Section** includes multiple rows. 
Each **row** uses a **cell** to display content.

## Cell — Dequeue with Identifier

`dequeueReusableCellWithIdentifier`

Different type of cell should use different identifier.

- image view
- accessory
- accessory view

## Cell style

- Custom
- Basic
- Right Detail
- Left Detail
- Subtitle

## Cell Accessory

- Checkmark (✔️)
- Disclosure Indicator (>)
- Detail (Info Button)
- Detail Disclosure (Info Button with >)

# Delegates

The following two protocols are automatically included in `UITableViewController`.

- UITableViewDataSource
- UITableViewDelegate

# UITableViewDataSource

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