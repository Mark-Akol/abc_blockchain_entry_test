# Part A: MCQ Answers

**Status:** [In Progress / Submitted]  

---

## Instructions
**COMPLETE ALL QUESTIONS FOR BOTH PART 1 AND PART 2 BELOW**

---

## PART 1: Renewable Energy Trading Platform (Real-World African Context)

**Scenario:** You are hired as a blockchain developer to build a decentralised renewable energy marketplace for African solar micro-grid providers. The platform must:

- Allow providers to list solar energy credits as NFTs with generation certificates  
- Enable buyers to swap tokens for energy credits using a DEX  
- Store provider reputation scores transparently  
- Process payments without intermediaries  

---

### Question 1: Architecture Decision (Technical Reasoning)

**Which combination of technologies demonstrates the best understanding of blockchain fundamentals for this use case?**

- **A)** Use ERC-721 for each energy credit, build a centralised database for reputation, and integrate Binance for payments because CEXs have better liquidity.  
- **B)** Use ERC-1155 for energy credits (enabling batch listings from providers), implement reputation as on-chain mappings in the marketplace smart contract, and integrate with a DEX like Uniswap for direct provider-to-buyer swaps to minimise intermediaries.  
- **C)** Use ERC-721 exclusively, store all data off-chain for gas savings, and require buyers to use MetaMask with manual price negotiations.  
- **D)** Build everything as separate NFT collections with no DEX integration since providers won't understand DeFi protocols.  

**Your Answer:** [B]  

**Your Reasoning:**  
[2–3 sentences explaining why you chose this answer. What makes it the best choice?]

DEX Integration:
We want to process payments without intemediaries, so DEX (Decentralized Exchange) will allow the buyer and seller to swap tokens directly through the smart contract - which fulfills the peer-to-peer marketplace.

ERC-1155 (Energy Credits) : 
Addditionally, because the production will be for more than one unique product (i.e Not 1 unique piece of digital art), ERC-1155 allows for 'batching' which will help greatly save on gas fees and help manage inventory easier, as opposed to minting 100 separate NFTs.
---

### Question 2: Cost Optimisation (Practical Aptitude)

A solar micro-grid provider wants to list 40 energy credit bundles. Gas costs are:

- **ERC-721:** 100,000 gas per NFT mint  
- **ERC-1155:** 150,000 gas for first mint + 5,000 gas per additional item in batch  

**Current gas price:** 20 gwei  
**1 ETH = $3,000**

**What is the gas cost difference between ERC-721 and ERC-1155 for listing 40 items?**

- **A)** ERC-721 is cheaper by $15  
- **B)** ERC-1155 is cheaper by approximately $27  
- **C)** They cost exactly the same  
- **D)** ERC-1155 is cheaper by approximately $180  

**Your Answer:** [D]  

**Your Calculation/Reasoning:**  
- ERC-721 cost = [Show calculation]
- ERC-1155 cost = [Show calculation]
- Difference = [Show calculation]

Comparative Costings:
1. ERC-721: 
Given that every item costs 100,000 gas to mint (expensive)
Therefore - 40 items x 100,000 = 4,000,000 total gas
2. ERC-1155:
Given that the 1st item costs 150,000 gas to mint and the other 39 are only 5,000 each (discount based option)
150,000 + (39 x 5,000) = 345,000 total gas
3. Difference:
4,000,000 - 345,000 = 3,655,000 gas saved (difference)

Given the 20 gwei : 3,655,000 x 20 gwei = 73,100,000 gwei.
Given that there are 1,000,000,000 gwei in 1 ETH ~ 73,100,000 / 1,000,000,000 = 0,0731 ETH
Convert to dollars - 0,0731 x $3,000 (given) = $219,30

This option does not exist, however 219,30 is closest to D (in the event that I made an error in my calculations)


[Explain why gas optimisation matters for African users]  

In essence, I believe that this gas optimisation matters for users across the globe, but especially in Africa because: 

Financial inclusion & Scalability : As high gas fees create a big portion of many African users transactions and as such would create a barrier to entry. Additionally, because users in Africa might trade in small / smaller amounts - it would be conterproductive to have high gas costs that outweight the amounts being dealt with.

Adoption : Lowering technical and financial barrier costs can encourage African users to build trust in decentralised systems, which would encourage adoption. If something is too expensive in Africa - you greatly limit the number of users that wouldbe keen on the offering.

---

### Question 3: Value Proposition Explanation (Communication & Thinking)

A micro-grid provider asks: *"Why can't we just use a normal website with a database?"*

**Which response demonstrates understanding of blockchain's actual value (not just its technology)?**

- **A)** "Blockchain is the future; everyone should use it."  
- **B)** "With blockchain, no middleman can manipulate your pricing or payment records. If a buyer claims they paid but you didn't receive funds, the blockchain provides immutable proof. Plus, your reputation score can follow you to other platforms since it's on-chain – it's your data, not the platform's."  
- **C)** "Because smart contracts are more secure than databases and Web3 is decentralised."  
- **D)** "Blockchain uses cryptography which makes it unhackable, unlike normal databases."  

**Your Answer:** [B]  

**Your Explanation:**  
[2–3 sentences explaining what makes this answer correct. What did you learn about why blockchain matters in Africa?]  

I believe that option B highlights the key focus and value of blockchain: decentralisation and immutability.

Ive learnt that:
In the African context, trust in centralized systems can sometimes be low - therefore, if you can help users understand and know about using a platform where reputation and payments are transparent and unchangable, users in Africa can participate in transactions that are fair for small energy providers and buyers. Ultimately, blockchain fosters for a peer to peer economy that does not need middlemen to manage the data.


---

## PART 2: DeFi & NFT Integration (Advanced Concepts)

**Scenario:** A DeFi protocol experiences the following sequence of events:

- A liquidity provider adds 5 ETH and 15,000 USDC to an AMM pool (constant product formula: x × y = k)  
- A trader swaps 1 ETH for USDC (no fees for simplicity)  
- The protocol's governance token holders vote on implementing impermanent loss protection  
- An NFT marketplace integrates with the DEX to enable ERC-1155 token swaps  

---

### Question: Multi-Concept Synthesis

**Which statement correctly combines understanding of AMMs, governance, and technical implementation?**

- **A)** After the 1 ETH swap, the liquidity provider will have exactly the same USD value as before because the constant product formula maintains equal ratios. ERC-1155 tokens cannot be traded on AMMs since they support both fungible and non-fungible characteristics.  
- **B)** The trader will receive approximately 2,500 USDC from the swap (calculated using k = 5 × 15,000 = 75,000,  prices. ERC-1155's batch transfer capability makes it more gas-efficient than ERC-721 for marketplace integration.  
- **C)** The liquidity provider experiences impermanent loss because the pool maintains a constant product rather than constant ratio. ERC-721 would be more suitable than ERC-1155 for the NFT marketplace since individual NFTs require unique transactions.  
- **D)** The constant product formula prevents any impermanent loss by automatically rebalancing. DAOs cannot implement financial protections due to smart contract immutability. ERC-1155 tokens are incompatible with standard DEX protocols.  

**Your Answer:** [B]  

**Your Reasoning:**  

- **AMM Mathematics:** How do you calculate the swap output? What happens to the liquidity provider's value? 
*** We use the (deleting for space........) 
- **DeFi Governance:** What is impermanent loss and how does protection work?  
- **Token Standards:** Why might ERC-1155 be preferred over ERC-721 for marketplace integration?  

[2–3 sentences synthesising these concepts into a coherent explanation]  

We can use the constant product formula (x * y = k) to determine that swapping 1 ETH into a pool of 5 ETH and 15,000 USDC results in a 2,500 USDC payout for the trader. 

While liquidity providers face risks like impairment loss, implementing governance-led protection ensures that the pool remains stable and fair for all those partaking. 

Lastly, leveraging the ERC-1155 standard is the best technical choice because its batch-transfer choice as its batch transfer capabilities significantly reduce gas costs for users compared to traditional NFT standards.

---

## SUBMISSION CHECKLIST

- You answered all questions for **BOTH PART 1 AND PART 2**  
- Your answers include reasoning (not just A/B/C/D)  
- For PART 1 Q2: You showed your gas cost calculations  
- For PART 2: You addressed all three concept areas (AMM, Governance, Token Standards)  
- You committed and pushed to GitLab  

---

**Challenges faced:** [What was difficult? Which concepts are you less confident about?]  