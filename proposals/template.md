# Proposal Process

Proposals are design documents to provide information to the community to describe a modification or enhancement of the HDF5 specification, a new feature for its processes or environment. The proposal should provide specific proposed changes to the HDF5 specification and a narrative rationale for the specification changes.

We intend forproposals to be the primary mechanism for evolving the spec, collecting community input on major issues and documenting the design decision that has gone into HDF5. In addition, the proposal author is responsible for building consensus within the community and documenting dissenting opinions.

Because the proposals are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

WHERE:

- Developers refer to contributors and maintainers of the project
- User(s) refers to an individual or group of individuals or the broader community using the project in any way.

# Proposal audience
The typical primary audience for proposals is the developers working on HDF5 and its various implementations and the HDF5 community.

The broader HDF5 community may also choose to use the process to document expected feature additions and to manage complex design coordination problems that require collaboration across multiple projects.

# Proposal types
- ** Specification Proposals ** 
Specification Proposals deal with the changes related to HDF5 Specifications. The Specification Proposals for now introduces changes in the core specification of HDF5. The changes related to core specification follow a strict and thorough review process and should be adopted by everyone in the HDF5 community.

- ** Core protocol Proposals ** 
Describes a proposal which involves changes in the core specification of HDF5. Core protocol proposals (commonly known as Core proposals) are a part of SPEC proposals and apply to HDF5 Specifications and its various implementations under the ** zarr-developers/zarr_implementations **  GitHub repo. The core protocol proposals should be adopted by every implementation of HDF5 and, in general, the overall HDF5 community. Core proposals must go through a thorough review process, including involvement, discussion, and voting from the author of the proposed proposal, HDF5 Technical Advisory Board, author(s) of various HDF5 implementations, and open-source projects/research groups using HDF5 and the general HDF5 community. The general advice is that everyone should be made aware of changes introduced by core proposals. Core protocol proposals require community consensus, and developers or users are typically not free to ignore them.

Note: Currently, Specification proposals only deal with the core specification of HDF5. The scope of SPEC proposals will be extended in the future.

- ** Informational proposal ** 
Describes a proposal design issue or provides general guidelines or information to the HDF5 community but does not propose a new feature. Informational proposals do not necessarily represent HDF5 community consensus or recommendation, so users and implementers are free to ignore informational proposalS or follow their advice.

- ** Process proposal ** 
Describes a new process around HDF5 and its implementations or proposes a change to (or an event in) a process. They may propose an implementation, but not to the HDF5 specification or its implementations; they require community consensus; unlike informational proposals, they are more than recommendations, and developers or users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in HDF5’s specification development. Any meta-proposal is also considered a Process proposal.

# Proposal Workflow 

The proposal process begins with a new idea for HDF5. It is highly recommended that a single proposal contain a single key proposal or new idea. Small enhancements or patches often don’t need a proposal and can be injected into the HDF5 development workflow with a pull request to the proposals or ** zarr-specs ** repo. The more focused the proposal, the more successful it tends to be. If in doubt, split your proposal into several well-focused ones.

Each proposal must have a champion – someone who writes the proposal using the style and format described below, shepherds the discussions in the appropriate forums, and attempts to build community consensus around the idea. The proposal champion (a.k.a. Author) should first attempt to ascertain whether the idea is suitable for a proposal.

Asking around during the proposals meetings/creating an issue in the proposals repository/posting to Gitter/posting on the organization discussions are the best ways to do this.

The proposal champion is the lead author of the proposal. A proposal should have a lead author and can have multiple co-author(s).

Vetting an idea publicly before going as far as writing a proposal is meant to save the potential author time. Asking the HDF5 community first if an idea is original helps prevent too much time being spent on something that is guaranteed to be rejected based on prior discussion. It also helps to make sure the idea applies to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people.

Once the champion has asked the HDF5 community whether an idea has any chance of acceptance, a draft proposal should be presented to the appropriate venue mentioned below. This allows the author to flesh out the draft proposal to make it properly formatted, of high quality, and address initial concerns about the proposal.

Spec proposals consist of two parts, a PR to the ** zarr-specs ** repository containing changes to the spec and a PR to the proposals repository containing a narrative document explaining the need, importance and use-case for the change. It is also highly recommended that the specification proposal be accompanied by an implementation PR in at least one of the repositories represented in the ** zarr-developers/zarr_implementations. **

# Submitting a proposal
For SPEC proposals, the proposal should be submitted as a draft proposal via two GitHub pull requests, one to the proposals repo and the other to the *  arr-specs * repository.

The first PR should contain the narrative text of the proposal and should be submitted in the proposal repository with the name proposal-<n>.md under /proposals/draft/ where <n> is an appropriately assigned four-digit number. The draft proposal must use the proposal X - Template and Instructions file.

The second PR should contain actual changes and should be submitted in the ** zarr-specs ** repository. The PR should mention the assigned four-digit proposal number from the ** zarr-developers/proposals repository.**

For proposals other than SPEC, the proposal should be submitted as a draft proposal via a GitHub pull request to the ** zarr-developers/proposals ** repository with the name proposal-<n>.md where <n> is an appropriately assigned four-digit number (e.g., proposal-0000.md). The draft proposal must use the proposal X - Template and Instructions file.

* A few points to consider while submitting your proposal: * 

- It should sound complete. The ideas must make technical sense.
- The title should accurately describe the content.
- The proposal’s language (spelling, grammar, sentence structure etc.) and code style should be correct and conformant.
- The HDF5 * Steering Council and the HDF5 Implementations Council * will not unreasonably deny publication of a proposal. Reasons for denying proposal include duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility, or not taking care of HDF5 CODE OF CONDUCT.

→ In conclusion: The submission of SPEC proposals needs two PRs, and other proposals need one PR.

# Discussing a proposal
As soon as the draft proposal is committed to the proposal repository, the author (s) should create a discussion thread for the proposal to provide a central place to discuss and review its contents. The proposal author(s) may create an issue in proposals repository for informational and process proposals and or similarly create an issue in **  zarr-specs ** repository for specifications proposals.

If the author prefers to hold the discussion for SPEC proposals in the second PR submitted in the ** zarr-specs ** repository (as mentioned above), there’s no need to create an issue.

The discussion regarding the proposal should follow HDF5’s CODE OF CONDUCT at all times.

Proposal authors are responsible for collecting community feedback on a proposal. However, to avoid long-winded and open-ended discussions, strategies such as soliciting private or more narrowly-tailored feedback in the early design phase, collaborating with other community members with expertise in the proposal’s subject matter, and picking appropriately-specialised discussion for the proposal’s topic should be considered. proposal authors should use their discretion here.

Once the proposal is committed to the proposal repository, substantive issues should generally be discussed on the canonical public thread, as opposed to private channels or unrelated venues. This ensures everyone can follow and contribute, avoids fragmenting the discussion, and makes sure it is fully considered as part of the proposal review process. Comments, support, concerns and other feedback on this designated thread are a critical part when reviewing the proposal.

# Review and Resolution
The possible paths of the status of proposals are as follows:

# Flowchart

All proposals should be created with the Draft status.

Eventually, after the discussion, there may be a consensus that the proposal should be accepted - see the next section for details. At this point, the status becomes Accepted.

Once a Specification proposal has been Accepted, the second PR which was submitted in the ** zarr-specs ** repository must be merged. After that, the status will be changed to Final.

Once an informational or process proposal has been Accepted, the author should implement changes in the procedure, guidelines, decision-making process, etc. ASAP.

To allow the gathering of additional design and interface feedback before committing to long term stability for specification change or standard library API, proposal may also be marked as “Provisional”. This is short for “Provisionally Accepted” and indicates that the proposal has been accepted for inclusion in the reference implementation or storage specification, but additional user feedback is needed before the full design can be considered “Final”. Unlike regular accepted proposals, provisionally accepted proposals may still be Rejected or Withdrawn even after the related changes have been included in a HDF5 release.

Wherever possible, it is considered preferable to reduce the scope of a proposal to avoid the need to rely on the “Provisional” status (e.g. by deferring some features to later proposals), as this status can lead to version compatibility challenges in the wider HDF5 ecosystem.

A proposal can also be assigned status Deferred. The proposal author or HDF5 Steering Council or HDF5 Implementations Council can assign the proposal this status when no progress is being made on the proposal.

A proposal can also be Rejected. Perhaps, after all, is said and done it was not a good idea. It is still important to have a record of this fact. The Withdrawn status is similar—it means that the proposal author themselves has decided that the proposal is a bad idea, or has accepted that a competing proposal is a better alternative.

When a proposal is Accepted, Rejected, or Withdrawn, the proposal should be updated accordingly. In addition to updating the status field, at the very least the Resolution header should be added with a link to the relevant link of the discussion.

proposals can also be Superseded by a different proposal, rendering the original obsolete. The Replaced-By and Replaces headers should be added to the original and new proposals respectively. Process proposals may also have a status of Active if they are never meant to be completed, e.g. proposal 0 (this proposal).

How does a proposal become accepted?
A proposal is Accepted by the consensus of all interested contributors. We need a concrete way to tell whether the agreement has been reached.

→ For Core proposals

We believe Core proposals are of utmost importance and should follow a thorough review before acceptance. Core proposals introduce changes in the core specification, which are necessary for every other implementation and everyone in the general community to follow. The HDF5 Steering Council (ZSC) and HDF5 Implementations Council (ZIC) closely review the Core proposals, while the author(s) should simultaneously engage the community in their proposal at several discussion forums mentioned previously. The ZSC and ZIC would take community consensus into account while taking the final decision on the Core proposals. Author (s) should ensure that the involvement and discussion form the consensus on the proposal from the author of various HDF5 implementations, open-source projects/research groups using HDF5, the general HDF5 community, and anyone else they, ZSC and ZIC think should be included in the discussions. The Core proposals are accepted by:

Unanimous approval of the HDF5 Steering Council

Majority approval of the HDF5 Implementations Council

Approval indicates that implementation plans to implement the new spec features. Not all implementations must implement all features, but a majority is required.

No vetos from the HDF5 Implementations Council
Each implementation has the right to veto a proposal if it would cause severe problems for that implementation.

Read more about HDF5 Implementations Council.

→ For other proposals

For proposals, other than specifications, the author(s) must form a consensus around their proposal. They may refer to Discussing a proposal section to pick an avenue for discussion and engaging the community.

When you think proposal is ready to accept, create a new issue in ** zarr-developers/proposals ** with a subject like:

Proposal to accept proposal <number>: <title>

In the body of your discussion, you should:

Link to the latest version of proposal,
Briefly describe any major points of contention and how they were resolved,
Include a sentence like: “If there are no substantive objections within 7 days from this post, then the proposal will be accepted;
After you create the issue, you should make sure to link the newly created thread in the Discussion section of the proposal, so that people can find it later.

Generally, the proposal author will be the one to create this post, but anyone can do it – the important thing is to make sure that everyone knows when a proposal is on the verge of acceptance, and give them a final chance to respond. If there’s some special reason to extend this final comment period beyond 7 days, then that’s fine, just say so in the post. You shouldn’t do less than 7 days, because sometimes people are travelling or similar and need some time to respond.

There may be a case that a proposal didn’t attract needed attention towards it, the engagement from the community is low, and 7 days pass by. In this case, the author(s) of the proposal must make necessary efforts to spread the word about the proposal through Gitter or using the organisation discussions feature of GitHub or, if needed, creating an additional issue in the community or proposals repository. In addition, the author(s) should get in touch with the HDF5 Steering Council to prevent the case that the proposal was accepted due to less participation from the community.

If all the above options are exhausted by the author(s), then it’s the responsibility of the HDF5 Steering Council to take the final decision on the proposal.

In general, the goal is to make sure that the community has consensus, not provide a rigid policy for people to try to game. When in doubt, err on the side of asking for more feedback and looking for opportunities to compromise.

If the final comment period passes without any substantive objections, then the proposal can officially be marked Accepted. You should create a follow-up issue in ** zarr-developers/proposals ** repository notifying everyone (celebratory emoji optional but encouraged 🎉✨), and then update the proposal by setting its :Status: to Accepted, and it’s :Resolution: header to a link to your follow-up discussion (the last issue created) thread.

If there are substantive objections, then the proposal remains in Draft state, discussion continues as normal, and it can be proposed for acceptance again later once the objections are resolved.

In unusual cases, the HDF5 Steering Council may be asked to decide whether a controversial proposal is Accepted.

Maintenance
In general, SPEC proposals are no longer modified after they have reached the Final state. The changes made to the HDF5’s core specification in the ** zarr-specs **repository are considered the ultimate reference. However, finalised SPEC proposalS may be updated with minor changes as needed.

Process proposals may be updated over time to reflect changes to development practices and other details. The precise process followed in these cases will depend on the nature and purpose of the proposal being updated.

proposal Format
proposals are UTF-8 encoded text files using the GitHub flavoured markdown format. Please see the proposal X - Template and Instructions file and the GitHub Markdown Spec for more information.

Header Preamble
Author: <list of authors’ real names and email addresses>
Status: < Draft | Active | Accepted | Deferred | Rejected | Withdrawn | Final | Superseded >
Type: <Specification | Process | Informational>
Created: <date created on, in dd-mmm-yyyy format>
Require: <Previous proposal number>
HDF5-Version: <version number>
Replaces: <proposal number>
Replaced-By: <proposal number>
Resolution:  <Link to discussion thread>

The Author header lists the names and the email addresses of all the authors of the proposal. The format of the Author header value must be:

Random J. User <address@dom.ain>

Discussion
Link 

Copyright
This document has been placed in the public domain.˙
