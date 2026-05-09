In the past decades, software engineering teams are faced with ==a phenomenon who’s challenges== are becoming more and more pressing: They’re being put under the management of non-technical managers. In the early years of software development, the nerds were among themselves. Today, however, they increasingly find themselves being placed in teams that include many non-technical managers and auxiliary support roles alongside experienced software engineers.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*A9yqxzU_NPj0uxs2CtW3QA.png)

Goodbye non-technical software manager?

I’ve seen it myself and I have been there multiple times in the past 25 years of my software engineering career. As a manager, CTO, consultant, and business owner. When software engineering teams are placed under direct non-technical management, the first reaction is a shock. That shock isn’t coming from developers rejecting any “outsiders”, but roots in real world experiences. Experiences include a high churn of technical people, cost explosions, and sometimes even business foreclosures. This article covers what engineering teams can expect, what non-technical managers need to reflect on, why the success for non-technical managers with software is almost impossible, and how it seems to be coming to an end now.

## Where are these managers coming from?

Back in my days, over 20 years ago, software development was a craft done by awkward coffee addicted nerds. Businesses who needed software, and customization thereof, would refer to professional software companies. These would take the businesses through a guided process, such as the Rational Unified Process (RUP). They would define the requirements, estimate the necessary work and implement the solutions that would solve the businesses’ problems. Software was such a nieche novelty that no business managers in their right mind would try to do it themselves.

![](https://miro.medium.com/v2/resize:fit:1144/format:webp/1*Kv2pnxnr7w4E8X1FJxSihA.png)

Rise of high-tech jobs in the late 1990s ( State of Wyoming; 1998)

With the rise of the Internet and growing popularity of computers, smartphones and apps, more and more businesses started software projects and built up in-house software teams themselves. In the early 2000s, the software industry transitioned from an weird bunch of people into a seemingly neverending hype cycle. Being “a tech guy” was no longer frowned upon, but became “hip”. A highly sought after profession. That transition opened up the flood gates for “gold diggers”, people who were in it purely for the money, not the excitement of software itself.

### Rise of the auxiliaries

A lot of auxiliary jobs appeared: Product Managers, Scrum Masters, Product Owners, Business Analysts, QA Managers, and whatnot. ==In some instances, the number of people with auxiliary tasks even outnumbered actual software engineers in development teams.== Some companies have “software” teams that purely manage outsourced development while holding little to no professional experience in software management. It’s a fatal misjudgement to think that anyone can do software management just because they can use a computer.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*_h2uTWkmXfwz5yPx)

Number of full-time Alphabet employees from 2007 to 2024 ( Statista )

Since these non-technical people aren’t overly interested in a deep dive into software internals or software management, they seek to rise up the ranks quickly. And they very often do. Coming from a variety of backgrounds, these people do not just lack the professional experience in managing software and development teams, they also totally lack the institutional education around it. Although often with an economic background, their institutional eduction never covered the quirks of virtual products that rely on ongoing research and development.

## Misunderstanding of software economics

Previously, a “technology company” was strictly defined as either a “hardware manufacturer” or a “software manufacturer.” Hardware companies produced semiconductors or systems largely composed of them. Software companies developed software for these semiconductors, which they sold or leased to customers who wanted to use it. By that strict definition, neither Uber, eBaym nor Airbnb were considered actual “tech companies”. They don’t produce hardware composed of semiconductors, and their core business has nothing to do with licensing or leasing software to customers who wish to use it. Before 2015, the number of actual software businesses in the United States even stagnated.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*4PIPZojS7qLYN7jyuQ8pCg.png)

Data aggregated from the US Census Bureau (County Business Patterns), IBISWorld, and industry reports.

### Look at me, I’m the tech company now!

The term “technology company” changed from an economic definition to a social frenzy. So much so that it hardly even makes any sense to debate what that actually is. [ISO 18245](https://en.wikipedia.org/wiki/ISO_18245) defines different merchant categories to allow financial institutions the identification of the nature of a business. The MCC code “5045” defines a merchant for “Computers, Computer Peripheral Equipment, Software”. When ISO 18245 was introduced in 2003, anyone who fell under “MCC 5045” was considered a “tech company”. But when you book a ride with Uber, your transaction isn’t categorized as “5045”. It is categorized as “4121”, which is “Taxicabs and Limousines” (see the full [List of Merchant Category Codes](https://www.citibank.com/tts/solutions/commercial-cards/assets/docs/govt/Merchant-Category-Codes.pdf)). Your Netflix subscriptions falls under “4899” (Cable, Satellite, and Other Pay Television). Yes, you heard it, your bank identifies Netflix’ subscriptions as a plain old cable bill.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*jzOCi87pOkmwEzOtoc4hrg.png)

Merchant category codes for technology companies, as categorised by the financial industry

Uber’s reported business metrics and KPIs are vastly different to those of Microsoft and Apple. Before Android and cloud computing, both Amazon and Google also weren’t really “tech companies”. They were classified as retail and advertising services. This invasion of “software companies” into other industries blurred the line between the software industry and any other. Suddenly, a lot more businesses became self proclaimed “tech companies”. Businesses that had no relationship or experience with the “management of uncertainty” in R&D, virtual products and engineering teams. Even worse, these businesses often don’t even need it.

### When you are your only customer

Netflix is a service business operating under the same economic conditions as a cable television provider. No business other than Netflix operates Netflix’ software. If they make a change to their software, they only need to deploy it to their own environment, managing their own data. There’s no migration plan to be discussed with hundreds of customers, no license agreement updates, and no customers refusing to upgrade. Netflix itself is its own software’s sole customer. No one knows how many, how often, and what updates to the core software are done.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*2vFytVW0RqoCGyA_.png)

Metaflow (Open Source): one of Netflix’ very rare software product releases

Now, Netflix is a very professional organization that understands this. But many other businesses, especially outside of California, very often don’t. For these, mostly non-technical business, important topics such as software risks, maintainability, economic sustainability of software, and uncertainty of research and development don’t matter. These businesses see software as merely an evil necessity of the modern world, required for them to achieve whatever actual business targets they have.

Netflix grew because traditional cable companies, and their contracted publishers, refused to accept the Internet. They failed and refused to provide modern alternatives to DVD rentals and pricey pay TV offerings. Netflix focused on users and useful technology, becoming the beloved media and entertainment company that it is today. A software company it is not, as its CEO Reed Hastings confirmed: “ [Netflix isn’t a media company or a technology company — it’s an entertainment company](https://www.cnbc.com/2020/09/09/reed-hastings-netflix-isnt-tech-or-media-its-entertainment.html) ”.

## Non functional, you say?!

A key mistake by non-technical managers, that I regularly observed over the last 20 years, is the ignorance of non-functional requirements. Why bother with something that has no functional value to the user? These managers never learned or experienced how unmaintainable software changes time-to-market from weeks into years, and can ultimately bring the entire development to a standstill.

> A **non-functional requirement (NFR)** defines the specific criteria used to judge the operation of a software system rather than its specific behaviors or features. While functional requirements dictate what the system does (e.g., “the user can log in”), NFRs describe how the system performs or its overall quality attributes, such as **scalability**, **security**, **usability**, and **reliability**. Essentially, they act as the constraints or performance standards that ensure the system is effective, maintainable, and provides a positive user experience.

Most non-technical managers are afraid to allocate 20–30% of their engineering capacity to NFRs. Simply because they lack the arguments needed to justify that in front of their, also non-technical, upper management. Even worse, they are so pressured to deliver new features and functionality that they’re willing to totally sacrifice NFRs for it.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*VWb_a2mfipPE1F0RXhYkAQ.png)

Source: Compiled from U.S. Bureau of Labor Statistics (BLS), Administrative Office of the U.S. Courts

Every successful software business tracks KPIs around NFRs at the executive board level. Healthy software businesses need to ensure their products remain maintainable, and thus time-to-market remains short. Professional software managers are very well aware that a collapse of their codebase results in extremely expensive, often year long, refactoring of the same. ==When rewriting a codebase becomes cheaper than maintaing it, the codebase essentially collapsed and the product is dead.==

### Stacking tech debt like there’s no tomorrow

When you ignore NFRs, tech debt is no longer just slowly dripping into your product, it will turn into a giant avalanche burrying it. It’s not the increased volume of tech debt that will cause most of the harm, but the severity of it. An ongoing stream of tightly coupled dependencies, overloaded callstacks and broken encapsulations will create lethal consequences. Consequences that may not be experienced immediately, but will cause the slow death of the product through slowly but steadily increasing time to markets month after month while the software becomes ever more unmaintainable.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*M7qgKZ0aofmMeg2PvhJSHQ.png)

Tech debt: Reclaiming tech equity — McKinsey

Experienced software managers often dedicate Fridays to NFR assessment, and plan for longer cool off periods after larger releases. Teams will get around 20% of the initial development time to cool off. They’ll use that time to assess the damages from the last release. They create new NFRs, bug fixes and adjustments to be scheduled for the next releases. Non-technical managers hardly ever do that. They rush from one large release to another, often forcefully demanding development teams to fix bugs like they’re a bunch of labourers in a 19th century factory.

### Architectures designed to collapse

Decoupling in distributed system architectures isn’t something the average person generally discusses, and thus non-technical managers mostly don’t know what that is. Encapsulation and logical separation of components and systems is delegated to the individual developer, while non-technical managers constantly make decisions that jeopardize it. Contradicting decisions of non-technical managers are one of the root causes for developer churn in such teams. Such decisions by manager without technical background isn’t ill intended, it’s merely a lack of knowledge.

With the arrival of Scrum and “agile as a buzzword”, prolongued design phases are essentially abolished and squeezed into each development iteration (i.e. “Sprint”). Instead of working with architects to carefully craft sustainable changes into the codebase, developers are forced to smear numerous small architectural misconceptions into it. It’s these small misconceptions that lead to the described lethal consequences.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*ZJHWC-B8tHF1_T76.png)

High coupling and low cohesion is a common symptom in poorly managed software

Building sustainable architectures takes more time initially. Taking a shortcut or entirely abolishing the design of software architectures is done at the cost of long-term maintainability. What is saved in development time initially will backfire in future developments, but at a much higher cost.

Non-technical managers are incapable of identifying architectural issues in their products and systems. If they do, it’s often way too late. As much as with spaghetti code, spaghetti architectures cause unmaintainable landscapes that result not just in a collapse of the codebase, but a collapse of the entire system landscape.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*F8WyLavkjDhbrbPRlSWVpw.png)

Entangled call stacks are a symptom of problematic architectures (see System Calls In Apache )

Spaghetti architectures cause 10–20x cost hikes in operating and development cost. Most managers without a technical background aren’t able to connect the dots between the architectural decisions and the cost. The moment they realize the dramatic cost explosions, the architectural debt is already so widely spread that large scale rearchitecting and refactoring are unavoidable. That doesn’t just cause headache for the finance department, but severely hurts competitiveness. If your competitor operates its systems at 10% of your cost, your business can’t compete.

## Research lab?! No, we’re agile!

Managers without software experience love the term “MVP” which refers to a “Pilotsystem” prototype, as academically researched by [Christiane Floyd](https://en.wikipedia.org/wiki/Christiane_Floyd) in [“A systematic look at prototyping”](http://www.piapetersen.dk/aktuelrhs/floyd-prototyping.pdf) and [Reinhard Budde](https://www.researchgate.net/profile/Reinhard-Budde) in “ [Approaches to Prototyping](https://books.google.de/books/about/Approaches_to_Prototyping.html?id=ik0gAQAAIAAJ&redir_esc=y) ”, both published in 1984. Someone entirely unfamiliar with these basics of Computer Science will have a very hard time deciding on what prototyping to best apply when. They’ll have to rely and trust their technical teams to make the right decisions. Teams that often don’t have the authority to make these decisions, and then mostly don’t.

Lacking the necessary experience, managers will almost always pick the Pilotsystem (aka “MVP”). They’re simply unable to notice the situations in which a “Lab Prototype” (aka “throw-away prototype”) is necessary. Before building the first iPod, Apple created dozens of lab prototypes to research the technology and evaluate the technical feasibility of the device.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*b6aPKdNyWRnn9RWq.png)

Oversized lab prototype of Apple’s first iPod

As a software team, you’re likely not inventing the next iPod. Yet, lab prototypes are necessary to identify interface and component risks, and try to solve them before building out the full product. This can be as simple as a lab prototype for ML models and Computer Vision for your company’s iPhone app. Without the lab prototyping approach, development teams will have to face interface risks during constructions. Something that may require costly rewriting at a later stage.

I have yet to find a non-technical manager that understands the necessity of prototyping, and what prototyping approach to use when. My personal experience is plastered with dozens of delayed projects and project cost overruns, because managers did not understand the nature of managing uncertainties in software development. In many of these cases, a lab prototype would’ve easily identified, and solved blockages. It would’ve done so at a fraction of the cost long before the project really took off.

Non-technical managers associate a lab with something that belongs into biological and pharmaceutical research, not in the development process of a software. They often pay homage to Steve Jobs, but completely ignore his path. Worse, they often seem to believe they know better.

### Software is not an inflated gearbox

When I say “non-technical managers”, I mean managers with no experience and educational background in software engineering specifically. Mechnical engineers can also be considered as “non-technical” when they do not possess the necessary background in software engineering. While they do have certain engineering knowledge and a much higher success rate with software projects, they bring along their very own challenges. Most notably a lack of understanding for virtual products and the associated vastly different economics of it.

Software isn’t a gearbox, it’s not set in stone, or rather metal in this case. Metallurgy has very little power here. Software can be updated over the air, on the go, and can update itself. That completely changes the way research and development is done. A gearbox can perfectly function and be serviced for decades, even when the vendor no longer supports it. Software can’t. It’s dead the moment the vendor ends support for it. No one other than the vendor can service the software’s codebase, and thus the software itself.

![](https://miro.medium.com/v2/resize:fit:1324/format:webp/1*Ytoo-RhufKRpcmnKvX9bsQ.png)

Key differences between software engineering and mechanical engineering

Mechanical engineers tend to impose the processes from mechanical engineering onto the software development process. This is almost as bad as not managing the development lifecycle at all. While mechanical engineers love to claim that software engineers aren’t engineers, the opposite is true as well. Mechanical engineers aren’t naturally born for software. Software has next to no production cost, only research and development. Virtual goods, such as software, can be multiplied by a simple copy operation on a disk. Gearboxes can’t, and that puts both disciplines into entirely different circumstances.

## Shiny object syndrome

I cannot write about non-technical managers in software engineering and software management without talking about the shiny object syndrome. It’s just way too prevalent in people who lack the necessary knowledge to make decisions on software systems and components. Many inexperienced software developers also regularly fall for it.

> Shiny object syndrome is the situation where people focus undue attention on an idea that is new and trendy, yet drop it in its entirety as soon as something new can take its place. (Wikipedia)

When you’re tasked with building a mobile app, what “tech stack” do you use? React Native, Flutter or native Kotlin on Android and Swift on iOS? The answer of any experienced software manager is: It depends on the requirements. If you’re unsure whether a certain technology meets requirements, you technically evaluate it with a proof of concept implementation. Once you technically evaluated your requirements, you make an informed decision. For each evaluated technology, you have sufficient arguments for and against it. You can explain these arguments and how you concluded your decision making step by step.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*OfrTQc1dgiCIeynJ)

Illustration of the Shiny Object Syndrome (Source: Rachel Pederson )

Non-technical managers hardly ever do that. It’s quite common that software teams under non-technical managers often need to evaluate technology not against specific requirements, but simply because their manager fell victim to a glossy sales pitch. With these managers, selection of components (i.e., “the tech stack”) often depends on sales pitches, marketing material or popularity, not the in-depth technical evaluation. Such decision making processes dramatically, and unnecessarily, inflate the risks of the software development process. They create technical debt long before the actual development even started.

## Falling off the learning curve

I started my professional career in software engineering over 25 years ago through an institutional education here in Germany. It took me 3 full years and resulted in a government-recognized certificate, certifying me as a software engineer. The educational path included dozens of books from various academic authors on software engineering, with thousands of pages. Even after going through that, I was still a greenhorn. Institutional education isn’t everything, but neither is practical experience. They both need to work hand in hand. Software managers need not just to know what the size of a pointer on iOS is, but also how to verify that.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*YSJ5kf0-2rbRE6KloB5jwQ.png)

Quick evaluation of the size of a pointer in Swift on macOS (surprise, it’s 64 bit or 8 bytes)

It took me less than a minute to quickly test the pointer size with [Swift Playgrounds](https://www.apple.com/de/swift/playgrounds/) on my Mac. You may now ask why a manager would need to able to evaluate the size of a pointer. I know at least a dozen computer science professors who would call for public prosecution for even asking. When talking to a senior manager from a well known tech giant in the bay area, she gave me the answer that I think describes it best.

> **“How do you intend to manage people who you have absolutely no idea of what they do all day, and can’t evaluate how they’re doing?”**

You’re hardly able to ensure that the company you work for stays ahead of the curve when you yourself are nowhere near it. Algorithms and data structures, software project management methods, object oriented programming, prototyping approaches, memory management, pointer arithmetic, machine learning and neural networks are taught for a reason.

The reality is that everyone who manages software projects without the necessary technical background will have to go through a steep learning curve for which managers actually do not have the time. Anyone who does not already bring the basic skills, will have almost no chance to keep up. The only hope for non-technical managers is to delegate everything other than bureaucracy to a subordinate, or survive long enough before the consequences hit. It’s a ticking time bomb for them.

### What training? I thought you knew how to program.

Software development teams need constant training. At least 20% of their work hours need to be dedicated to it. Otherwise, they will fall behind in technological developments. Without constant learning, engineers will continue to write endless lines of code in situations where others already train [BERT models](https://en.wikipedia.org/wiki/BERT_\(language_model\)), just to give an example.

Since a non-technical will itself not be on a continuous learning path, his subordinates won’t likely be either. If a software team, in this day and age, does not know when to write code, when to use a [Lazy Learner](https://en.wikipedia.org/wiki/Lazy_learning) (e.g., k-NN) or an [Eager Learner](https://en.wikipedia.org/wiki/Eager_learning) (e.g., BERT), they’ve already fallen far behind.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*RJLCjGcLuZowFOuI5ZFJkg.png)

Text classification model selection in Apple’s Create ML

An experienced software manager that is tasked with building a mobile app will be able to supervise the development team and ask questions like “Did you consider training an ELMo or BERT model for this instead of using a RegEx?”. A non-technical manager can’t and likely doesn’t even know what it is, how it works or what the advantages and disadvantages are. That person will just be freightened by the perceived complexity of “training your own model”, and the additional engineering effort upfront. Non-technical managers will simply refuse custom model training because they’ve read somewhere that it is expensive and only for “tech giants”.

Experienced software managers however know that training your own model is not witchcraft, but should be carefully evaluated against possible alternatives. In almost all cases that I went through, training existing models into customized ones is often the most economic method. Yet, it requires engineers to have the necessary skills and understanding. Something a software manager needs to ensure they have gotten.

## Demise of the non-technicals

I met people with CTO titles that got totally excited when they wrote their first line of code in Swift Playgrounds, like a child that baked muffins with a ready-made muffin mix for the first time in their life. I’m not kidding you. But the time for the non-technical managers in software, and the non-technicals in general, is ending. The cost is simply too high, the results aren’t really there, and the churn of software engineers in these teams speaks for itself. The hypetrain terminates here.

AI, namely LLMs like ChatGPT and Gemini, won’t make it easier for these people. They’ll make it worse. It’s like not visiting the doctor because you googled your symptoms and now apply medication for scabies, although you have a bacterial infection. Due to the increased productivity of professionals, there’s less need for non-technical people in auxiliary support functions of software developers. These are the ones who will drop out of software and technology first. The gold mine has run dry.

There are numerous first hand experiences of non-technicals making engineering decisions that are totally violating principles of software management taught even to first semester Computer Science students. And trust me, companies are starting to notice. All the described problems will multiply by several orders of magnitude with AI. Companies will implode faster than they can type “Ignore all previous instructions”.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*HqMqWKDRowLWngCC.png)

Job postings for software development are in decline ( Pragmaticengineer )

### Experienced programmers need to level up with AI

Average programmers will likely not survive the AI/ML tsunami either. The large majority of industry specific business software, in the form of expert systems, won’t survive. It’s not that AI will replace the developers of such software systems, but the entire systems themselves. In the near future, there’ll likely be customized agents with industry-specific tooling and ML models, carefully crafted by the most experienced software engineers.

![](https://miro.medium.com/v2/resize:fit:1270/format:webp/1*tFZquEZn3Z9SrRjEtTmQrg.png)

“ A method for studying natural language dialogue ” from John C. Thomas, 1976 (Source: U.S. DTIC)

I’m not making this up as it was already described on pages 164–190 of the publication “Human Factors and Interactive Computer Systems” by Yannis Vassiliou from the New York University, published right after the NYU Symposium on User Interfaces in New York on May 26th to 28th of 1982. Several years earlier, the publication “ [A method for studying natural language dialogue](https://apps.dtic.mil/sti/tr/pdf/ADA041288.pdf) ” from John C. Thomas in 1976 also explored the effects of natural language interaction with computers. What was early research back in the day has become a production-reality with LLMs.

The educational path of junior software engineers is already changing course towards a more ML and LLM model focused approach. Anyone who is comfortably sailing along in a.NET or Java role writing happy little business applications will have to seriously reconsider future options, depending on how long that person wishes to stay in the industry.

## Conclusion: Back to the future.

Non-technical managers in software and technology were, and in some places still are, a symptom of an overheated, overhyped and inflated computer technology sector. Computer technology as in the strict definition from the financial services industry, made up only of hardware and software businesses. The software industry’s burns are now healing. This is the hypetrain’s final stop as it terminates here.

The Matcha Latte ping pong table era with “A day in the life of whoever at whatever” is now over. Technically, software and hardware will advance into the future faster and further than ever before. Organisationally, and socially, software businesses will return to the pre-hype era, somewhere very similar to what it was around ‘98–2005.

We’re going back to the future.

Thank you for reading. Jan

*I’m a software business owner from Germany, worked in various CTO roles, an active programmer in C++, Go, Swift and passionate technology enthusiast. My programming career started at a young age and I later acquired a professional institutional education in software engineering. My journey on Medium started out as note taking and documenting my projects. Over time, it became more and more popular with you, my beloved readers. Not because I am someone special, but because people crave for thoroughly researched technical articles. Following me, clapping and subscribing is one step forward in keeping technical writing and its community alive.*
