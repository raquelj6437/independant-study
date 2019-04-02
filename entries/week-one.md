# Independent Study Week One Intro/Plan
My name is Raquel Joseph. I am embarking in a 9-week independant study. This is week one's entry.

#### Choosing a Topic
I have spent the first week exploring two languages: Swift and C#. I originally wanted to create my own version of the sims which is why I was looking into C#, but the I realized that it would be more innovative to create a mobile app. I decided that swift would be a good option for me. Even though creating an app on swift would not be the most marketable because majority of the human population uses android, 52.1 percent, I considered that it would allow me to focus sowly on apple products. Also, another reason I decided to study Swift was because I only own Apple products.

#### What is Swift?
[Swift](https://swift.org) is a powerful and intuitive programming language for macOS, iOS, watchOS, tvOS and beyond. Swift code is safe by design, yet also produces software that runs lightning-fast. Swift is the result of the latest research on programming languages, combined with decades of experience building Apple platforms. Swift is designed to work with Apple's Cocoa and Cocoa Touch frameworks and the large body of existing Objective-C code written for Apple products. It is built with the open source LLVM compiler framework and has been included in Xcode since version 6, released in 2014. 

#### The Beginning always starts with "Hello World"
In order to install swift I had 
1. to type
`xcode-select --install` in my terminal to install xcode. Swift was recently developed under xcode so this step was necessary.
2. then I had to type `brew install node` into my terminal. VSCode extensions are written in JavaScript / TypeScript. If you’re not already set up for JS development, you can download Node.
3. lastly I typed `npm --version` into my terminal to verify that you have a working installation.

To begin my study on swift, I thought to myself what would be the most basic form of swift. Then I figured that learning how Hello World would be a good way to start. Below is a snippit of the hello world that I tested.

```
*import UIKit

class ViewController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.
    }

    @IBAction func showMessage(sender: UIButton) {
        let alertController = UIAlertController(title: "Welcome to My First App", message: "Hello World", preferredStyle: UIAlertController.Style.alert)
        alertController.addAction(UIAlertAction(title: "OK", style: UIAlertAction.Style.default, handler: nil))
        present(alertController, animated: true, completion: nil)
    }
}
```
Swift is a very foreign language to me because the set up is not like HTML, Python, or Ruby. The set up is more complicated than ecpected so it took me by surprise. I then started to research a simplier way to start swift code but unfortunately the set up stayed the same. I decided to create a template for all my swift projects.


#### Takeaways
1. The first step into learning a new language or in other words “dip your toes in” is by starting with the basic “Hello World” code.
2. __Following installation steps are very important!__ At first I struggled to get my code to work and then I realized that it was because there were installation instructions that I completly disregarded.
3. Understand a new coding language may be difficult and discouraging but what you create/achieve in the end will be worth it.

#### Resources
https://www.appcoda.com/learnswift/build-your-first-app.html
https://nshipster.com/vscode/
https://swift.org