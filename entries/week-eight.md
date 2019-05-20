# Week 8 Independent Study: Where do I begin?
This has been one of the hardest weeks in the independent study. This has also been one of the most busiest weeks of my life. My last highschool play was actually on saturday so I spent most of my well preparing and rehearsing for the play.

### Are we starting over?

Arieta and I both participated in the schools play. We realized that we had no time to really put in any work into this independant study. We decided that our original project would be too much for us to handle. We spent another few hours thinking of ways to make this app easier so that we can show what we learned while also creating something interesting.

### The new and final plan

The new project that we decided to make was Pong. We got inspiration for this game from our p5js projects. We decided to follow [pong tutorial](https://www.youtube.com/watch?v=LdL99CH23E8) becuase it was the most straight forward tutorial. In the end, we will add our own flair to it. Probably harder levels or every time the ball touches the paddle, it will get shorter making it harder for the user to hit the ball.

### What I learned

I learned how to make swift sprites and making them interact with eachother. You need to use something called SpriteKit which is already built into the OS. 

#### To install SpriteKit
```swift
let scene = GameScene(size: view.bounds.size)
let skView = view as! SKView
skView.showsFPS = true
skView.showsNodeCount = true
skView.ignoresSiblingOrder = true
scene.scaleMode = .resizeFill
skView.presentScene(scene)
```

#### Creating a sprite
``` swift
// 1
let player = SKSpriteNode(imageNamed: "player")
  
override func didMove(to view: SKView) {
  // 2
  backgroundColor = SKColor.white
  // 3
  player.position = CGPoint(x: size.width * 0.1, y: size.height * 0.5)
  // 4
  addChild(player)
}
```

#### Moving a sprite
``` swift
func random() -> CGFloat {
  return CGFloat(Float(arc4random()) / 0xFFFFFFFF)
}

func random(min: CGFloat, max: CGFloat) -> CGFloat {
  return random() * (max - min) + min
}

func addMonster() {
  
  // Create sprite
  let monster = SKSpriteNode(imageNamed: "monster")
  
  // Determine where to spawn the monster along the Y axis
  let actualY = random(min: monster.size.height/2, max: size.height - monster.size.height/2)
  
  // Position the monster slightly off-screen along the right edge,
  // and along a random position along the Y axis as calculated above
  monster.position = CGPoint(x: size.width + monster.size.width/2, y: actualY)
  
  // Add the monster to the scene
  addChild(monster)
  
  // Determine speed of the monster
  let actualDuration = random(min: CGFloat(2.0), max: CGFloat(4.0))
  
  // Create the actions
  let actionMove = SKAction.move(to: CGPoint(x: -monster.size.width/2, y: actualY),
                                 duration: TimeInterval(actualDuration))
  let actionMoveDone = SKAction.removeFromParent()
  monster.run(SKAction.sequence([actionMove, actionMoveDone]))
}
```

### Takeaways
1. Time management is important because if youre juggling many activities at once, time management will help you to organize your life so that youre not too stressed out.