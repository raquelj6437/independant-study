# Independent Study Week Six: The New App
We decided to name our app Clubraising. A play on fundrasing because it's an app where clubs can fundraise more efficiently.

### Divide and Conquor
Arieta and I decided that it would be more effective if we divided the project and come back together week 8 to put everything togther. I took on the challenge of creating a well working student side of the project while she took on creating the faculty side of the project.

### The Wireframe
![wireframe gif](app-wireframe.gif)

As you can see, I used the skills from week three to include multiple view in the app. I did not know how to connect the views when clicking a button so I had to google it. I learned that if you hold contro; and drag the button to the view you'd like to acces, it connects. I also learned how to make the collection view show up when you click theater. Originally, it was showing a blank page when launching clubraising even though everything was placed correctly in the view. I googled the problem and learned that you needed to call it from the code itself.

```swift
class MyCollectionViewCell: UICollectionViewCell {

@IBOutlet weak var myLabel: UILabel!
    
// tell the collection view how many cells to make
func collectionView(_ collectionView: UICollectionView, numberOfItemsInSection section: Int) -> Int {
    return self.items.count
}

// make a cell for each cell index path
func collectionView(_ collectionView: UICollectionView, cellForItemAt indexPath: IndexPath) -> UICollectionViewCell {

    // get a reference to our storyboard cell
    let cell = collectionView.dequeueReusableCell(withReuseIdentifier: reuseIdentifier, for: indexPath as IndexPath) as! MyCollectionViewCell

    // Use the outlet in our custom class to get a reference to the UILabel in the cell
    cell.myLabel.text = self.items[indexPath.item]
    cell.backgroundColor = UIColor.cyan // make cell more visible in our example project

    return cell
}

// MARK: - UICollectionViewDelegate protocol

func collectionView(_ collectionView: UICollectionView, didSelectItemAt indexPath: IndexPath) {
    // handle tap events
    print("You selected cell #\(indexPath.item)!")
}

}
```

In the gif is mostly what the student will see when using the app. What's missing is the part where students can actually checkout the items that they added to the cart.

We thought about the most efficent way for the student to find clubs in their school. If you noticed, when the student signs up, they are asked for a school code which each school is given so that they are only offered to buy from clubs in their school.
### Next Steps
My next steps are to include a database so that students can actually make an account. The database should be local which is the easiest way. I thought of using firebase but there are a lot of step in adding firebase to swift which I am not familiar with. I am, however, familiar with SQlite from using it in ruby. There is a swift version which I will learn from [SQLite: Local Database | Swift 4, Xcode 9](https://www.youtube.com/watch?v=c4wLS9py1rU).
### Takeaways
* Baby steps are okay. I thought that I would have to finish the student side completly by this week until I talked to Arieta and we agreed that we should create wireframes and have each veiw interact with eachother. Then the next week we will implement hard code.
* Patience is very important. I got frustrated a lot while creating the wireframe because when I launched the demo, it did not look the way I wanted it to. I felt like I was gonna fail. I wanted to just throw my laptop and give up, but then I thought to myself, how would it benefit me by giving up? I opened my laptop and finally figured out the bugs in my code. Patience is important expecially when learning a new language and trying to build an app.