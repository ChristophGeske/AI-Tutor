# AI-Tutor
Large-Language-Models (LLMs) are powerful AI models that can generate natural language texts and programming code for various purposes and tasks. Students in higher education use tools like ChatGPT already to learn and create projects in various fields. However, not all subjects are equally affected by these tools.

The subjects that are most transformed by Large Language Models are as the name suggest languages. But also programming can be considered a language hence the term programming language used in computer science (cs).
The field of cs benefits immensely and one could argue it is truly transformed by these tools because of several factors that we will explore in detail later. 

Therefore, educators, pupils and schools should also have access to these tools, but not simply by access to it via a chat interface that can't be modefied but instead in a way that suits the specific needs aof schools, educators and pupils.

To explore the benefits of LLMs tailor made for education the aim of this project is to develop a flexible Intelligent-Tutoring-Systems (ITS) for K-12 students that focuses on cs as a subject that could benefits the most from a personalised digital Tutor.

Whats the value of an AI-Tutor when we have ChatGPT?

At the core of all this is the LLM. The magic is mostly provided by the LLM and many people are happy with the core functionality that the chat interface offers. 
The chat/voice interface seems to be the most general interface possible, it is easy to use and suitable for all kind of users from students to professionals. 

However there are two big ideas this projects builds on:

1.) An optimized user interface (Frontend)
2.) LLM performance improvemnts via additional software, data and prompting strategies. (Backend)

These ideas are by no means new, there already exists a term for software build based on these two ideasa and are called GPT-Wrappers. Meaning software that incorperates ChatGPT to offer new capabilities to already sucessfull tools or enabling completly new tools which depand on the outputs of the LLM.

For 1.) evey project will have different requirements and the design will be optemized for the targeted use case. The UI will be the outermost layer the user will see and interact with and can reach from a simple chat interface to a talking avatar in virtual reality.

The ideas for 2.) will be mostly run in the background and here another seperation makes sense:

2.1.) A core layer around the LLM which improves the output and optimizes the inputs. This layer is so general that all projects benefit from it. 
This is also the layer Open AI constently improves by offering features like "Custome Instructions" and "Memory" which are forms of prompt engineering adding commands to each prompt in the background or "Retrieval-Augmented Generation" (RAG) allowing the addition of personalized data the LLM has fast and efficient access to. 
Furthermore there are many prompt engeneering strategies lige Agents that can improve the output but come with the trade off of higher cost because of higher compute. Also when the prompt gets longer the amount of user input tokens the LLM can process. However advances in the amount of usable tokens makes this less of an issue.

This core layer should be as flexible as possible ant it should be easy to replace this core module even in a finished software. Ideally it has as few interactions with higher layers as possible so that replacing it when an improved version is released becomes simple.

2.2.) After the core layer should come another layer that sits just below the UI layer. Here data specific to the software should be processed. Some of the data here never reaches the core module for example one could image that the output always ends with a link to the social media sites which is simply concatinated to the output of the core module. Also one could imagine multiple agents that are based on the core module interact with one another and the logic is defined in this layer. Also data like the time or location for example which might not be known to the core module could be combined with the input data and then send to the core module. Also the output of the core module could be modefied or checked for example if you want to keep the output a certain lenght a method could loop over the output and if it determines that it is to short or long it outomatically could reprompt the core module to redo the answear. 
