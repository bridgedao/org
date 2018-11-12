# BridgeDAO
BridgeDAO is a general implementation of a concept of [Collateralized DAO Proxy Services](https://research.aragon.org/t/collateralized-dao-proxy-services-as-an-aragon-network-use-case/137) with purpose of bridging the gap between the phyisical world and DAOs. Its first specific implementation, called Paperclip, solves the problem of DAOs being unable to receive, hold and send fiat transactions in a trustless way.
Further introduction is available in Aragon Nest Proposal.

# org
The governing body in charge of the project. Home of research papers, discussion and ideas for the BridgeDAO project.

## Content
1. [Technical Whitepaper](https://github.com/bridgedao/org/blob/master/Technical%20whitepaper.md)
2. [Paperclip Lite](https://github.com/bridgedao/org/blob/master/Paperclip%20Lite.md)(latest iteration)
3. [Paperclip MVP](https://github.com/bridgedao/org/blob/master/Paperclip%20MVP.md)(needs revision)
4. [Aragon Nest Proposal](https://github.com/bridgedao/org/blob/master/Aragon%20Nest%20Proposal.md)
5. [License](https://github.com/bridgedao/org/blob/master/LICENSE)

# Paperclip Lite
*Trustless fiat interface for popular common business services and expenses of smart contracts.*

## Claims:
**1. Trustless:** there is no single trusted intermediary, behaviour of the network is predefined and enforced by smart contract
**2. Safe:** all transactions are overcollateralized in DAI and held by a smart contract
**3. Legal:** smart contracts are not legally recognized, but their services are. Services and participants (smart contracts) are welcome to participate only if all their services are legal, understandable and auditable.
**4. Cheap:** no conversion costs
**5. Interoperable:** easily interacts with both physical world and smart contracts
**6. Consensus inducing:** every interacting party has more to lose than gain from a dispute
