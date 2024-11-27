### LLMs as Operating Systems: Agent Memory
\
An LLM's input context window has limited space. Using a longer input context also costs more and results in slower processing. So, managing what's stored in this context window is important. \
\
In the innovative paper MemGPT: Towards LLMs as Operating Systems, its authors (which include the instructors) proposed using an LLM agent to manage this context window. Their system uses a large persistent memory that stores everything that could be included in the input context, and  an agent decides   what is actually included. \
\
Take the example of building a chatbot that needs to remember what's been said earlier in a conversation (perhaps over many days of interaction with a user). As the conversation's length grows, the memory management agent will move information from the input context to a persistent searchable database; summarize information to keep relevant facts in the input context; and restore relevant conversation elements from further back in time. This allows a chatbot to keep what's currently most relevant in its input context memory to generate the next response. \

---------
#### Notebooks contents:

- L1: Basic Intro
- L3: First implementation of MemGPT. All the different structures, tools used and types of memories that can be made and accessed.
- L4: Setup and working example of memgpt
- L5: Importing data into archival memory, connecting to external tools, performing search
- L6: Implementing Multiple agents orchestration (Complex and resource intensive, as their are many LLM calls, Therefore slightly more expensive)