# MVP (or ELP)
Minimal Viable or [Earliest Lovable](https://github.com/mrkrumhausen) Product.

For more information on OwnYou, visit the [documentation pages](www.ownyou.io).

There are three components to OwnYou's MVP - an application for the individual user, a publisher SDK and an advertiser SDK.

- The OwnYou consumer application MVP needs to be sufficiently useful that, from its first release, it begs to be shared.
- The OwnYou publisher SDK MVP needs to be so easy to implement, that even the most poorly funded technical team can plug and play it.
- The OwnYou advertiser SDK MVP needs to be so useful, and insightful, that even the most entrenched advertiser will want to use it, and share it.

Each use case needs to be simple as possible.</br>
The MVP establishes a minimum use case per principal stakeholder.</br>
We may choose to mimimic an operational intelligence stack.</br>

Specific MVP requirements can be found in the [Projects](https://github.com/OwnYouLtd/mvp/projects?query=is%3Aopen) section but we would encourage you to explore the OwnYou [documentation pages](www.ownyou.io) first, and discuss the requirements in either the OwnYou [discussion](https://github.com/orgs/OwnYouLtd/discussions) boards on GitHub or on [Discord](https://discord.com/channels/960473414978646036/960473414978646040).

# What is this MVP
- [chat](#chat)
- [avatar/NFT](#a-dynamically-changing-avatar-that-you-can-mint-into-a-nft)
- [sign-in with OwnYou](#sign)

###  <a name="chat"></a>Chatting with your digital self
A fun and engaging application that allows the user to interact with their digital self, asking questions to, and about, their digital "self".
- "what did I spend the most on last week?"
- "where should I go on holiday this summer?"
- "how can I save more money?"
- "what am I most likely to spend money on over the next thirty days?"
- "recommend a dish I might like to cook for dinner"

A "digital self" is composed from locally stored data (or cloud/IPFS storage under their exclusive control), extracted from their Gmail, financial records, calendars and images.

A "digital self" is a function of several components
- one or more vector databases storing embeddings constructed from raw user data
- prompt engineering that uses agents + tools + embeddings and a large language model (LLM) to answer user questions

*Why this important: it is functional, acting as natural language semantic search on personal data. It is engaging; learning what our raw personal data reveals about ourselves. It provides the backbone for all other OwnYou related inference, driving advertising and prices comparison use cases.*

#### todo
- [ ] detailed components
- [ ] what libraries/tools can be used
- [ ] boundaries and challenges

#### Competing products
- [Personal AI](https://www.personal.ai/)

#### Open source libraries, tools, development Effort

| Developer | Tools                                                                                           | Development Effort |
| --------- | ----------------------------------------------------------------------------------------------- | ------------------ |
| [SpruceID](https://www.spruceid.dev/)  | Verified Credential creation, verification, presentation. Digital Wallet, Decentralized Storage | medium             |
| tbd       |                                                                                                 |                    |
| Verida    |                                                                                                 |                    |
| Fision    |                                                                                                 |                    |
| MATTR     |                                                                                                 |                    |


### <a name="avatar"></a>A dynamically changing avatar that you can mint into a NFT
Other than engaging with their digital-self via a "chat" application, the user can mint a unique avatar created from their digital profile. The avatar changes to reflect any new inference from  additional data added by the user. New items sets are unlocked by the avatar, as the user adds new data sources. This results in an avatar that changes overtime, reflecting the user's changing needs and interests.

*Why this important: it shows how raw personal data can be used to create unique digital art, dynamically and impermanent, unless minted. It keeps the relationship with OwnYou "personal". It keeps changing, the more the user shares, and the more they engage with the app. It provides an opportunity to share something with other existing and potential users. *
