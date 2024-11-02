---
layout: post
title: "Urban Design Critique Platform"
date: 2024-10-10
categories: projects
---

**Description**: This is a cute website I envision that would act like a mini reddit, but for urban design fails. I would like to implement an in-browser or lightweight large language model to help the layman make better comments.

**Inspiration**: Bus stops designed with pillars very close to the road, which block the view of buses, and making commuting by public transport feel like a sad and thoughtless experience. This is in contrast to high quality infrastructure that clearly take the human experience into account that you can find in other major cities.

There's a lot more similar things I'd like to share, and I thought a comment section would let other residents give weight to my concerns, share their own experiences, or even disagree that it is a problem at all.

However, the layman only has an intuition about whether it's good or bad, and doesn't have vocabulary to talk about it. Comments can also get very stale if it's only people agreeing or disagreeing, or complaining even more. 

**Implementation**:
1) A warning to the commenter if they are repeating a point someone else has made. Could be implemented using embeddings and cosine similarity.

2) A suggestion to the commenter about what they can write. For example, "Name 3 things you dislike about this." , "Which specific parts of your neighbourhood do you also see this?", "Think about what kind of city user you are - student, parent, caregiver - and how this affects you". This can come from a pre-made question bank, augmented with post-specific questions that are generated in the backend by a large language model based on the title, location, and description of the post.

3) Prompts as the person writes a comment. These prompts can be about what the writer missed out. Or it can introduce perspectives on-the-go. For example, if someone writes about hating raised zebra crossings because it is bumpy to drive over, it can prompt a description of why raised zebra crossings are good with regards to safety and comfort for the pedestrian, why a pedestrian might find it good, and what sources and studies have influenced cities around the world to adopt such a feature. 
However, this feels too computationally expensive to do as it requires an LLM to parse and provide a response whenver there is a natural pause in the writing.