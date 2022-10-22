# Software Design and Architecture in Haskell

A structured set of materials on how to build real-world applications in Haskell.

---------

### Table of Contents

* [Books on Software Design and Architecture in Haskell](#Books-on-Software-Design-and-Architecture-in-Haskell)
* [Application Architectures](#Application-Architectures)
* [Design Approaches and Design Patterns](#Design-Approaches-and-Design-Patterns)
  * [Free Monads](#Free-Monads)
  * [Final Tagless / mtl](#Final-Tagless--mtl)
  * [Effect Systems](#Effect-Systems)
  * [ReaderT Pattern](#ReaderT-Pattern)
  * [Service Handle Pattern](#Service-Handle-Pattern)
  * [Other Patterns](#Other-Patterns)
  * [OOP Design Patterns vs FP Design Patterns](#OOP-Design-Patterns-vs-FP-Design-Patterns)
  * [Comparison of Approaches](#Comparison-of-Approaches)
  * [Comparison Table](#Comparison-Table)
* [Design Principles](#Design-Principles)
* [Philosophy](#Philosophy)
* [Best Practices & Guidelines](#Best-Practices--Guidelines)
  * [Exceptions](#Exceptions)
  * [Style Guides](#Style-Guides)
* [Showcase Projects & Code Organization Samples](#Showcase-Projects--Code-Orgranization-Samples)
* [Haskell in Production. Success Stories, Experience Reports](#Haskell-in-Production--Success-Stories--Experience-Reports)
* [Talks](#Talks)
* [Haskell Ecosystem and Accessibility](#Haskell-Ecosystem-and-Accessibility)
  * [Haskell Ecosystem and Community](#Haskell-Ecosystem-and-Community)
  * [Haskeller Competency Matrix](#Haskeller-Competency-Matrix)
  * [Haskell Learn: Books](#Haskell-Learn-Books)
* [Misc](#Misc)

--------

# Books on Software Design and Architecture in Haskell

- [Functional Design and Architecture (Second Edition)](https://www.manning.com/books/functional-design-and-architecture) | **Alexander Granin**
- [Production Haskell](https://leanpub.com/production-haskell) | **Matt Parsons**
- [Algebra-Driven-Design](https://leanpub.com/algebra-driven-design) | **Sandy Maguire**
- [Practical Haskell. A Real World Guide to Programming](https://www.apress.com/gp/book/9781484244791) | **Serrano, Alejandro**
- [Real World Haskell](http://book.realworldhaskell.org/) | **Bryan O'Sullivan, Don Stewart, John Goerzen**
- [Up-to-date Real World Haskell](https://github.com/tssm/up-to-date-real-world-haskell) | **Bryan O'Sullivan, Don Stewart, John Goerzen, Tae Sandoval**
- [Haskell Design Patterns](https://www.oreilly.com/library/view/haskell-design-patterns/9781783988723/) | **Ryan Lemmer**
- [The Simple Haskell Handbook](https://leanpub.com/simple-haskell-book) | **Marco Sampellegrini**
- [Haskell And Yesod](https://www.yesodweb.com/book) | **Michael Snoyman**

# Application Architectures

- [Three Layer Haskell Cake](https://www.parsonsmatt.org/2018/03/22/three_layer_haskell_cake.html) | **Matt Parsons**
- [A Modern Architecture for FP](http://degoes.net/articles/modern-fp) | **John A De Goes**
- [Modern Functional Programming: Part 2](http://degoes.net/articles/modern-fp-part-2) | **John A De Goes**
- [Anatomy of a Haskell-based Application](https://abailly.github.io/posts/cm-arch-design.html) | **abailly**
- [Architecture of a Real World Haskell Application](https://www.onikudaki.net/blog/archives/6) | **Michael Oswald**
- [Functional architecture - The pits of success](https://m.youtube.com/watch?v=US8QG9I1XW0) | **Mark Seemann** | NDC Sidney 2016
- [Hierarchical Free Monads: The Most Developed Approach In Haskell (And The Death Of Final Tagless)](https://github.com/graninas/hierarchical-free-monads-the-most-developed-approach-in-haskell/blob/master/README.md) | **Alexander Granin**
- [Hierarchical Free Monads and Software Design in Functional Programming (Talk)](https://youtu.be/3GKQ4ni2pS0) | [Slides](https://docs.google.com/presentation/d/1SYMIZ-LOI8Ylykz0PTxwiPuHN_02gIWh9AjJDO6xbvM/edit?usp=sharing) | **Alexander Granin** | FunctionalConf 2019, Bangalore, India
- [Hexagonal Architecture and Free Monad: Two related design patterns?](https://www.pinterest.ru/pin/791929915696726474/#amp) | **Quentin Duval**
- [Large-scale design in Haskell? (SO question)](https://stackoverflow.com/questions/3077866/large-scale-design-in-haskell)

# Design Approaches and Design Patterns

### Free Monads

- [Why free monads matter](http://www.haskellforall.com/2012/06/you-could-have-invented-free-monads.html) | **la Gonzalez**
- [Free monads in 7 easy steps](https://joa.sh/posts/2015-09-13-free-monad-steps.html) | **joa**
- [A Modern Architecture for FP](http://degoes.net/articles/modern-fp) | **John A De Goes**
- [Building network actors with Node Framework](https://gist.github.com/graninas/9beb8df5d88dda5fa21c47ce9bcb0e16) | **Alexander Granin** | _Note: a Free monadic architecture is described there._
- [Automatic White-Box Testing with Free Monads](https://github.com/graninas/automatic-whitebox-testing-showcase) | **Alexander Granin** | [Showcase](https://github.com/graninas/automatic-whitebox-testing-showcase)
- [Hierarchical Free Monads: The Most Developed Approach In Haskell (And The Death Of Final Tagless)](https://github.com/graninas/hierarchical-free-monads-the-most-developed-approach-in-haskell/blob/master/README.md) | **Alexander Granin**
- [Hierarchical Free Monads and Software Design in Functional Programming (Talk)](https://youtu.be/3GKQ4ni2pS0) | [Slides](https://docs.google.com/presentation/d/1SYMIZ-LOI8Ylykz0PTxwiPuHN_02gIWh9AjJDO6xbvM/edit?usp=sharing) | **Alexander Granin** | FunctionalConf 2019, Bangalore, India
- [Strict typing fun example — Free Monads in Haskell](https://www.endpoint.com/blog/2016/03/11/strict-typing-fun-example-free-monads) | **Kamil Ciemniewski**
- [Free Monads: from the basics to the implementation of composable and effectful stream processing](https://deque.blog/2017/11/13/free-monads-from-basics-up-to-implementing-composable-and-effectful-stream-processing/) | **Quentin Duval**
- [What does Free buy us?](https://www.parsonsmatt.org/2017/09/22/what_does_free_buy_us.html) | **Matt Parsons**
- [Combining free monads in Haskell](https://blog.ploeh.dk/2017/07/24/combining-free-monads-in-haskell/) | **Mark Seemann**
- [Free monad considered harmful](https://markkarpov.com/post/free-monad-considered-harmful.html) | **Mark Karpov**
- [What is the “Free Monad + Interpreter” pattern? (SO question)](https://softwareengineering.stackexchange.com/questions/242795/what-is-the-free-monad-interpreter-pattern#)
- [A Practical Introduction to Freer Monads (Eff)](https://captjakk.com/posts/2019-05-12-practical-intro-eff.html) | **Keagan McClelland**

### Final Tagless / mtl

- [Tagless Final Encoding in Haskell](https://jproyo.github.io/posts/2019-03-17-tagless-final-haskell.html) | **Juan Pablo Royo**
- [Introduction to Tagless Final](https://serokell.io/blog/tagless-final) | **Vasiliy Kevroletin** | Serokell
- [Reducing boilerplate in finally tagless style](https://ro-che.info/articles/2016-02-03-finally-tagless-boilerplate) | **Roman Cheplyaka**
- [Tagless Final Encoding of a Test Language](https://wickstrom.tech/programming/2017/06/05/tagless-final-encoding-of-a-test-language.html) | **Oskar Wickström**

### Effect Systems

- [Eff to the Rescue!](https://mmhaskell.com/blog/2017/11/20/eff-to-the-rescue) | **Monday Morning Haskell**
- [Freer doesn’t come for free](https://medium.com/barely-functional/freer-doesnt-come-for-free-c9fade793501) | **Eric Torreborre**
- [Serving HTTP Content with Fused-Effects](https://blog.sumtypeofway.com/posts/serving-http-content-with-fused-effects.html) | **Patrick Thomson**
- [A Practical Introduction to Freer Monads (Eff)](https://captjakk.com/posts/2019-05-12-practical-intro-eff.html) | **Keagan McClelland**

### ReaderT Pattern

- [The ReaderT Design Pattern](https://www.fpcomplete.com/blog/2017/06/readert-design-pattern) | **Michael Snoyman**
- [The ReaderT design pattern or tagless final?](http://magnus.therning.org/posts/2019-02-02-000-the-readert-design-pattern-or-tagless-final-.html) | **Magnus Therning**
- [Capability: The ReaderT Pattern Without The Boilerplate](https://www.tweag.io/posts/2018-10-04-capability.html) | **Andreas Herrmann, Arnaud Spiwack** | Tweag.IO

### Service Handle Pattern

- [The Service Pattern](https://www.schoolofhaskell.com/user/meiersi/the-service-pattern) | **Simon Meier**
- [Haskell Design Patterns: The Handle Pattern](https://jaspervdj.be/posts/2018-03-08-handle-pattern.html) | **Jasper Van der Jeugt**

### Other Patterns

- [Haskell mini-patterns handbook](https://kowainik.github.io/posts/haskell-mini-patterns) | **Kowainik** (**Dmitrii Kovanikov**, **Veronika Romashkina**)
- [Haskell Design Patterns (Book)](https://www.oreilly.com/library/view/haskell-design-patterns/9781783988723/) | **Ryan Lemmer**
- [Enterprise Haskell Pattern: Lensed Reader](https://michaelxavier.net/posts/2016-04-03-Enterprise-Haskell-Pattern-Lensed-Reader.html) | **Michael Xavier**
- [The Has Type Class Pattern](https://hackernoon.com/the-has-type-class-pattern-ca12adab70ae) | **Jonathan Fischoff**
- [Type Class Patterns and Anti-patterns](https://hackernoon.com/type-class-patterns-and-anti-patterns-efd045c5af66) | **Jonathan Fischoff**

### OOP Design Patterns vs FP Design Patterns

- [Lambda the Ultimate Pattern Factory](https://github.com/thma/LtuPatternFactory) | **thma**

### Comparison of Approaches

- [Which Type-Safe Database Library Should You Use?](https://williamyaoh.com/posts/2019-12-14-typesafe-db-libraries.html) | **William Yao**
- [Revising application structure](http://felixmulder.com/writing/2020/08/08/Revisiting-application-structure) | **Felix Mulder**
- [Final Tagless vs Free Monad (Talk, Rus)](https://youtu.be/u1GGqDQyGfc) | [Slides (Eng)](https://drive.google.com/open?id=1VhS8ySgk2w5RoN_l_Ar_axcE4Dzf97zLw1uuzUJQbCo) | **Alexander Granin** | FPure 2019, Kazan
- [Monad transformers, free monads, mtl, laws and a new approach](https://ocharles.org.uk/posts/2016-01-26-transformers-free-monads-mtl-laws.html) | **Oliver Charles**
- [Backpack for initial and final encodings](https://qfpl.io/posts/backpack-for-initial-and-final-encodings/) | **qfpl**
- [Capability: The ReaderT Pattern Without The Boilerplate](https://www.tweag.io/posts/2018-10-04-capability.html) | **Andreas Herrmann, Arnaud Spiwack** | Tweag.io

### Comparison Table

Separate page:
- [Haskell Approaches Comparison Table](https://gist.github.com/graninas/1b7961ccaedf7b5cb92417a1599fdc99)

# Philosophy

- [Boring Haskell Manifesto](https://www.snoyman.com/blog/2019/11/boring-haskell-manifesto) | **Michael Snoyman** | [Reddit discussion](https://www.reddit.com/r/haskell/comments/dzx15d/boring_haskell_manifesto_by_michael_snoyman/)
- [The Haskell Pyramid](https://patrickmn.com/software/the-haskell-pyramid/) | **Patrick**
- [My thoughts on Haskell in 2020](https://alpacaaa.net/thoughts-on-haskell-2020/) | **Marco Sampellegrini**
- [Write Junior Code](https://www.parsonsmatt.org/2019/12/26/write_junior_code.html) | **Matt Parsons**
- [Fancy Haskell](https://dfithian.github.io/2019/12/30/fancy-haskell.html) | **Dan Fithian**
- [Simple Haskell Is Best Haskell](https://medium.com/@fommil/simple-haskell-is-best-haskell-6a1ea59c73b) | **Sam Halliday**
- [On Marketing Haskell](https://www.stephendiehl.com/posts/marketing.html) | **Stephen Diehl**
- [How to market Haskell to mainstream programmers](https://www.youtube.com/watch?v=fNpsgTIpODA) | Talk | **Gabriella Gonzalez**

# Design Principles

*Note. It's a big void here in these topics. We don't have any good materials about Design Principles applicable to Haskell.*

- Inversion of Control
- Dependency Injection
- Low Coupling / High Cohesion
- Rule of Least Power / Law of Demeter
- SOLID
- KISS
- YAGNI
- DRY

# Best Practices & Guidelines

- [Figuring Out How To Use Beam For DB Migrations](https://williamyaoh.com/posts/2019-09-27-figuring-out-beam-migrations.html) | **Willam Yao**
- [Making a small Haskell application](https://github.com/morteako/bitcoin) | **Morten Kolstad** 
- [Haskell practices](https://github.com/freckle/guides/blob/master/haskell-best-practices.md) | **freckle**
- [An opinionated guide to Haskell in 2018](https://lexi-lambda.github.io/blog/2018/02/10/an-opinionated-guide-to-haskell-in-2018/) | **Lexi Lambda**
- [Getting things done in Haskell (Talk)](https://www.youtube.com/watch?v=-X1vrxQUETM) |  **Jasper Van der Jeugt** | HaskellerZ, Feb 2018
- [Working around Haskell's namespace problem for records](https://gist.github.com/mtesseract/1b69087b0aeeb6ddd7023ff05f7b7e68) | **Moritz Clasmeier**

### Exceptions

 * [Exceptions Best Practices in Haskell](https://www.fpcomplete.com/blog/2016/11/exceptions-best-practices-haskell) | **Michael Snoyman** | FP Complete
 * [Asynchronous exception handling in Haskell](https://www.fpcomplete.com/blog/2018/04/async-exception-handling-haskell/) | **Michael Snoyman** | FP Complete
 * [Exceptions tutorial](https://markkarpov.com/tutorial/exceptions.html) | **Mark Karpov**
 * [The three kinds of Haskell exceptions and how to use them](https://www.tweag.io/blog/2020-04-16-exceptions-in-haskell/) | **Tweag**
 
### Style Guides

 * [Programming guidelines](https://wiki.haskell.org/Programming_guidelines)
 * [Kowainik's Haskell Style Guide](https://kowainik.github.io/posts/2019-02-06-style-guide)
 * [Tweag.IO's Haskell Style Guide](https://github.com/tweag/guides/blob/master/style/Haskell.md)
 * [Tibbe's Haskell Style Guide](https://github.com/tibbe/haskell-style-guide/blob/master/haskell-style.md)

# Showcase Projects & Code Orgranization Samples

Separate page:
- [Software Design Showcase Projects in Haskell](https://gist.github.com/graninas/49be74a21fbd58236bad28e1ce1eed94)

# Haskell in Production. Success Stories, Experience Reports

- [Why Haskell is our first choice for building production software systems](https://www.foxhound.systems/blog/why-haskell-for-production/)
- [The Joy and Agony of Haskell in Production](http://www.stephendiehl.com/posts/production.html) | **Stephen Diehl**
- [Haskell is Not For Production and Other Tales (Talk)](https://m.youtube.com/watch?v=mlTO510zO78) | **Katie Miller** | Linux.conf.au 2016 | Geelong, Australia
- [Production Haskell (Talk)](https://m.youtube.com/watch?v=AZQLkkDXy68) | **Reid Draper**
- Haskell in Production | **Felix Mulder**
  - [Haskell in Production](http://felixmulder.com/writing/2019/10/05/Haskell-in-Production.html)
  - [Designing Testable Components](http://felixmulder.com/writing/2019/10/05/Designing-testable-components.html)
- [Haskell in Production](https://blog.hasura.io/from-zero-to-hipster-haskell-in-production-97ea99d90c3b/) | Hasura.IO
- [5 Years of Haskell in Production (Talk)](https://youtu.be/hZgW4mT1PkE) | **Alexander Thiemann**
- [Retrospective: Haskell in Production](https://www.infoq.com/news/2016/08/haskell-production-retrospective/) | **Sergio De Simone**
- [My “Haskell In Production” Story](https://medium.com/@djoyner/my-haskell-in-production-story-e48897ed54c) | **David Joyner**
- [Introducing Haskell in Soisy](http://marcosh.github.io/post/2021/06/04/introducing-haskell-in-soisy.html)

# Talks

- [Getting things done in Haskell (Talk)](https://www.youtube.com/watch?v=-X1vrxQUETM) |  **Jasper Van der Jeugt** | HaskellerZ, Feb 2018
- [Your Second Haskell Web App—A Yesod Workshop with Michael Snoyman](https://www.youtube.com/watch?v=LEdEOlLlMfM) | **Michael Snoyman**
- [Functional architecture - The pits of success](https://m.youtube.com/watch?v=US8QG9I1XW0) | **Mark Seemann** | NDC Sidney 2016
- [Hierarchical Free Monads and Software Design in Functional Programming (Talk)](https://youtu.be/3GKQ4ni2pS0) | [Slides](https://docs.google.com/presentation/d/1SYMIZ-LOI8Ylykz0PTxwiPuHN_02gIWh9AjJDO6xbvM/edit?usp=sharing) | **Alexander Granin** | FunctionalConf 2019, Bangalore, India
- [Final Tagless vs Free Monad (Talk, Rus)](https://youtu.be/u1GGqDQyGfc) | [Slides (Eng)](https://drive.google.com/open?id=1VhS8ySgk2w5RoN_l_Ar_axcE4Dzf97zLw1uuzUJQbCo) | **Alexander Granin** | FPure 2019, Kazan
- [Haskell is Not For Production and Other Tales (Talk)](https://m.youtube.com/watch?v=mlTO510zO78) | **Katie Miller** | Linux.conf.au 2016 | Geelong, Australia
- [Production Haskell (Talk)](https://m.youtube.com/watch?v=AZQLkkDXy68) | **Reid Draper**
- [5 Years of Haskell in Production (Talk)](https://youtu.be/hZgW4mT1PkE) | **Alexander Thiemann**

# Haskell Ecosystem and Accessibility

This section is aimed to show that learning and using Haskell is not as horrible as some folks are trying to claim.

### Haskell Ecosystem and Community

- [State of the Haskell ecosystem](https://github.com/Gabriella439/post-rfc/blob/main/sotu.md) | **Gabriella Gonzalez**
- [2017 State of Haskell Survey results](https://taylor.fausak.me/2017/11/15/2017-state-of-haskell-survey-results/) | **Taylor Fausak**
- [2018 State of Haskell Survey results](https://taylor.fausak.me/2018/11/18/2018-state-of-haskell-survey-results/) | **Taylor Fausak**
- [2019 State of Haskell Survey results](https://taylor.fausak.me/2019/11/16/haskell-survey-results/) | **Taylor Fausak**
- [2020 State of Haskell Survey results](https://taylor.fausak.me/2020/11/22/haskell-survey-results/) | **Taylor Fausak**
- [The Haskell Pyramid](https://patrickmn.com/software/the-haskell-pyramid/) | **Patrick**
- [Haskell Survey Results 2018 (FP Complete)](https://www.fpcomplete.com/blog/2018-haskell-survey-results) | FP Complete

### Haskeller Competency Matrix

- [Haskeller Competency Matrix (separate page)](https://gist.github.com/graninas/833a9ff306338aefec7e543100c16ea1)

### Haskell Learn: Books

- [Get Programming with Haskell](https://www.manning.com/books/get-programming-with-haskell) | **Will Kurt**
- [Haskell in Depth](https://www.manning.com/books/haskell-in-depth) | **Vitaly Bragilevsky**
- [What I Wish I Knew When Learning Haskell](http://dev.stephendiehl.com/hask/) | **Stephen Diehl**
- [Haskell from the Very Beginning](https://www.haskellfromtheverybeginning.com/) | **John Whitington**
- [Learn You a Haskell for Great Good!]( http://learnyouahaskell.com/) | **Miran Lipovača**
- [Programming in Haskell](https://www.cs.nott.ac.uk/~pszgmh/pih.html) | **Graham Hutton**
- [Haskell And Yesod](https://www.yesodweb.com/book) | **Michael Snoyman**
- [The Simple Haskell Handbook](https://leanpub.com/simple-haskell-book) | **Marco Sampellegrini**
- [Production Haskell](https://leanpub.com/production-haskell) | **Matt Parsons**
- [Beginning Haskell: A Project-Based Approach](https://www.apress.com/gp/book/9781430262510) | **Serrano, Alejandro**
- [Practical Haskell. A Real World Guide to Programming](https://www.apress.com/gp/book/9781484244791) | **Serrano, Alejandro**
- [Parallel and Concurrent Programming in Haskell: Techniques for Multicore and Multithreaded Programming](http://shop.oreilly.com/product/0636920026365.do) | **Simon Marlow**
- [Real World Haskell](http://book.realworldhaskell.org/) | **Bryan O'Sullivan, Don Stewart, John Goerzen**
- [Haskell Design Patterns](https://www.oreilly.com/library/view/haskell-design-patterns/9781783988723/) | **Ryan Lemmer**
- [Functional Design and Architecture (Second Edition)](https://www.manning.com/books/functional-design-and-architecture) | **Alexander Granin**
- [Thinking with Types. Type-Level Programming in Haskell](https://thinkingwithtypes.com/) | **Sandy Maguire**
- [Algebra-Driven-Design](https://leanpub.com/algebra-driven-design) | **Sandy Maguire**
- [Haskell Programming from First Principles (aka Haskell Book)](https://haskellbook.com/) | **Chistopher Allen, Julie Moronuki**
- [Optics by example](https://leanpub.com/optics-by-example) | **Chris Penner**
- [A type of programming](https://atypeofprogramming.com/) | **Renzo Carbonara**
- [The Haskell School of Music: From Signals to Symphonies](https://www.amazon.com/Haskell-School-Music-Signals-Symphonies/dp/1108416756) | **Paul Hudak, Donya Quick**
- [Algorithm Design with Haskell](https://www.amazon.com/Algorithm-Design-Haskell-Richard-Bird/dp/1108491618) | **Richard Bird, Jeremy Gibbons**
- [Thinking Functionally with Haskell](https://www.amazon.com/Thinking-Functionally-Haskell-Richard-Bird/dp) | **Richard Bird**
- [Haskell: The Craft of Functional Programming](https://www.amazon.com/Haskell-Functional-Programming-International-Computer/dp/0201882957) | **Simon Thompson**
- [Practical Web Development with Haskell](https://www.amazon.com/Practical-Web-Development-Haskell-Applications-ebook/dp/B07FP523HS) | **Ecky Putrady**
- [Haskell Data Analysis Cookbook](https://www.packtpub.com/product/haskell-data-analysis-cookbook/9781783286331)

### Misc

- [HASKELL DOCUMENTATION WITH HADDOCK: WISHES'N'TIPS](https://kowainik.github.io/posts/haddock-tips#top-level) | **Veronika Romashkina**, **Dmitrii Kovanikov** (Kowainik)
- [Appendix to Software Design in Haskell](https://gist.github.com/graninas/ef5dd5a2b57903af81039fb21ff3b0bf)
  - [Testing](https://gist.github.com/graninas/ef5dd5a2b57903af81039fb21ff3b0bf#Testing)
  - [Final Tagless](https://gist.github.com/graninas/ef5dd5a2b57903af81039fb21ff3b0bf#Final-tagless)
  - [Records](https://gist.github.com/graninas/ef5dd5a2b57903af81039fb21ff3b0bf#Records)
  - [Exceptions and Error Handling](https://gist.github.com/graninas/ef5dd5a2b57903af81039fb21ff3b0bf#Exceptions-and-Error-Handling)
  - [Build Tools](https://gist.github.com/graninas/ef5dd5a2b57903af81039fb21ff3b0bf#Build-Tools)
