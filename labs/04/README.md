# Lab 4: Agentic coding

- Partner: Hafssa Zainou
- Pair repository: [HafssaZainou/co2-pipeline](https://github.com/HafssaZainou/co2-pipeline)
- AI usage of our pair: [AI_USAGE.md](https://github.com/HafssaZainou/co2-pipeline/blob/main/AI_USAGE.md)
- Team pull request (AGENTS.md for the cinema project): [PR #16](https://github.com/chaymaeloukili/data-integration-projekt/pull/16)
- My agent setup: [setup.md](setup.md)

## What I will delegate, and what I will not

I did not answer the think–pair–share question before the lab, so I answer it now, after working with an agent. In our cinema project I will hand an agent the code that I can check quickly: a first version of a download or cleaning script, plotting code, and a draft of a README. I will never delegate the decisions behind that code: which population we divide by, what an empty cell means, and whether we show a result in tonnes or in percent, because each choice changes the answer that our audience takes home. The lab showed me why: in the fence test the agent tried twice to overwrite the raw data, and in the bug hunt all 13 tests passed while the world share was still wrong by a factor of seven, which we only saw by comparing with an independent number. This matches the slide "Your project: delegate vs. own", and I would add one row to it: checking results against a second source is a step I always do myself.