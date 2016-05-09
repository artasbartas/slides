# Introducing Contentful
### An API-first content management platform
## David Jenkins / Fred Pullin

![](https://images.contentful.com/256tjdsmm689/6eVeSgMr2EsEGiGc208c6M/1d45b9ef4d393d23298016a84f10d8b7/contentful-logo.png)

---

<!-- -- data-background="https://media.giphy.com/media/l3V0rRnYN185HInLi/giphy.gif" data-background-size="contain" data-state="blur" -->

# The Big Shift

^ We're seeing a huge shift in how online media is consumed and created

---
<!-- -- data-background="https://media.giphy.com/media/l3V0rRnYN185HInLi/giphy.gif" data-background-size="contain" data-state="blur" -->

### Ways of consuming and creating content evolve

- Mobile dominates everything
- Social networks are huge
- Rise of API ecosystem
- New technologies proliferate
- Faster innovation all-around

^ Mobile dominates everything: Mobile is used for everything - surfing, entertainment, shopping - and by a lot of people, so publishers have to ensure greate mobile experience or lose their mindshare. 

Social networks are huge: Users spend lots of time on Facebook, Twitter, Snapchat, Instagram and myriads of other social networks. So publishers have to follow and offer compelling experiences on these platforms.

Rise of API ecosystem: There are many great businesses out there offering amazing solutions - payment (Stripe, Braintree), shopping cart (Snipcart), comments (Disqus), shipping (Shipwire), sms (Twillio), transactional email (Sendgrid) - but to access them you need to integrate via API. 

New technologies proliferate: We are seeing technologies that allow to do more, easier and faster both on the backend (node.js, AWS lambda, blockchain), frontend (javascript frameworks, HTML5), mobile (Swift), but to take advantage of them, you need to work with decoupled architecture.

Faster innovation all-around: Robots learnt to walk, AI to play Go, and cars to drive. Online publishers, similarly, are getting smarter and faster unveiling new business models, distribution channels and revamped products. If you want to keep up, you have to speed up your own development cycle to the point where you can credibly compete.

---

<!-- -- data-transition="concave" data-background="#ff0000" -->

# Growing 
# out of touch

^ Legacy vendors struggle to adapt to the new realities, because their bottomline depends on all business models and it would take their engineers many years to reinvent their tech stack

---

### Traditional CMS vendors struggle to adapt

- Highly processed content
- Authoring and presentation layers are mixed up
- APIs are added as an afterthought <!-- {_class="fragment highlight-red"} -->
- Bloated application
- Single server architecture <!-- {_class="fragment fade"} -->

^ Highly processed content: Legacy CMS mix up content with markup (HTML attributes) and metadata (personalization tags) and fail to define individual fields (you can't know if it's a string or a decimal number).

Authoring and presentation layers fused into one: Legacy CMS use some sort of templating framework, which severely restricts what one can do on the front end, plus mix up authoring and presentation components in a way that is very hard to separate. 

APIs are added as an afterthought: That means they are implemented on old, complex platforms like JAVA or .NET, lack understandable documentation, are hard to debug, only expose a small part of methods available internally and almost without exception fail to provide an authoring API (that is APIs are strictly for content delivery).

Bloated application: You might want to buy just content authoring tool, but the legacy vendors would insist that you buy translation, analytics and personalization modules too, because they are already built into the package. This results in three problems: a high price tag, long implementation cycle, and terrible user experience.  

Single server architecture: Legacy vendors are learning to use the cloud, but they are not awfully good at it so far. This means that they charge customers a lot of money, while failing to live up to uptime, availability and reliability benchmarks set by pure-play SaaS businesses.

---

<!-- -- class="stretch" data-background="http://poignant.guide/images/2007-cover-shut.jpg" -->

# Contentful's 
# secret idea 

^ We might be a young company, but we are bringing to the table some bold technical ideas, which are likely to dominate the publishing world for decades to come. 


---

<video class="stretch" data-autoplay src="http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4"></video>
### Here's what makes us special

- Pure content
- Microservice architecture
- Cloud service

^ Pure content: We treat content in a different way than other CMS vendors. This means that content is stored in pure form, with presentational elements, business logic and meta data stripped out. Our content is typed, which means that we always know what type of input we store in a given field. And we store content as JSON documents, a lightweight and scalable format. When taken together, these features result in structured content, whose defining feature is that it can be easily consumed by any platform.

Microservice architecture: Our application is architected in a special way - we have decoupled 4 APIs, which allow to users to perform all usual actions programmatically. Our authoring stack (where draft document live) and our delivery stack (where published documents live) are completely independent of each other. And our internal application components communicate asynchronously via the message bus. This means that our application is very resilient, can be scaled easily, is unlikely to keel over if any one component will unexpectedly die, and can be developed further without major headaches.

Cloud service: Our application is natively built in the cloud and we've been working for several years now to optimize our performance. This gives us distinct competitive advantages. First, we run a lean operation, which keeps our costs low, but automatically provision more resources to meet spikes in demand, which makes us reliable (our CDA uptime for the last year was 100%). Secondly, we integrate tightly with a bunch of CDN providers and have built advanced caching techniques into our application, which is why our APIs respond so fast (average of 100 ms). Finally, running in the cloud makes us very resilient, because for any given system there is a backup system ready to be automatically deployed at a moment's notice and we simply outsource the boring parts of the system to the Amazon itself. 

---

<!-- -- data-background="https://media.giphy.com/media/l3V0rRnYN185HInLi/giphy.gif" -->

# Compelling 
# benefits

^ On a practical level, our unique approach to managing content yields a number of benefits to organizations working with us

---
{.slide: data-background="//giphy.com/embed/l3V0rRnYN185HInLi?html5=true"}

### Why use our platform?

- API magic 
- Blazing performance
- Development ecosystem
- Secure by default
- Lighter cost base

^ API magic: Our APIs enable developers to do interesting things (since we support authoring, preview, image transformations and delivery) out of the box (because our API is almost self-explanatory) and with awesome results (since we have so many cool features in the api, like geo-search, link resolution, value type definitions).

Blazing performance: We thought about speed from the scratch, which means that we avoided architectural solutions which penalize speed (serving content from the DB, mixing together delivery and authoring, not having a caching layer) plus we invested into services and made sure that our content delivery is blazing fast (thanks to the use of multiple CDN providers, not just one, default optimizatio of images, and reduction of API response payloads, autoscaling and more).

Development ecosystem: We have a robust ecosystem around our product which covers SDKs for popular languages (currently 9), example apps and demos, a constant stream of practical guides on how to integrate Contentful with other tools, and plenty of space for customizing the product to ones need inside (roles and permissions, webhooks, custom widgets, languages, UI extensions, content modelling). Then we also play nicely with javascript frameworks like Angular and React. Put togerthe that results in ability to build proof of concept projects in a matter of days, not quarters like it is with legacy vendors.

Security: Although we did not talk much about it, but operating in the cloud + having cleverly architected application + a bunch of extremely smart engineers + round the clock monitoring makes us much more reliable than CMSses running on internal servers of our corporate clients. 

Cost: We are an order of magniture cheaper than traditional vendors. Cost savings accrue from several sources: first our licenses are ~5 to 10 times cheaper than those of traditional vendors. We then eliminate the need to pay for services like hosting, monitoring software, security scans and so on. Customizing our solution to customer's needs is super fast a week vs. 6-9 months it takes with legacy systems. Plus Contentful gives customers the advantage of always being on the newest platform without doing anything. With legacy providers customers need to upgrade manually every few years and that costs easily couple millions dollars. 

---

# Real-life 
# scenarios

^ Customers use contentful for a number of very distinct scenarios.

---
### Popular Contentful use cases

- Static website CMS
- mobile Backend-as-a-Service (mBaaS)
- Backend-as-a-Service (BaaS)
- Cross-platform publishing
- IoT CMS
- Content repository

^ Authoring interface for a static website
  mobile Backend-as-a-Service (mBaaS) powering a native mobile app (or a smartwatch)
  Backend-as-a-Service powering an interactive website or a single page application (SPA)
  CMS for cross-platform publishing, including things like Snapchat, Apple TV, and Facebook 
  CMS for Internet-of-Things (IoT) devices, including beacon campaigns, smart fridges and car dashboards
  Content repository for aggregating content or preserving it for future use

---

# Questions?

![](https://images.contentful.com/256tjdsmm689/NsISSSI382WM0ECkkOI8O/02ff66bcf554ba70e6e1f3bddc75dfb2/Dani.jpg?h=650&)



