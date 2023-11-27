Current Streak: 8
All Time Best Streak: 8

# The Busy Person's Intro to LLMs
#Tags: #AndrejKarpathy #llm #DataScience #YouTube

I generally enjoy Andrej's content and am looking forward to his overview of LLMs. The notes below are my takeaways from his video found [here](https://www.youtube.com/watch?v=zjkBMFhNj_g).

# Notes
- A LLM is just two files. The parameters files and some code that runs those parameters. 16-bit model, every parameter is 2 bytes, 70 billion parameter model is 140GB. Run file takes the paramters and then runs the model. Run file can be any language but C and Python are most common. 

- Computational complexity comes when we try to get the parameters. Training much harder than inference. 
    - EX. LLaMA 70B:
        - 10TB of text (crawl of the internet) 
        - -> train the model on 6k GPUs for 12 days (~$2M, ~1e24 FLOPS) 
        - -> ~140GB file. State of the art multipy the numbers above by 10. 

- LLM is a next word prediction model. This forces the network to learn a lot about the world.

- How does it work?
    - Billions of parameters are dispersed through the network.
    - We know how to iteratively adjust them to make predictions better but not how the parameters collaborate to make predictions.

- Finetuning
    - Swap out training documents from internet crawl to examples of interest.
    - Pretraining is high volume/low quality (knowledge)
    - Finetuning is low volume/high quality (alignment)

- How to train
    - Stage 1: Pretraining (~ once a year)
        - Download ~10TB of text
        - Get cluster of ~6k GPUs
        - Compress text into a neural network (takes ~12 days and costs ~$2M)
        - Obtain base model
    - Stage 2: Finetuning (~ every week)
        - Write labeling instructions (how should model behave)
        - Collect 100K high quality Q&A responses
        - Finetune base model on this data (~ 1 day)
        - Obtain assistant model
        - Run evaluations
        - Deploy
        - Monitor, collect misbehaviors (input to step 1 next week)
    - Stage 3: Comparisons (optional)
        - Compare answers instead of writing answers (RLHF)

- Chatbot Arena
    - Leaderboard maintained by Cal Berkeley
    - Uses Elo rating (pose same question to each model, rank outputs, repeat)
    - Open source is chasing proprietary models

- Scaling Laws
    - Performance of LLMs is a smooth, well-behaved predictable function of:
        - N, # of parameters
        - D, amount of text we train on
    - We expect more intelligence by scaling

- Tool use is a major aspect in how these LLMs are improving
    - Uses calculator for calculations
    - Opens command line tools for code generation
    - Uses DALL-E for image generation

- System 2
    - System 1: Quick, instinctive thinking
    - System 2: Rational, slower, complex decision making
    - LLMs currently only have a System 1. Predicting next word and each next word takes the same about of time.
    - Interest in developing System 2 for LLMs. Telling the LLM to take its time and think through an answer before giving a response.

- Self-improvement
    - Two ways to learn
        - Imitate experts
        - Self-improvement, reward = win the game, think AlphaGo
    - What is equivalent of AlphaGo self-improvement for LLMs?
    - Main challenge is lack of reward criterion

- Customization
    - Customize LLMs so they become experts at specific tasks

- Jailbreaks
    - Directly asking for "bad" info is typically rejected. Creating a sweet story around the bad info can bypass security. 
    - Can also encode nefarious questions in base 64 or other way to get around security measures.
    - Messages hidden in images can be used bypass security measures.
    - People might start to put malicious links in webpages that LLMs will then use.
