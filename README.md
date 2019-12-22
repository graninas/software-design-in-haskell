# WIP

# software-design-in-haskell
Software Design in Haskell. A structured set of materials. How to build real-world applications in Haskell.


# Books on Software Architecture in Haskell

- Functional Design and Architecture, Alexander Granin
  https://graninas.com/functional-design-and-architecture-book/

- Practical Haskell. A Real World Guide to Programming, Serrano, Alejandro
  https://www.apress.com/gp/book/9781484244791
  TODO: read and assess

- Real World Haskell, Bryan O'Sullivan, Don Stewart, and John Goerzen
  http://book.realworldhaskell.org/


# Application Architectures

- Three Layer Haskell Cake. Matt Parsons
  https://www.parsonsmatt.org/2018/03/22/three_layer_haskell_cake.html

- A Modern Architecture for FP, John A De Goes
  http://degoes.net/articles/modern-fp

- (Talk) Hierarchical Free Monads and Software Design in Functional Programming, Alexander Granin, FunctionalConf 2019, Bangalore, India
  Talk https://youtu.be/3GKQ4ni2pS0
  Slides

- Hexagonal Architecture and Free Monad: Two related design patterns?
  https://www.pinterest.ru/pin/791929915696726474/#amp
  NOTE: TODO: read and assess
  
- Anatomy of a Haskell-based Application
  https://abailly.github.io/posts/cm-arch-design.html
  NOTE: TODO: read and assess
  
- Architecture of a Real World Haskell Application
  https://www.onikudaki.net/blog/archives/6
  
- Large-scale design in Haskell?
  https://stackoverflow.com/questions/3077866/large-scale-design-in-haskell
  
# Design Principles

# Design Approaches

### Free Monads

- Why free monads matter, Gabriel Gonzalez
  http://www.haskellforall.com/2012/06/you-could-have-invented-free-monads.html

- Free monads in 7 easy steps
  https://joa.sh/posts/2015-09-13-free-monad-steps.html
  
- A Modern Architecture for FP, John A De Goes
  http://degoes.net/articles/modern-fp
  
- Automatic White-Box Testing with Free Monads. Alexander Granin
  https://github.com/graninas/automatic-whitebox-testing-showcase
  
- Building network actors with Node Framework. Alexander Granin
  https://gist.github.com/graninas/9beb8df5d88dda5fa21c47ce9bcb0e16
  
- (Talk) Hierarchical Free Monads and Software Design in Functional Programming, Alexander Granin, FunctionalConf 2019, Bangalore, India
  Talk https://youtu.be/3GKQ4ni2pS0
  Slides
  
- Strict typing fun example — Free Monads in Haskell
  https://www.endpoint.com/blog/2016/03/11/strict-typing-fun-example-free-monads
  
- Free Monads: from the basics to the implementation of composable and effectful stream processing
  https://deque.blog/2017/11/13/free-monads-from-basics-up-to-implementing-composable-and-effectful-stream-processing/

- What does Free buy us? Matt Parsons
  https://www.parsonsmatt.org/2017/09/22/what_does_free_buy_us.html
  
- What is the “Free Monad + Interpreter” pattern?
  https://softwareengineering.stackexchange.com/questions/242795/what-is-the-free-monad-interpreter-pattern#

- Combining free monads in Haskell, Mark Seemann
  https://blog.ploeh.dk/2017/07/24/combining-free-monads-in-haskell/
  TODO: assess. Note: Unnecessary type level machinery to combine Free monads, functors & interpreters

### Final Tagless / mtl

- Tagless Final Encoding in Haskell, Juan Pablo Royo
  https://jproyo.github.io/posts/2019-03-17-tagless-final-haskell.html

- Introduction to Tagless Final, Vasiliy Kevroletin, Serokell
  https://serokell.io/blog/tagless-final
  Note: wrong statements about Free Monads

- Reducing boilerplate in finally tagless style, Roman Cheplyaka
  https://ro-che.info/articles/2016-02-03-finally-tagless-boilerplate

- Tagless Final Encoding of a Test Language,
  https://wickstrom.tech/programming/2017/06/05/tagless-final-encoding-of-a-test-language.html

# Design Patterns

### ReaderT Pattern

- The ReaderT Design Pattern. Michael Snoyman
  https://www.fpcomplete.com/blog/2017/06/readert-design-pattern

- The ReaderT design pattern or tagless final? Magnus Therning
  https://wickstrom.tech/programming/2017/06/05/tagless-final-encoding-of-a-test-language.html

- Capability: The ReaderT Pattern Without The Boilerplate
  https://www.tweag.io/posts/2018-10-04-capability.html

### Service Handle Pattern

- The Service Pattern. Simon Meier
  https://www.schoolofhaskell.com/user/meiersi/the-service-pattern
  TODO: read and assess

- Haskell Design Patterns: The Handle Pattern. Jasper Van der Jeugt
  https://jaspervdj.be/posts/2018-03-08-handle-pattern.html

### Other Patterns

- (Book) Haskell Design Patterns. Ryan Lemmer
  https://www.packtpub.com/application-development/haskell-design-patterns
  https://www.oreilly.com/library/view/haskell-design-patterns/9781783988723/
  TODO: read and assess

- Enterprise Haskell Pattern: Lensed Reader. Michael Xavier
  https://michaelxavier.net/posts/2016-04-03-Enterprise-Haskell-Pattern-Lensed-Reader.html
  TODO: read and assess

- The Has Type Class Pattern. Jonathan Fischoff
  https://hackernoon.com/the-has-type-class-pattern-ca12adab70ae
  TODO: read and assess
  
- Type Class Patterns and Anti-patterns. Jonathan Fischoff
  https://hackernoon.com/type-class-patterns-and-anti-patterns-efd045c5af66
  TODO: read and assess
  

### OOP Design Patterns vs FP Design Patterns

- Lambda the Ultimate Pattern Factory
  https://github.com/thma/LtuPatternFactory


### Effect Systems

### Comparison of Approaches

- Monad transformers, free monads, mtl, laws and a new approach
  https://ocharles.org.uk/posts/2016-01-26-transformers-free-monads-mtl-laws.html

- Backpack for initial and final encodings
  https://qfpl.io/posts/backpack-for-initial-and-final-encodings/
  Note: benchmarks

- Capability: The ReaderT Pattern Without The Boilerplate
  https://www.tweag.io/posts/2018-10-04-capability.html
  TODO: Comparison of what?
  
- (Talk) Final Tagless vs Free Monad, Alexander Granin, FPure 2019, Kazan
  Talk (Rus) https://youtu.be/u1GGqDQyGfc
  Slides (Eng)

# Testing

# Frameworks

- Yesod

- RIO

- Node

- Hydra

- PureScript Presto

- PureScript Presto.Backend

# Code Orgranization Samples

# Haskell in Production. Success Stories, Experience Reports

- Haskell in Production
  TODO: read and assess
  - Haskell in Production
    http://felixmulder.com/writing/2019/10/05/Haskell-in-Production.html
  - Designing Testable Components
    http://felixmulder.com/writing/2019/10/05/Designing-testable-components.html

# Phylosophy

- Boring Haskell Manifesto. Michael Snoyman
  https://www.snoyman.com/blog/2019/11/boring-haskell-manifesto
  Reddit discussion: https://www.reddit.com/r/haskell/comments/dzx15d/boring_haskell_manifesto_by_michael_snoyman/

- The Haskell Pyramid
  https://patrickmn.com/software/the-haskell-pyramid/

# Talks

- Hierarchical Free Monads and Software Design in Functional Programming, Alexander Granin, FunctionalConf 2019, Bangalore, India
  Talk https://youtu.be/3GKQ4ni2pS0
  Slides

- Final Tagless vs Free Monad, Alexander Granin, FPure 2019, Kazan
  Talk (Rus) https://youtu.be/u1GGqDQyGfc
  Slides (Eng)

# Misc

- TODO: Table with Software Design discipline topic coverability
- Boring Haskell substet voting

### Read, Assess & Classify

- Haskell Design Patterns: Service-Oriented Programming
  https://github.com/jaspervdj/jaspervdj/blob/master/drafts/2015-01-30-haskell-design-patterns-services.markdown

- How do you design programs in Haskell or other functional programming languages?
  https://softwareengineering.stackexchange.com/questions/72557/how-do-you-design-programs-in-haskell-or-other-functional-programming-languages

- Where are all the functional programming design patterns?
  https://softwareengineering.stackexchange.com/questions/89273/where-are-all-the-functional-programming-design-patterns
  TODO: read and extract info


# Haskell Learn

TODO: Is this section needed?

### Books

- Get Programming with Haskell, Will Kurt
  https://www.manning.com/books/get-programming-with-haskell

- Haskell in Depth. Vitaly Bragilevsky
  https://www.manning.com/books/haskell-in-depth

- What I Wish I Knew When Learning Haskell. Stephen Diehl
  http://dev.stephendiehl.com/hask/

- Haskell from the Very Beginning, John Whitington
  https://www.haskellfromtheverybeginning.com/

- Learn You a Haskell for Great Good!, Miran Lipovača
  http://learnyouahaskell.com/

- Programming in Haskell, Graham Hutton
  https://www.cs.nott.ac.uk/~pszgmh/pih.html

- Parallel and Concurrent Programming in Haskell: Techniques for Multicore and Multithreaded Programming, Simon Marlow
  http://shop.oreilly.com/product/0636920026365.do
