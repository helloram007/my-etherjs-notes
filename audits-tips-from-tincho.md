[Audit Youtube Link](https://github.com/PatrickAlphaC/hardhat-security-fcc).


- Add comments
  - This will help your auditors understand what you're doing.
- Use natspec
  - Document your functions. DOCUMENT YOUR FUNCTIONS.
- Test
  - If you don't have tests, and test coverage of all your functions and lines of code, you shouldn't go to audit. If your tests don't pass, don't go to audit.
- Be ready to talk to your auditors
- The more communication, the better.
- Be prepared to give them plenty of time.
- They literally pour themselves over your code.
> "At this time, there are 0 good auditors that can get you an audit in under a week. If an auditor says they can do it in that time frame, they are either doing you a favor or they are shit. " - Patrick Collins, March 4th, 2022

## When writing good code, you 100% need to follow these before sending you code to an audit.
1. You cannot imagine the countless hours you save an auditor by just stating what you intend to do with that crazy obscure low-level assembly math thing that just multiplies two numbers. So, add comments.
2. Document everything that is part of the contracts' public API. If functions are private . internal but are super sensitive, document them as well. Big big big plus for using NatSpec format!
3. Test! Countless critical vulns can be saved with simple unit tests. Also, tests let us understand intended behavior. A trick some auditors use: if a public function is not being called in the tests, that's where they aim their guns. Yes, it really works to find bugs
4. An easy one, but so overlooked. Make sure the project compiles and test suite passes. Yeah, that basic. First thing we do before auditing is building and running the tests. It’s just sooo disappointing when it fails.
5. Don’t assume that we’ll know your code, or we’ve heard of that EIP you’re implementing, or we’ve seen that crazy algorithm . data structure you’re coding. We need documentation, and time to understand it. So have plenty of docs ready for us to start digging on the first day.
6. Be ready to have an open comms channel. There’ll be lots of things we don’t understand, and we’ll need you to help. Depending on the auditors’ style we might be more quiet or more chatty, but knowing that you’ll be there and responsive is SUCH a big plus.
7. Don’t try to be so clever with optimizations. First code for correctness and security. I’ve seen so many vulns coming from trying to optimize simple operations. And if you use some obscure trick to optimize, add comments explaining why.
8. A crazy naming system doesn’t make anyone a better dev. It just badly hinders onboarding of new people to the ecosystem. U cn b bttr thn ths.
9. Clean up old comments, unused functions, etc. Make your code shiny and pretty. We’ll be reading it for weeks, and it’s tough having to spend so many hours reading something that is SO difficult to look at.
10. Some projects to check dev practices: Uniswap, Augur, Compound, UMA, Optimism. Not only see their Solidity. See how they test, deploy, upgrade. See the open discussions in issues and PRs. They might not be perfect, agreed, but I’ve really enjoyed reading their code.
11. Don’t reinvent the wheel. It’s 2021, and you shouldn’t be coding your own ERC20 from scratch. Same for other ERCs, governance, access controls, etc. Use known secure libraries. It's safer, the audit’s scope will be smaller, and you’ll save money.
12. Try not to be so secretive about your roadmap and future developments. We'll likely ask about it. The more you share, the easier it'll be to understand the big picture of what you're building, and what kind of attack vectors are more relevant.
13. Auditing a moving target is so complicated we need to constantly adapt and change our mental model of the system. So if you can keep that commit frozen, or at least plan in advance when you'll change it, oh dear we'll WORSHIP you.
14. If you can run some high level code walkthroughs for us, specially on the first days, that's gonna be great. Imagine we're a dev you're onboarding to your code base: what'd you show ? what'd you warn ? what'd you highlight ?
15. Ideally, I think should see a security audit as valuable process beyond finding or not a specific critical issue. Of course we want to do that, but we can also have insightful conversations just asking and entertaining ideas for attack vectors, design considerations, etc.
16. From day one, think of the audit as a best-effort code review with a security-oriented adversarial mindset. Lots of misconception and false expectations come from confusions with the “real” legal . financial auditors. We're not that kind (nor plan to be).
17. Considering that, don’t assume we'll find every single vulnerability forever and that your code is perfect once the audit is done. Not even if after our report you managed to fix everything. Which means...
18. Security incidents can happen after an audit. Be sensible, assume you can be hacked, get insurance, and set up monitoring infrastructure and recovery plans.
