---
title: Being right vs. being helpful
published: true
tags: advice
---

# Moving the needle

A few years into my career as a software engineer, I worked on a project that might sound familiar to some of you -- a monolithic legacy app that was painfully dated and being phased out with a microservice architecture. To help it succeed, the lead architect ran a recurring meeting where any of the engineers could bring up questions or concerns.

It was at one of these meetings where I brought up what I thought was an architectural shortcoming. Our microservices had a single data adapter interface to the monolithic backend. This posed a challenge for data migration, I argued, because it required an all-or-nothing switch of the single data adapter implementation to use a new data store. This kind of *big bang* change is notoriously difficult. "We need to switch to finer-grained data adapters!" I yelled, pounding the table (not really). The lead architect listened to me patiently, asking a few probing questions, before moving the meeting along to more pressing matters.

I bristled. I was brushed off despite raising a valid concern and spending time articulating the problem and coming up with a way forward! But in retrospect, the lead architect could tell pretty quickly I had devoted all of thought to this topic. It's why he opted to move the meeting along and send me an email later that day. He knew I had enough ammo to keep the discussion going on for a while and knew the outcome didn't matter in the grand scheme of things. In our particular instance, the point at which we would switch over our backend was so far into the future and the entire landscape so different that it made the conversation theoretical.

This is what he tried to convey to me in the email. He didn't address my rant about adapters directly but instead give me some unsolicited career advice that he felt I needed. The lead architect opened with how he's made some decisions in his career that people disagreed with -- strongly. It's a tough spot to be in. People get very passionate about big decisions and heated exchanges can be demoralizing and demotivating. The thing is, he said, is you want to take a stand for the things that "move the the needle forward". If you do that, you'll make decisions you believe in and skip the ones that are a waste of your career.

At the time it felt good that he took the time to impart this zen-like wisdom. But once the feeling faded, I realized I didn't know what moving the needle forward looked like. It was good advice in general -- the idea of making progress being your north-star -- but it could mean anything or nothing in my day-to-day work. The analogy of a two-dimensional gauge didn't feel helpful when it felt like I was making moves in five-dimensional space. Is slowly designing for a scalable future moving the needle forward? Is adding a feature as fast as possible moving the needle forward? Is fixing some flakey tests moving the needle forward. Of all the actions and decisions I could make in a given day, how do I know which ones will move the needle forward?

I didn't have the answer to these questions, so at the time I didn't dwell on the advice for very long. Over the course of my career I would, however, revisit this idea of "moving the needle forward". And I would eventually figure out what it meant for me. 

# Being right

A lot of what frustrated me early in my career, like my story about the microservice adapters, was a sense of being correct about things but never listened to or recognized for it. Hindsight, though, has shown me what that behavior was -- I was focused on being right without considering if I was being helpful. It's like interrupting a conversation to correct someone's grammar. You're technically correct, so no one disagrees; but you're not substantially contributing to the discussion, so no cares.

It's behavior that I think comes from my path into software engineering. As a  student I enjoyed and embraced the simplicity of outcomes in math classes. The problems only had two possible and inarguable results -- right or wrong. Compare that to a writing assignment, where I'd produce something that had things right, had things wrong, and plenty of space for me to disagree with my teacher on the amount of both. Like the human experience, it could be ambiguous, uncertain, and confusing.

Software engineering appealed to me as a career where'd I'd avoid that kind of messiness and instead take refuge in the certainty of outcomes. I imagined a job where I would only worry about getting code to compile and tests to turn green. Obviously, this wasn't an accurate picture of the profession. As I learned, the software world is a chaotic mix of industry fads, perceived market needs, shifting priorities, and inherited legacy cruft. In short, it's very much a human enterprise. 

I would refactor code according to SOLID principles, satisfied in my correctness but disappointed by it's muted reception. I'd increase test coverage, certain in its absolute goodness but never rewarded for it. I'd point out shortcomings in our architecture, proud of my knowledge but greeted by shrugs. In other words, I was correcting people's grammar, but not moving the needle.

# Being helpful

None of my work was inherently bad, but it was a lot of misguided energy. Over time, I've gotten better at guiding that energy. A lot of that growth could be attribute to asking myself, "Will this work result in a noticeable improvement in someone's life?" Not just a theoretical benefit that applies over time, like say the argument for refactoring code or or choosing a specific architecture, but a concrete one with a demonstrable benefit. I try to imagine who I'm doing the work for and whether they would notice the change if they weren't told. An example of this might be a performance optimization -- if the end user didn't notice the change then it was probably a poor use of my time.

It's worth clarifying that being helpful and being right aren't mutually exclusive; they should both be used as inputs to your decision making. For example, if you have an area of your code base that's complex, error prone, and the bane of every engineer at the company, then refactoring it will not go unnoticed. Compare that to repeatedly refactoring your greenfield project that has no clients and only one or two other engineers contributing -- you're not really helping anyone relative to the time and effort you're putting in.

Ideally you can be both helpful and right, but being right is harder to prove in an absolute way in complex systems. There's just too many competing factors. So if you're like me, consider placing more emphasis on how helpful your actions will be in your decision making process.