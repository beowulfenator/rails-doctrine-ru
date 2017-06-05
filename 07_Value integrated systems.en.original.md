Value integrated systems

Rails can be used in many contexts, but its first love is the making of integrated systems: Majestic monoliths! A whole system that addresses an entire problem. This means Rails is concerned with everything from the front-end JavaScript needed to make live updates to how the database is migrated from one version to another in production.

That’s a very broad scope, as we’ve discussed, but no broader than to be realistic to understand for a single person. Rails specifically seeks to equip generalist individuals to make these full systems. Its purpose is not to segregate specialists into small niches and then require whole teams of such in order to build anything of enduring value.

It is this focus on empowering the individual that points to the integrated system. It’s in the integrated system we can cut out many needless abstractions, reduce the duplication between layers (like templates on both the server and the client), and, above all, avoid distributing our system before we absolutely, positively have to.

Much of the complication in systems development comes from introducing new boundaries between the elements that restrict how you make calls between A and B. Method calls between objects is far simpler than remote procedure calls between microservices. There’s a whole new world of hurt in failure states, latency issues, and dependency update schedules that await those who venture into the lair of distribution.

Sometimes this distribution is simply necessary. If you want to create an API to your web application that other people can call over HTTP, well, then you just have to suck it up and deal with many of these issues (although handling requests inbound rather than sending them outbound is much easier – your downtime is someone else’s failure state!). But that’s at least a limited amount of damage inflicted on your own personal development experience.

What’s worse is when systems are prematurely disintegrated and broken into services or, even worse, microservices. This drive frequently starts from the misconception that if you want a Modern Internet Application, you’ll simply have to build the systems many times over: Once on the server side, once on the JavaScript MVC client-side, once for each of the native mobile applications, and so forth. This is not a law of nature, it needn’t be so.

It’s entirely possible to share large chunks of the entire application across multiple apps and accesses. To use the same controllers and views for the desktop web as for embedded in native mobile apps. To centralize as much as possible within that glorious, majestic monolith: The integrated system.

All this without giving up much if anything in terms of speed, user experience, or other attributes that falsely draw developers to premature distribution.

That’s the have-most-of-it-all we seek: All the power of individually tuned and distributed applications with the ease-of-use and understanding of a single, integrated system.