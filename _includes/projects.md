### Synthesizing correct programs from lightweight specifications

Automating programming _correctly_ has immense potential to increase programmer productivity. All program synthesis methods take as input some form of specification---a description of the user intent. Most formal methods synthesis rely on sophisticated expertise to provide high-assurance specifications. In contrast, recent LLM-based approaches use ambiguous natural language that cannot be checked for correctnes against the output. Can we find a middle-ground that uses some combination of lightweight formal methods, test cases, and LLMs to build practical programming automations with minimal user effort?

### Can types help in testing and synthesis of dynamic programs?

Random testing and program synthesis have emerged as complementary software assurance methods to type systems. Types help during program development; synthesis helps by automating some programming effort; and testing helps assure correctness after development. However, most random testing and synthesis tools rely on typed languages---excluding all programmers that use dynamic languages to write software! Recently gradual types have emerged to bring the benfits of typing to dynamic languages. Can we bring the philosophy of gradual typing to synthesis and random testing as well?

### Designing reliable cloud servers and APIs

Cloud services ranging from social networking to finance are an important part of our daily life; yet we face regular issues of downtimes, crashes, and even disastrous bugs. A key factor behind the complexity is the web server application state, backed by external and/or distributed databases. Additionally, network flakiness, asynchronous programming, and use of a myriad of external APIs make it difficult to reason about such programs. Can we build tools that aid programmers to build better cloud servers and REST APIs by reasoning about intermittent bugs like idempotency or consensus problems?