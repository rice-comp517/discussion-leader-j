# Discussion leader assignment for Comp 417/517

In this assignment you will lead discussions and be
responsible for the following three elements:

1. Fill out paper review form
2. Short presentation highlighting key moves and
   contributions of the paper 
3. Facilitating discussion. 
 
## Review Form (25%)

Fill out and commit by midnight the night before: 

[Standard Review Form](./review.md)

Note for most of these sections, concision is preferred.
Provide 1-2 sentences if possible, of course go over if you
need.

## Presentation (25%)

The goal of leading the presentation is to format your
understanding of the paper from the perspective of a
critical reader. It is more an exercise to capture that
you've extracted the critical elements from the paper, as
well as a quick refresher to the class. 

The following slides are expected:

1. Title Page
2. Problem and Motivation
3. Why isn't it solved?
4. The key hypothesis of this paper?
5. The methods used to achieve it (how)?
6. The evaluation results
7. Key takeaways

The presentation should take between 5-12 minutes.

[Presentation](./unikernel.pdf)

## Discussion Leading (%25)

Develop 5-7 questions after reviewing the online discussion
and lead an initial 15 minute small group and a larger 15
minute discussion.

1. What are the tradeoffs between containers and unikernels? How would you choose between containers and unikernels?
2. Are you satisfied with or convinced by the security that unikernels claim to provide?
3. What are other potential use cases for unikernels?
4. Do you agree with writing system libraries in high level language? Why is using type safe languages important for unikernels?
5. MirageOS does not provide POSIX compatibility. Is it a good idea?

## Discussion Debrief (%25)

Answer the following questions: 

1. What new insights came out of the discussion?
- In my discussion group, people were concerned that the single address space model was not secure, because there was no separation between trusted code and distrusted code.
- People thought that unikernels could be used in areas other than the cloud, for example in embedded systems and self-driving cars.
2. Was there disagreement? Why? 
- Some people thought that the small image size of unikernels was its biggest advantage compared to containers, but other people thought that its security was the biggest advantage.
3. What was the consensus about the work?
- People agreed that unikernels were one of its kind and had a lot of potentials, but it would be hard for unikernels to become mainstream because they were not compatible with existing applications.

