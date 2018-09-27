# LIP (Loki Improvement Proposal)
Loki Improvement Proposals (LIPs) are the formalized methods by which the Loki Project Team, external contributors or contractors can make proposals for any major Loki or Lokinet upgrades, this can including core protocol specifications, client APIs, and additional features. LIP's should also be used to describe any Major changes that go before Loki Service Nodes to vote on, outside of non relevant requests handled oy the Loki funding system. 


LIPs can also act as supplementary documents for funding applications  to the Loki foundation, or Loki funding system.

# Contributing

Anyone is free to propose an LIP, if they follow the formatting rules setout in this document. 

 1. Fork the repository by clicking "Fork" in the top right.
 2. Read the [LIP-x](lip-X.md) template to understand how a LIP should be structured
 2. Add your LIP, in the LIP's folder [Here](https://github.com/loki-project/LIPs/tree/master/LIPS) of your fork.
 3. Submit a Pull Request to Loki's [LIPs repository](https://github.com/loki-project/LIPs) from your fork.

Your first PR should be a first draft of the final LIP. An editor will manually review the first PR for a new LIP and assign it a number before merging it. All discussion should occur inside of the LIP.

If your LIP requires images, the image files should be included in a subdirectory of the `assets` folder for that LIP as follow: `assets/lip-X` (for lip **X**). When linking to an image in the LIP, use relative links such as `../assets/lip-X/image.png`.

There are two main progression routes for LIP's

**Submitting your LIP for Vote**

If you are submitting your LIP for vote by the Loki Foundation or the Loki Service Nodes you should tag the title of your request as per LIP-x Specs with either [Foundation Vote] or [Service Node Vote]. If the Foundation or Service Nodes approve your LIP then an editor will tag your LIP as finalized. If the Service Nodes or the Foundation denies your LIP then your pull request will be closed, you are free to make another proposal which addresses any concerns raised by the foundation or Service Node operators and re-propose your LIP.

**LIP Assessment by the Loki Project Team**

If you believe your LIP does not need to be voted on by the Loki Foundation or Service Nodes then you can tag your LIP as a [No Vote]. If a LIP is tagged with [No Vote] your LIP editor may still refer your LIP to a vote by the Foundation or Service Nodes if they believe the LIP is controversial or the discussion around the LIP does not reach consensus.
If the LIP does not need to go to a vote then the LIP editor should decide when the LIP is ready to be marked as final. 

**LIP Finalized**

Once an LIP is finalized the Loki development team will work alongside you to help you merge your changes into the development branch of Loki, any pull request to Loki should reference relevant LIPs if the change is major. if your LIP is marked as Final but does not yet have developed code, we encourage regular communication to the community using the LIP pull request as a sounding board.

# LIP Status Terms
* **Draft** - an LIP that is undergoing rapid iteration and changes
* **Last Call** - an LIP that is done with its initial iteration and ready for review by a wide audience
* **Denied** - an LIP that has been rejected by either a vote from the Loki Service Nodes, the Loki foundation or the LIP editor.
* **Final** - an LIP that the Loki Project team have decide to implement and release in a future hard fork or has already been released in a hard fork
