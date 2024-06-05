# CaT

Github page for paper **Context-Aware Tracking and Dynamic Introduction for Incomplete Utterance Rewriting in Extended Multi-Turn Dialogues** accepted by Findings of ACL 2024

# Data

Our experiments are concstructed on the three benchmarks covering both English and Chinese
1. [CANARD](https://sites.google.com/view/qanta/projects/canard) is a representative English IUR dataset derived by QuAC, an open-domain conversational question answering dataset about specific Wikipedia sections.
2. [CQR](https://github.com/alexa/alexa-dataset-contextual-query-rewrite) is an English IUR dataset extended from task-oriented dialogue between drivers and an in-car assistant.
3. INSQR is a constructed challenging Chinese IUR dataset, which is collect by the real dialogues between customers and sales from our Alipay Platform. For the sake of data privacy, please contact us though email to get dataset.

# Prompt of Context Tracking
Take Canard for example：
```
You are now required to undertake a task of Key-phrase Tracking. In each case, you will receive a list of "dialogues", and you need to dynamically maintain a "key-phrase list" for each turn of dialogue in the dialogue list. Each element in the key phrase list is extracted from the original dialogue text. The dynamic maintenance process includes: 1. Addition (when new important elements appear), 2. Deletion (when the dialogue topic shifts, old elements which only relevant to the former subtopic are removed); for each turn of dialogue, you need to output the corresponding key-phrase list. The following are some examples. 
dialogue 1: 
[1] Meat Beat Manifesto
[2] Early years
[3] What happened in the early years?
[4] Dangers and Stephens had formed the English pop group Perennial Divide in 1986 with Paul Freeguard.
[5] Did they release any albums?
[6] They left Perennial Divide in 1988 to record a full Meat Beat album.
[7] Was Meat Beat successful?
[8] The tapes of what would have been the debut MBM album were claimed to have been destroyed in a studio fire before it could be released
key-phrase list 1: 
[1] Meat Beat Manifesto
[2] Meat Beat Manifesto || Early years
[3] Meat Beat Manifesto || Early years
[4] Meat Beat Manifesto || Early years || Dangers || Stephens || Perennial Divide || in 1986 || Paul Freeguard
[5] Meat Beat Manifesto || Early years || Dangers || Stephens || Perennial Divide
[6] Meat Beat Manifesto || Early years || Dangers || Stephens || Perennial Divide || in 1988 || Meat Beat
[7] Meat Beat Manifesto || Early years || Dangers || Stephens || Perennial Divide || in 1988 || Meat Beat
[8] Meat Beat Manifesto || Early years || Dangers || Stephens || Perennial Divide || in 1988 || Meat Beat || studio fire
dialogue & key-phrase list 2-5: ... 
Now I am providing you with a list of dialogues. Please output the corresponding key-phrase list, each turn of dialogue corresponds to one line of the key-phrase list. Only output the key-phrase list!
```


