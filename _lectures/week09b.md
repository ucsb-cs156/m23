---
title: "Week 09b - 08.24 Thu"
lecture_date: 2023-08-24
description: "Work on legacy code projects"
ready: true
layout: default
parent: lectures
slides: 
---

# Today

* Start with standup
* Review team Kanban board, and PR queue
* Make sure anything that needs a code review, has one.

# Surveys coming soon

* ESCIs: please don't forget to fill them out! They are super important.
* CATME surveys
* End of quarter extra credit (research survey)

# Today:

## If your team isn't yet at 100 points:

* Do a standup
* Review team Kanban board, and PR queue
* Look at the PRs you have and get everything code reviewed that's ready to be code reviewed
* Work to get things merged
* Make sure anything that needs a code review, has one.

## For Everyone

Optional but *highly recommended* as preparation for takehome final exam
* Every team member should locate a PR they *authored* that was merged into main; if there's more than one, choose the one that best shows off your skills and your contributions to the team's success.  Post a link to that PR in the team slack channel with the text `My best PR`
* Every team member should locate a PR they *code reviewed* that was merged into main; if there's more than one, choose the on that best shows off your code reviewing skills.  Post a link to that PR in the team slack channel with the text `My best Code Review`

## If your team is already at 100 points but not yet at 200 or more:

* Discuss as a team: do you want to continue working on coding and PRs, or start on your release notes/final presentation?
* If you want to continue, what are you your best candidates from the remaining PRs to get merged by Friday afternoon?
* Make a post with the team consensus and tag Prof. Conrad
* List the top three contenders (with links to the PRs) and give a brief explanation of where each one stands.
* Or, start planning your video (see below)

## If your team is already at 200 or more:

* Start planning your video (see below).


# Week 10 Tuesday and Thursday are for presentations

The instructions for the final video are listed below.
* The final video presentations will take place Tuesday and Thursday of next week.
* You are not required to attend in person, but you are required to participate;
  - There's a participation grade for providing feedback on one another's presentations
  - There's a live demo component as well, and your team needs to be represented there.

<details markdown="1">
<summary>
Notes about the final exam
</summary>
  
  
# Notes about the final exam
  
The final exam will be an online take home exam, and will be mainly high level questions about the process of software development that you learned in team01, team02, team03 and the legacy code project.

There may be questions about any of the following.  If you've been paying attention all along, you shouldn't really need to "cram".  The answers should be pretty much in your knowledge base already.

* Agile processes, e.g. standups, retrospectives, the role of a product owner/manager
* GitHub tools and their interaction with Agile processes: using feature branches, issues, Kanban board, Pull requests, code review
* General Web Development concepts, e.g.: Backend vs. Frontend
* Some Spring Boot specifics: controllers, services, use of Swagger
* Some React specifics: components, use of Storybook
* Testing in general: unit testing, test coverage, mutation testing
* Spring Boot Testing: Role of JUnit, Jacoco, Pitest, Mocking and Stubbing
* React Testing: role of jest, and Stryker
* Using third party APIs and representing data with JSON (as we did in team01, and later phases as well.)

I'll be asking questions about these topics that I think are the type you might be asked as a job interview.  So if you study, study the way you would for a job interview.

# Please do not collaborate on your exam answers.

* Identical text is unlikely to occur if each of you is working indepenently and writing in your own words.
* If you are copying/pasting text from an online source (e.g. to explain what a retrospective is) be sure that you use "quotation marks" around direct quotations, and **cite your source.**
  
  Otherwise, you are liable to end up triggering the suspicion of academic dishonesty because of the similarity of your text to someone else that happens to be
  using the same source.
  
  Also: relying too much on direct quotes rather than putting things in your own words may result in lower grades; if you have to quote others too much, 
  it suggests that you have not really internalized the content, but have to rely on others understanding.  So use direct quotes sparingly, if at all; try instead
  to answer in your own words.
  
 
Academic integrity investigations are unpleasant for everyone, and they don't help anyone learn. 

I really dont want to spend my time on those, so please don't create conditions where I have to do that.

Work independently, and let your learning speak for itself.

# Clarity and consiseness counts

* Small grammar / spelling errors may or may not be penalized; if an interviewer would be confused by the answer, or have some doubt as to your understanding,
  then they count.   If there is no doubt about your understanding, I'm liable to be more lenient.
* Make sure your answers are clear and understandable.
* Do not just do an information dump of everything you know about the topic, or everything you can possibly find online about the topic.  An employer wants someone to answer
* their question, and they also want someone that makes good use of their time.  Don't waste the interviewer's time.

</details>

<details markdown="1">
<summary>
Notes about the final presentation
</summary>

# Notes about the final presentation

The final presentation should be a team effort, and should highlight all of the PRs that got merged into the main branch.

Make a video of between 5-8 minutes (see guidelines below) and submit the link on Gauchospace.

Limit your presentation to 5-8 minutes.   8 minutes is a hard upper limit.

Highlight the work *from an end user perspective first*.

That is:
* The best thing is to show how an end user would use the feature
* The next best thing is to show either a front or backend component in isolation, for example:
  - If there is a front end component that is not active in the app yet, you can show it in Storybook
  - If there is a backend API, but the functionality isn't available in the user interface yet, you can demo it in Swagger.
* Show internals of code only after explaining the user facing functions, and even then, only if you have left over time.

  
# Instructions for your video:

Here's a tutorial [video on making demo videos from CS48 S20](https://youtu.be/k0Je8ASh4jo) (Video inception)

Based on the experience of CS48 students, **pre-recording is strongly recommended**.  You will *know for sure* in advance whether the
demo is successful, and whether or not you've hit the target length of 5-8 minutes.

Your video should be 5 to 8 minutes long, and cover these points:

* First, mention the names of the members of the team, and introduce the person narrating the video.  
  - It is ok if all the team members appear in the video.  It is also ok if only one person narrates the video on behalf of the team.
* Second, go through each of the features that your team worked on that were merged into `main`
  - Only demo the features that were merged into `main`
  - Focus in this part of the video on demoing the features from a *user perspective*, not on the technical details of how they were implemented.
* Next, if there is time remaining to reach the 5-10 minute mark, you may briefly cover any technical and/or non-technical challenges your team faced
  - You don't have to cover everything.  
  - You don't really even have to include this part if your demo already hits the 5-10 minute range.
  - If you do include this part, focus on the items that you think would be interesting to the audience (fellow students in CS156 M23, and the staff of CS156 M23, and potential users of the software you worked on). 
  - Possible items to include
    - Particularly interesting technical details of what you had to write in the code
    - Challenges in testing
    - Challenges in team communication and organization, and what you did to overcome those
* Optional: at the end, if you like, you may thank anyone that was particularly helpful to the team from the staff (TAs and LAs, or students from other teams). 
  - Please don't include thanks to me (Prof. Conrad) in the video; I don't want this to be an exercise in brown-nosing.
  - If you do want to express gratitude, feel free to share your thoughts with me on the Slack, by email, etc.  

Please then also poll your team members and let me know your thoughts about the privacy of your final demo video:
* public, available to anyone that is interested in the app and the course
* unlisted, but ok to make it available to future CMPSC 156 students (as an example, and to orient them to the app and the course)
* unlisted, and only shown once for this team's final demo, and to course staff 

</details>


<details markdown="1">
<summary markdown="1">
Example Videos (these teams gave me permission to share them publically)
</summary>

## Gauchoride

* [s23-5pm-4 Gauchoride](https://drive.google.com/file/d/1p2ZWmYj3z5CuXQyZ2b3m1pTFz8WeDNuH/view?usp=sharing)

## HappyCows

* [s23-6pm-4 Happycows](https://drive.google.com/file/d/1e5ItNmY0UPYJEGHYP0zuGnGyJoCeAAis/view?usp=sharing)

* [f22-5pm-3 happycows](https://drive.google.com/file/d/1lNaRYu-LNSv03MrwPxWYezMXH9pkaeBY/view?usp=sharing)
* [f22-6pm-4 happycows](https://drive.google.com/file/d/1l5L88UaTG4B_-8ZKiYx-PXu62cZgSjP9/view?usp=sharing)
* [f22-7pm-3 happycows](https://drive.google.com/file/d/1H3RapJJbsP0pAV6YcvRMLeTIG77nBl-J/view?usp=sharing)
* [f22-7pm-4 happycows](https://drive.google.com/file/d/1yzT9WInuLZQyvenYqBLh_fEgNSvlkulp/view?usp=sharing)

* [s22-4pm-3 happycows](https://www.youtube.com/watch?v=U5l8mp6F3OU)
* [s22-4pm-4 happycows](https://www.youtube.com/watch?v=CTqyYt5ob4c)
* [s22-5pm-3 happycows](https://drive.google.com/file/d/1WHxpYGr9UQYEQFUomv9NpUXZ5MkwvHXL/view)

* [w22-7pm-3 HappyCows](https://youtu.be/RJ8Tf_xfN9E)

## Courses

* [s23-7pm-1 Courses](https://www.youtube.com/watch?v=FtegV0S_fhc)
* [s23-7pm-3 Courses](https://drive.google.com/file/d/1snWRRRjOrMHHANGm9UyUml52wq01rtXh/view?usp=drive_link)

* [f22-5pm-1 courses](https://www.youtube.com/watch?v=qVludXu1n9c)
* [f22-5pm-2 courses](https://www.youtube.com/watch?v=TJCToeTyasw)
  
* [s22-4pm-1 courses](https://www.youtube.com/watch?v=aRSIdiHSZOI)
* [s22-4pm-2 courses](https://drive.google.com/file/d/1TtjZmlN3W9fAiQS0brLsyMw5KE_ix0Oi/view)

* [s22-5pm-2 courses](https://drive.google.com/file/d/17KYDvB2EDmShv2Gr1Ux-rf1917Lw6AHJ/view)
* [s22-6pm-1 courses](https://www.youtube.com/watch?v=v3rP1a6yf9A)
  
* [w22-7pm-1 courses](https://drive.google.com/file/d/1i_lIyzWLFyUkyDSHmsumgim1HsPp35u9/view?usp=sharing)
* [w22-6pm-2 courses](https://youtu.be/g3xrcSSBOGs)
* [w22-5pm-2 courses](https://www.youtube.com/watch?v=OYj6NVf9-ls)

</details>

