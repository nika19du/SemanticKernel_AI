# SemanticKernel_AI
C#

<img width="1107" height="632" alt="image" src="https://github.com/user-attachments/assets/84cc31c7-c5bf-479c-a146-477284fa6bc4" />

<img width="1125" height="1027" alt="image" src="https://github.com/user-attachments/assets/6dcd18aa-42a5-4a5d-9f34-99bd545ab2b7" />

<img width="1712" height="600" alt="image" src="https://github.com/user-attachments/assets/fa57493e-7019-4111-92a4-c2628f5ccccc" />


Understanding Semantic Kernel: Sk is at its core a library, so it's an SDK
created by Microsoft.It is very lightweight and also very extensible, which means that future changes to AI models can easily be integrated.
The goal is to abstract away the complexities of working with different AI models. So, in essence, Semantic Kernel acts as a middleware, providing an easy way to integrate different AI models into your applications. Without it, each AI provider has its own API with different request formats,authentication methods, and response handling. This means that if you wanted to switch AI providers, you'd have to rewrite large portions of your applications. Semantic Kernel removed that complexity by standardizing interactions across different models, allowing you to use the in unified way.

3 big benefits in using Semantic Kernel to integrate AI into your .NET apps: 
	- 1. Abstraction: Semantic Kernel provides an abstraction layer. It takes away the need we're seeing to understand how the different AI models work. Abstraction give us a higher-level unified way to interact with different AI models.
	- 2. Integration: it comes indeed with support for several core AI model features already integrated, like chat,text and image generation
	- 3. Extensibility: Semantic Kernel is build to be flexible. You can add plugins and extend it with additional AI services very easily.
	
Key Components of Semantic Kernel:
Semantic Kernel library consists out of a number of components which we can use separeately or in combination.
there's a Kernel. there's a AI Service connectors, then there's a very important building blcok called Funstions and plugins.
There's prompts and prompt templates. We can use memory and we can use filters

The kernel in Semantic Kernel:
	- Central component
	- Act as an orchestratior between our app and the AI models.
	- it is the kernel that handles the communication and ensures that the application interacts with these services in a unified way. One of its key responsibilities is managing services and plugins. With services, I mean AI models and logging mechanisms. While plugins extend AI functionality by integrating additional capabilities, such as calling external APIs or retrieving data from databases, the kernel brings these elements together.
	- the kernel also works as a dependency injection container, and by this I mean that it'll hold all AI services, plugins, and more that application requires and makes it accessible when needed. So we do an AI task like executing a prompt, the kernel will ensure that the right components are available and are used efficiently
Semantic Kernel is designed to work with multiple AI models, including OpenAI's GPT, Azure OpenAI, and other AI services. AI services require authentication, and an API key is what allows your application to securely communicate with them. 

Services: include AI models, like chat completion, text generation, or image creation, but they also extend beyond AI. The kernel can manage additional services, such as logging, HttpClient, or other utilities needed for your application. Allowing for dependency injection across different languages

Plugins: are additional components that help the kernel to perform specific tasjs beyond just calling an AI model. For example a plugin could fetch real-time data from an external API, retrieve database records, or trigger other application workflows. This makes the kernel highly extensible, as you can integrate AI-driven functionality with custom business logic.
So by combining services and plugins, the kernel becomes the central hub for AI operations in your application.




Prompt is instruction or input that we give to an AI model to get specific responses. Input to get desired output. It is how we ask the model to do something, whether it's answering a question, summarizing text, or generating an image. The key thing to remember is that the quality of the response depends heavily on how well the prompt is crafted.


* RAG - Retrieval-Augmented Generation
	- is technique to enhance AI-generated responses by bringin in
	relevant external data. Instead of relying only on the models build in training data,
	RAG allows AI systems to retrieve additional information from sources like databases, APIs, or document repositories. This ensures that responses are more accurate, well-grounded in real data, and contextually relevant. So, in essence, we will somehow get extra data. We share that with the AI so that it can create a better, more grounded response.
 **Retrieval: fetch relevant data from external sources, we used plug-ins to  get extra data. Using functions and plugins is a way to do RAG.
 Through the use of this extra data, we enhance the generation side of things. We will provide the AI model with extra data so that it can enhance its generated response.
 RAG will help us to steer the AI models so that the generated responses are better.
 It will definitely help with avoiding hallucination
 
 **Typical Use Cases for RAG:
	1. Customer support where AI-powered chatbots and virtual assistants can pull relevant information from knowledge bases, and perhaps past interactions to provice precise and helpful answers to customer inquiries.
	2. Research assistance - where RAG enhances the ability of AI to fetch the latest studies, papers, or technical documentations
	3. Healthcare: where accurate and timely information retrieval is definitely critical.
