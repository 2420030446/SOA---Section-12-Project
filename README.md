Abstract :

Digital mental-wellness systems often focus on conversational response generation while treating accessibility,
emotional context, wellness guidance, and safety-oriented risk handling as separate concerns. 
This paper presents MindBridgeAI, a service-oriented multi-agent platform designed to integrate these capabilities into a single modular architecture.
The system decomposes the interaction workflow into specialized services for emotional assessment, accessibility adaptation, wellness guidance,
crisis-risk detection, and final response generation.
A central orchestrator coordinates these services through well-defined interfaces, making the architecture loosely coupled, reusable, and scalable. 
The implementation is designed to operate with a replaceable large-language-model (LLM) backend and includes a lightweight demonstration backend for validating the complete
service flow in resource-constrained environments.
Evaluation is aligned with the ESConv emotional-support benchmark and the
protocol used by the MultiAgentESC base study, including Distinct1/2, BLEU-1/2/3, F1, and ROUGE-L. 

A. Emotional Support Conversation

Emotional support differs from ordinary question answering because the quality of a response depends on recognizing the
user’s emotional state, the cause or context of the difficulty,
and the support strategy that is appropriate to the situation.
ESConv was developed to support this research direction with
help-seeker and supporter conversations and annotations related
to support strategies [1]. The dataset established a common
experimental setting for evaluating dialogue systems intended
to provide emotional support.

B. Accessibility Gap
Accessibility is not equivalent to simply adding a voice
option. A truly accessible conversational system must consider
how a user interacts with the interface, the complexity of
language, the presentation format, and assistive technology
compatibility. Grassini et al. report that only four of the 21
healthcare chatbot applications reviewed were accessible, with
only one designed specifically for people with disabilities
[3]. Their analysis calls for accessibility-by-design, including
attention to interface, navigation, speech, visual output, and
screen-reader considerations.

C. Need for Context-Aware Wellness Support
Conversational agents have also been studied as tools for
symptom-management and support interventions. Yang et al.
reviewed randomized controlled trials involving conversationalagent interventions for physical and psychological symptoms
and identified feasibility, acceptability, and effectiveness as
important evaluation dimensions [4]. MindBridge does not
claim to diagnose or treat medical conditions. Its wellness
service is deliberately positioned as a non-clinical support
component that uses contextual information to produce general
wellness-oriented suggestions.

D. Multi-Agent Systems
Multi-agent LLM systems decompose complex tasks across
specialized roles. AutoGen, for example, provides mechanisms
for composing multiple conversable agents and coordinating
flexible interaction patterns [7]. Recent surveys also identify
workflow design, infrastructure, communication topology, and
coordination as central issues in LLM-based multi-agent
systems [6]. MindBridge applies this design pattern to mentalwellness interaction while emphasizing SOA modularity
