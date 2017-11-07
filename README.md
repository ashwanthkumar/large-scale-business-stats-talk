# Using Monoids for Large Scale Business Stats 

At Indix we collect and process lots of data. Most of our processing initially were done as MapReduce (henceforth MR) jobs but as our data grew in size we moved towards stream processing. We monitor the behaviour of our systems through collection of business metrics. It was relatively easy to write Stats jobs on our MR output but things got tricky when we moved to Stream based processing.

Our key learnings over the years have been

- Approximate stats now > Accurate stats tomorrow
- Our metrics were just aggregates (counts / uniques) with rollups
- Existing open source systems were more for system monitoring than business metrics
- Model aggregates as Commutative Monoids using [Algebird](https://twitter.github.io/algebird/typeclasses/monoid.html)'s typeclasses.

We put all our learnings and built a system called Abel which solved this for us. It aggregates a million events in ~15 seconds on a single box.

## About Author
Ashwanth Kumar is a Principal Engineer at Indix. His major interest lies in building and operating large data systems. When not dealing with data, he spends his time reading research papers in similar topics.

Abel as an idea was conceptualised by [Vinoth Kumar](https://github.com/vinothkr) while working at Indix as part of the Ingestion team.

## References
- [Evolution of stats @ Indix](https://speakerdeck.com/vinothkr/evolution-of-stats-at-indix) from Vinothkumar Raman
- [HyperLogLog Overview](https://docs.google.com/presentation/d/1vSsQIsXfwuntcja6zDySTTeq9fPahp4GZRlnrritTPQ/edit#slide=id.p) by Andrew Sy
- [Add ALL the Things: Abstract Algebra Meets Analytics](https://www.infoq.com/presentations/abstract-algebra-analytics) by Avi Bryant. One of the best introductions on Monoids and Algebird library.
- Video by [@brewkode](https://twitter.com/brewkode) on [Suuchi - Toolkit to build distributed systems](https://www.youtube.com/watch?v=GK0-ICFvIGw) at Fifth Elephant, 2017.
- [Zach Tellman - Everything Will Flow](https://www.youtube.com/watch?v=1bNOO3xxMc0)
- [Of Algebirds, Monoids, Monads, and Other Bestiary for Large-Scale Data Analytics](http://www.michael-noll.com/blog/2013/12/02/twitter-algebird-monoid-monad-for-large-scala-data-analytics/) by Michael G. Noll
- [Functional Programming in Scala](http://www.manning.com/bjarnason/) by P. Chiusano and R. Bjarnason, published by Manning. Includes chapters on monoids and monads, and how to implement them in Scala.

## Links
- https://github.com/ashwanthkumar/suuchi
- https://github.com/twitter/algebird
- http://riemann.io/
- http://kafka.apache.org/
- http://hadoop.apache.org/
- http://spark.apache.org/
- https://github.com/facebook/rocksdb

## Image Credits
- [Twitter by aguycalledgary](https://thenounproject.com/search/?q=twitter+bird&i=23267) from the Noun Project
- [team by Wilson Joseph](https://thenounproject.com/term/team/717083/) from the Noun Project
- [Earth by To Uyen](https://thenounproject.com/search/?q=internet+globe&i=318309) from the Noun Project
- [database by Kevin Woodland](https://thenounproject.com/search/?q=database&i=282705) from the Noun Project
- [options by Mert Güler](https://thenounproject.com/search/?q=toolkit&i=638516) from the Noun Project
- [SQL File by Viktor Vorobyev](https://thenounproject.com/search/?q=sql&i=342070) from the Noun Project
- [database by ✦ Shmidt Sergey ✦](https://thenounproject.com/search/?q=database&i=691819) from the Noun Project
- [sigma by Davo Sime from the Noun Project](https://thenounproject.com/search/?q=sigma&i=607382)
- [tools by Viktor Vorobyev from the Noun Project](https://thenounproject.com/search/?q=hammer&i=561830)
- [Info by Lance Weisser from the Noun Project](https://thenounproject.com/search/?q=info&i=91723)
- [Heart by i cons from the Noun Project](https://thenounproject.com/search/?q=heart&i=995105)

## License
[![Creative Commons License](https://i.creativecommons.org/l/by/4.0/88x31.png)](http://creativecommons.org/licenses/by/4.0/)  
<span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Using Monoids for Large Scale Business Stats</span> by [Ashwanth Kumar](https://speakerdeck.com/ashwanthkumar/using-monoids-for-large-scale-business-stats) is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).  

