---
layout: page-fullwidth
show_meta: false
#title: "MOOClet"
subheadline: "The MOOClet/AdapComp Framework"
#teaser: ""
header: 
permalink: "/mooclet/"
---
[![Watch the video](https://img.youtube.com/vi/_PrBCaOE4QE/default.jpg)](https://www.youtube.com/watch?v=_PrBCaOE4QE)
[Watch the video (7:02 mins)](https://www.youtube.com/watch?v=_PrBCaOE4QE)

An AdapComp (short for "Adaptive Component," also known as a MOOClet) is a digital component – like an explanation in an online course or a problem – designed using the AdapComp technology. This technology enables instructors and researchers to engage in a wide range of A/B experimentation, crowdsourcing, real-time data analysis, and personalization.

The term MOOClet is used because this technology was first developed for MOOCs. However, the framework can be used to redesign any digital resource such as this webpage, emails, and components of smartphone apps.

The AdapComp Framework is a specific process for building the technology underlying components of digital resources – like explanations and other text components of webpages – to enable a range of A/B experimentation, crowdsourcing, real-time data analytics, and personalization.

For example, we redesigned the text component that provided students with explanations for correct answers on math problems as an AdapComp. This enabled new explanations to be added dynamically while students were solving problems (crowdsourced from other students). The AdapComp enabled the use of a machine learning algorithm to compare explanations in a randomized A/B experiment and to automatically present the best (most highly rated explanations) more frequently as data was collected.

To give a very different example, we redesigned the emails instructors sent out in an online course to be AdapComps, designed to maximize response rates to emails. This allowed us to start by conducting A/B Experiments that compared three different subject lines, analyze data in real-time to discover which subject lines increased response rates for people who spent different numbers of days in the course, and modify the A/B experiment so that it transformed into active personalization of subject lines to student profiles.

Educational components we have redesigned as AdapComps include text explanations in EdX, hints in math problems in ASSISTments, study tips in Canvas problems, and emails instructors send on campus or in MOOCs.

The formalized process for implementing an AdapComp framework is described below. But once a digital component is implemented as an AdapComp (like a text/image/video explanation, a discussion answer, a webpage), this guarantees that components of these online resources can be easily modified by instructors and researchers to:

- Add new versions at any point in time.
- Compare these multiple versions using randomized experiments (A/B testing).
- Personalize by providing multiple versions to different student profiles.
- Receive data in **real-time** about students' interactions with these components.
- Link anonymized data from other non-AdapComp sources like existing learning management systems and use it for analyzing the impact of experiments and conducting adaptive personalization.
- Dynamically change the rules for how versions are presented, and to whom, using hand-written rules or algorithms. This allows:
  - A/B Experiments to be changed automatically so that the best (or better) version is presented more often as data is collected.
  - A/B Experiments to discover how to personalize, and these new rules for personalization to be implemented.
  - Any machine learning algorithm for dynamically modifying experiments and personalizing to be deployed in real-time. Specifically, an AdapComp is an abstraction for a reinforcement learning agent (including multi-armed bandits).

The formal definition: A digital resource component (e.g., lesson/problem) is an AdapComp IF and ONLY IF:
1. There is a collection of multiple versions of the AdapComp content that can be modified and added to at any time via API.
2. Which version is delivered to a student is determined by a policy or function that takes as input variables from the **User Variable Store**, and the policy/function can be **modified** via API.
3. There is a **User Variable Store** that can receive data from the AdapComp and is modifiable by outside sources via **API**.

## Relevant Publication
Reza, M., Kim, J., Bhattacharjee, A., Rafferty, A.N. and Williams, J. J. (2021). [The MOOClet Framework: Unifying Experimentation, Dynamic Improvement, and Personalization in Online Courses](https://dl.acm.org/doi/10.1145/3430895.3460128). In Proceedings of the Eighth ACM Conference on Learning @ Scale (L@S '21). Association for Computing Machinery, New York, NY, USA, 15–26. DOI: https://doi.org/10.1145/3430895.3460128