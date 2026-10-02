---
layout: post
title: "The technology is there. Do we trust each other enough to use it?"
date: 2026-10-02
---

I came away from EGI2026 thinking about a question that kept surfacing across very different sessions: what would it take for a data owner to feel comfortable letting a researcher at another organisation use their data?

The technical possibilities are exciting. A researcher can sign in through their own institution, have their project membership checked through a research community, and request access to a service elsewhere. That service can make a decision based on who they are, what they are trying to do, and the conditions attached to the data. This could make studies involving several institutions much easier to organise.

For sensitive data, though, “the system can do it” is a long way from “we are willing to use it”.

One example at the conference was a federated approach to assessing health data quality. The checks run where the data is held, and a researcher receives limited results that help them judge whether a dataset might suit their study. They can learn something useful before applying for access to the data itself. That could help researchers find suitable cohorts across more sites while each site retains control over what leaves it.

The questions from the room were revealing. Several people wanted to know what would stop a data store from overstating the quality of its data or changing the results before sending them back. Meanwhile, a data owner might reasonably ask whether a quality report could reveal something about a small, sensitive cohort. Both sides were being asked to rely on results produced somewhere they could not fully see.

I do not think those questions undermine the idea. They show what a useful technical demonstration needs to be followed by: an agreement about who defines the checks, what can be reported, how results can be verified, and what happens if either party disputes them.

In another session, someone said, “I don’t trust sysadmins.” I cannot say what lay behind that comment, but it added another dimension to the discussion. Trust also involves the people operating the infrastructure and the access they have. A data owner may want to know who can change an access rule, whether an administrator can bypass it, and how those actions are checked. Those questions need answers alongside any demonstration of the access system.

The same issue came up in discussions of federated access. Signing in tells a service something about a person’s identity. It does not, by itself, establish that the person is approved for a particular project or allowed to download a particular dataset. Those decisions may depend on a university, a research community, a project lead and the organisation holding the data. Each needs to know which claims it can rely on and who is responsible when something changes.

Consider a researcher whose project role is removed while they still hold a valid access token. Who can stop access first? Who can see what happened? Who contacts the data owner? If the answers are vague, reluctance to share data is reasonable.

## Is an audit trail enough?

Traceability and transparency came up repeatedly at EGI2026, and they matter. A data owner should be able to find out who requested access, which rule was applied and what the service allowed. A researcher using a federated data quality report should know how its checks were defined and what the reported results mean. If something goes wrong, the organisations involved need enough information to investigate it together.

But an excellent record of an access decision is cold comfort if it only tells you how data left after it should have been protected. A record of a quality check is of limited use if nobody can tell whether the reported result reflects the check that was agreed. The harder question is how we give both sides confidence that the system will behave as agreed *before* either has to rely on it.

That means testing more than the successful route through a request. We need to know what happens when a project ends, a role is assigned to the wrong person, an approval changes or a service cannot check a claim. Does access stop? How quickly? For a data quality check, we also need to agree what evidence would let a requester trust the reported result without requiring the data owner to expose the underlying data.

It would be easy to respond by adding another manual approval at every stage. That might feel reassuring, but it would make cross-institutional work so cumbersome that people would avoid the system. We need clear conditions for routine decisions and a route to a person when a request falls outside them or something unexpected happens.

## Can written policy become an access decision?

Another strand of EGI2026 offered a way to make some of those conditions clearer. A session on policy based authorisation described using ODRL to represent access conditions, with Open Policy Agent evaluating requests and services enforcing the resulting decisions. Related work, including OpenREL, is exploring how to express conditions that currently sit across licences and other documents.

The attraction is concrete. If an approval says that a named project team may analyse a dataset in an approved compute environment until a given date, those conditions could be represented in a form a service can check. A researcher would not need to wait for someone to interpret the same approval from scratch at every access point. Changes to the approval could also be reflected in the rules the service uses.

That could speed up access to data and compute. But the policy has to say what people actually mean.

In my work on connecting project approval to research infrastructure access, I have repeatedly found that the necessary information is spread across proposal systems, data management plans, ethics approvals, contracts and conversations. Some conditions are written down but never passed to the team operating the infrastructure. Others are treated as obvious by the people making the decision and are absent from the documents altogether.

Does “the project team” include a visiting collaborator? Who approves a new member after the project starts? Is analysis allowed at another institution if the data cannot be downloaded there? What happens when an ethics amendment changes the permitted work?

A system can apply an agreed rule consistently. It cannot safely work out an unstated one for us. Making policy actionable starts with people talking through real cases, including the awkward exceptions, and recording who has authority to decide each one.

## Giving people a reason to try it

I think trust will grow when the people involved can see how a system behaves under the conditions that worry them. A data owner needs to see how an eligible researcher gets access, how an ineligible request is refused and how access is withdrawn. A researcher needs to understand why a dataset has been described as suitable for their study and what they can reasonably infer from a quality report. Both need to know who will answer when they challenge a decision or a result.

A limited trial seems a sensible place to start. Choose a dataset and a specific kind of request. Agree the access conditions with its owner, then test the expected approvals, refusals and changes of circumstance. Rehearse a mistaken role assignment or an expired approval. For a quality check, agree the method and reporting limits in advance, then test what the requester can verify without seeing the underlying data.

That work may expose gaps in the policy, the technology or the communication between organisations. Finding those gaps early gives us a way to improve the system before asking people to rely on it at scale. It also gives researchers and data owners a more useful question to ask each other than “Do you trust us?”: “What would you need to see this system do before you would use it?”
