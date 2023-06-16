# MVP (or ELP)
Minimal Viable or [Earliest Lovable](https://github.com/mrkrumhausen) Product.

For more information on OwnYou, visit the [documentation pages](http://www.ownyou.io).

There are three components to OwnYou's MVP - an application for the individual user, a publisher SDK and an advertiser SDK.

- The OwnYou consumer application MVP needs to be sufficiently useful that, from its first release, it begs to be shared.
- The OwnYou publisher SDK MVP needs to be so easy to implement, that even the most poorly funded technical team can plug and play it.
- The OwnYou advertiser SDK MVP needs to be so useful, and insightful, that even the most entrenched advertiser will want to use it, and share it.

Each use case needs to be simple as possible.</br>
The MVP establishes a minimum use case per principal stakeholder.</br>
We may choose to mimimic an operational intelligence stack.</br>

Specific MVP requirements can be found in the [Projects](https://github.com/OwnYouLtd/mvp/projects?query=is%3Aopen) section but we would encourage you to explore the OwnYou [documentation pages](www.ownyou.io) first, and discuss the requirements in either the OwnYou [discussion](https://github.com/orgs/OwnYouLtd/discussions) boards on GitHub or on [Discord](https://discord.com/channels/960473414978646036/960473414978646040).

## MVP Goals
A successful MVP helps validate our US$700bn TAM.
The digital advertising market is in an existential crisis. After two decades of personal data abuse, individuals and regulators are demanding an end to personal data harvesting.  
Leveraging decentralized technology primitives creates room for an entirely new approach to digital advertising. Where personal data is a resource that individuals can monetize themselves. My data becomes something I can trade, for services and money, while still retaining control,  ownership and privacy. The technology works for me rather than locking me into one walled garden or another.
This MVP lights up a path for OwnYou. 

## The OwnYou MVP
OwnYou develops open-source software for users, publishers and advertisers. OwnYou does not collect, process or use personal user data. The following summarizes why people, publishers and advertisers will user OwnYou:

- Individual's use OwnYou because it is easy to log into websites, and they make money doing so. The more personal data they collect, the more relevant the advertising they receive and the more income they generate. Their data never leaves their direct control or ownership. OwnYou does not collect, manage or process personal user data.
- Publishers like OwnYou because higher quality zero-party user metadata boosts the quality of their inventory. They get that data from individuals directly. They do not need to integrate with any third-party systems. 
- Advertisers like OwnYou because it guarantees they connect to real humans, with high-quality metadata, and real-time transactional attribution data. The data comes through existing bid-streams. If they want to pay users for attribution data, they need to use the OwnYou SDK which allows them to generate attribution hashes, and register them on a public OwnYou blockchain.

OwnYou makes money by facilitating personal data transactions using a public blockchain. That money is put back into developing open-source software for users, and businesses that wish to connect to users, while protecting user personal data privacy.

#### There are three core components to the OwnYou software stack:
- A Consumer Application
- A Publisher SDK
- An Advertiser SDK

#### The OwnYou MVP needs to demonstrate three things:
1. how pseudonymous personal user data drives more relevant advertising, benefiting publishers and advertisers.
2. how attribution hashes provide advertisers with the attribution information they need, and compensates users for providing it, without data harvesters, processors or any middlemen.
3. how decentralized technology makes that possible without centrally managed services.

A successful MVP will result in publisher, advertiser and individual user sign-ups.

#### The main technologies used include:
- A digital wallet, verified credentials and decentralized identifiers (DIDs)
- Decentralized Web Nodes (DWN) and Encrypted Data Vaults (EDV)
- Cryptographic hashing functions and digital signature schemes
- A public blockchain
- Sign-in with Ethereum, or with any other public blockchain. 

## The OwnYou roadmap and the MVP

#### Collecting Personal Data
OwnYou will provide the means for individuals to aggregate their personal data into local storage, or into remote storage (cloud or IPFS), under their control. OwnYou will make it easy for users to choose how and where that data it stored. 

The MVP demonstrates how a user controlled app can create decentralized storage managed by the user, to consolidate their emails, personal calendar, financial records and photos. 
In a steady state, we want to create connectors that connect to the user's data and automatically syncs for all future updates. The MVP should accommodate manual refreshes.

#### Extracting Target Audience Data from Personal Data
OwnYou will provide infrastructure, or leverage a third-party decentralized compute networks, for individuals (or their agents) to run third-party inference algorithms on their personal data, without sacrificing control or privacy. The result is a list of the most relevant target advertising topics and a list of relevant goods and services for price comparison and direct marketing opportunities. 

The MVP demonstrates how we can run basic inference on the individual's data with weaker privacy guarantees, but still resulting in target advertising topics than conform to IAB Tech labs target audience taxonomy.

#### The Publisher SDK
OwnYou will make it easy for individuals to sign in to websites, and apps, using the OwnYou publisher SDK. Using the OwnYou sign-in process for both publishing and e-commerce sites, allows the user to monetize their personal data for more relevant advertising, generating real money, and OwnYou token rewards. For existing OwnYou app users, the login process will be no more than a one click-process. Publishers and application developers, both traditional and web3 variants, will be able to use a simple SDK that makes it easy for them to offer the sign-in-with-OwnYou (SIWO) sign-in option.  

The MVP demonstrates a simple publisher sign in process that connects a webpage to a user's digital wallet and shares user metadata that can be used in a header bidder wrapper. 

#### Attribution Data
OwnYou will make attribution data easy for advertisers to use, and easy for users to sell.
All payments will be in stablecoins (or CBDCs, when they become available).
OwnYou tokens will be issued as a reward for participating in a transaction. OwnYou tokens will be non-transferable for at least the first five year's of operation. The token is not a security. 

The MVP needs to demonstrate a simple user attribution data cycle. We want to demonstrate:
- Secure, asynchronous, peer to peer communication between the advertiser SDK and the user. It is likely this will leverage the DWN standard (W3C) and the DIDComm protocol (W3C).
- Advertisers share the campaign ID, channel, a time stamp, a nonce, and any other values they which to include in the hash, with a request for attribution.
- Both the advertiser SDK and the user's wallet create the same attribution hash using their respective DIDs, the campaign ID, the shared time stamp, the nonce provided by the advertiser, and any other values requested by the advertiser.
- The advertiser records the hash on-chain, using the user's DID to derive the user's blockchain address. Eventually, but not in the MVP, the advertisers will also transfer a payment for attribution to that address. 
- The user's wallet will use the same address to match the attribution hash. Eventually, the user wallet will both check the attribution hash on chain, and confirm receipt of funds, before releasing the attribution hash in future sign-on with OwnYou interactions. 
- For the next 30 days, the user will share this hash with all subsequent OwnYou Sign-in interactions. 
- This is an asynchronous, workflow, leveraging a shared deterministic protocol, used by the Advertisers SDK and the user's digital wallet.


## What is the OwnYou Consumer Application MVP?

- Verified Credentials with selective disclosure and holder blinding. Importing them, and creating them.
- A digital wallet to store verified credentials, and crypto tokens received from one-time blockchain addresses (created by the wallet, for the sign-in-with-ownyou process).
- Digital wallet agents tasked with managing personal data access rights and interacting with the publisher SDK for sign-in-with-ownyou (SIWO).
- An application that helps users to synch their existing personal data (email, photos, financial records, social media etc) with their Personal Data Store.
- A personal data store (cloud, preferably decentralized) for unstructured raw personal data that can be permissioned for AI inference.
- A personal data store (client, maybe also decentralized) for target audience profiles and decentralized identifiers (DIDs), that can be synched across devices.
- An agent that manages peer-to-peer communication with advertisers
- An agent that uses a hashing protocol to create one time-hashes specific to an advertiser campaign and time-stamp. 

#### Options to make the user app more engaging
If we feel the user MVP value proposition won't keep users engaged, we should explore what would make users want to connect more personal data, and revisit the application. We have a few options, including a personalized ChatGPT. This is already a crowded space but that might suggest less development work.
- Chatting with your digital self - a fun and engaging application that allows the user to interact with their digital self, asking questions to, and about, their digital "self".
	- "what did I spend the most on last week?"
	- "where should I go on holiday this summer?"
	- "how can I save more money?"
	- "what am I most likely to spend money on over the next thirty days?"
	- "recommend a dish I might like to cook for dinner"
- A "digital self" is composed from locally stored data (or cloud/IPFS storage under their exclusive control), extracted from their Gmail, financial records, calendars and images.
- A "digital self" is a function of several components
	- one or more vector databases storing embeddings constructed from raw user data
	- prompt engineering that uses agents + tools + embeddings and a large language model (LLM) to answer user questions
- The app acts as natural language semantic search on personal data. It is engaging; learning what our raw personal data reveals about ourselves. It helps demonstrate OwnYou's core infrastrcuture, used by the same inference processes that create target audience profiles and driving advertising and price comparison use cases. This allows us to demonstrate how raw personal data can be used to create "intelligence". 


## What is the OwnYou Publisher SDK MVP?

- Publishers integrate a sign-in with OwnYou button on their webpage.
- The button initiates a request to connect to the user's OwnYou wallet.
- Once connected, the wallet shares a one-time DID and metadata (including attribution hashes) with the publisher.
- The publisher SDK makes it easy for the publisher to include the additional metadata in their bid-stream.


## What is the OwnYou Advertiser SDK MVP?

- The advertiser SDK makes it easy for advertisers to initiate the attribution hash workflow and
- use existing attribution hashes in new bid-steams.
- The advertiser SDK demonstrates how decentralized technologies can create peer to peer relationships with individuals without relying on third-party data collectors, processors or any other intermediary. This SDK plants the seed for a new type of digital advertising that connects the advertiser directly to the individual for real-time, granular, attribution data.  

## OwnYou MVP target users
People, publishers and advertisers.

#### What type of people?
Early adopters. Crypto users with digital wallets. Users of Spruces sign-on with Ethereum. Advertising techno geeks. Privacy advocated.

#### What type of publishers?
Small to medium sized publishers, using header bidding. Some internal development resources. Frustrated with Google. Suffering from low quality user data. Overcrowded webpages with excessive adverting.

#### What type of advertisers?
Early adopters. Frustrated by increasingly poor attribution data. Advertiser that recognize Apple is less interested in privacy and more interested in advertising revenues. Advertisers frustrated by Google's excessive market share. Advertisers frustrated by poor user data.

## What is our go-to-market?
1. The app is fun, it is free, it is novel - early adopters want to experiment. Small marketing budget at web 3 conferences, promotion via popular tech/crypto podcasts, speaking events 
2. Publishers that want to experiment with verifiable zero-party personal metadata. They deploy the ownyou login SDK which attracts more user app downloads as early adopter. We are exploring SSP partnerships.
3. Advertisers value to quality of OwnYou meta-data, they suggest more publishers use the free SDK. We are exploring DSP partnerships.
