Part 2 

This part is enhanced with Graphical user interface where users can now visually see the application with beautiful user friendly design. Firstly page of the application is where the user sees the home page and is welcomed to application with a voice greeting, then the logo and button appear to enable the user to proceed and takes them to the next page. The second page is where now where the user will enter their name in order for the application to store their name in the computer memory in the secondary storage device which is the RAM random access memory (RAM). Once the user has entered their name they will then come across the chats window where the user can now ask the AI chat bot questions regarding cybersecurity and how to protect themselves from cyber attacks. The chat bot can also respond to the user based on how their are feeling towards a certain topic which is making users to be worried about their safety online, this is a process called sentiment detection.



The following information will elaborate how all files integrated interact together cohesively:

MainWindow.xaml- is the front end design page of what the user will see when they use the application which are designs. Firstly there is the parent Grid which is the one that allows us to work on the whole application. then we have the child Grid which make up all the different page that the user will interact with as they using the application step by step.
The first child Grid is the home\_Grid which is the home page that shows the user the logo and button to proceed this button has a event handler that will take the user to next page if the button is clicked.
The second child Grid is the username\_grid page for capturing the username. This page is responsible for prompting the user for their name which will then store the name is a file for future reference as the application must remember the name of the user and constantly respond to the user's questions using their name. then the user can click the button which has a event handler to take the user to the next page.
The third Grid is the chats\_grid page, the user will be taken to a page where they can then have a conversation and the user can ask questions related to cyber security. The user will ask a question in the textbox below then click on the send button which is also handled by the event handler, the AI chatbot will then respond to those questions, speech bubble are used to show what the user and the BOT are talking about.




MainWindow.cs- is the back end part of the application that is responsible for handling the interaction between the user and the application. Modern, strongly-typed generic structures (List<string>) replace previous collections to maintain primary message answers and noise-filtering words in the MainWindow class constructor, which initializes the application's fundamental architecture. The layout engine loads peripheral data components, builds the user interface, and initiates an audio greeting upon launch. Then, using a specific procedure, the application modifies element visibilities to manage views. The user is first presented with a landing screen; clicking the proceed trigger hides this initial panel and unrolls the registration interface. Before the core chat module can be accessed, the submit action validates the text box to confirm that the input is not null or empty whitespace. Once validated, it calls a dedicated profile class to set up the identity registers, caches the string locally, updates the primary display panel, and transitions the user into the active chat room. To ensure system stability, a rigorous filtering and processing pipeline is applied to the data when a user submits a question. A sanitation approach supported by regex is applied to the raw text, which verifies each letter, eliminates complicated symbols, maintains alphanumeric elements, and collapses irregular spaces into consistent spacing. This keeps the matching logic from being broken by punctuation.



An interest-tracking engine processes the cleaned text once it has been divided into lowercase words. A background sub-routine uses a duplicate-rejecting HashSet to isolate the surrounding keywords if the token "interested" is found. The application checks a local file named interested\_topic.txt for the active profile. If the user already has saved interests, it extracts the historical data, blends it with the new entries, and overwrites the file. If no profile exists, a new record is appended to the text file.



For standard questions, the system loops through its internal memory bank to match user keywords against pre-defined answers. To prevent repetitive interactions, a random index selector selects a response if multiple variations are found. If the input matches no known keywords, the system defaults to a randomized fallback phrase. The system maintains engagement through automated reminder loops and real-time interface rendering. Every interaction advances a tracking counter. When this counter reaches three, the routine searches the text file for the user's specific interests. It injects a custom notification into the chat feed and routes those interests back into the central language processor, causing the chatbot to automatically generate contextual data matched to the user's preferences before resetting the counter back to zero. Because live conversations are unpredictable, the visual message blocks are constructed programmatically in the code-behind file rather than relying on static design files. The rendering method evaluates the sender's identity to apply distinct formatting. Chatbot messages receive light blue message borders and dark blue bold headers, while human responses use light gray backdrops and dark green headers. The layout sets explicit text wrapping to keep long strings from clipping past the screen boundaries, and dynamically invokes auto-scrolling commands to anchor the view to the latest message entry.




VoiceGreet.cs- This cs file is a class that is responsible for playing the greeting sound. The method is called to play the sound named greet. The bin/Debug is replaced from the path with greeting.wav.The instance of the sound player class is then created with a method to play the sound.




user\_name.cs- The core logic of this username management class operates as a sequential data pipeline that sanitizes raw interface inputs, manages a flat-file database, evaluates historical states, and compiles dynamic UI components on the fly. Upon receiving text from the input layer, the engine verifies the infrastructure using File.Exists to check for user\_names.txt, automatically initializing it with a default "auto\_create" header via File.WriteAllText if it is missing. The user's input is then stripped of any preceding or trailing spacing artifacts using a clean .Trim() method to prevent unintended whitespace from corrupting downstream evaluation metrics. Once prepared, the engine reads the historical log file into system memory using File.ReadAllLines, splitting each text line into a one-dimensional string array. A foreach loop scans this array using a case-insensitive StringComparison.OrdinalIgnoreCase evaluation, ensuring that variations like "Alice" and "alice" point to the exact same profile, which effectively prevents duplicate entries within the flat-file database. The Boolean outcome of this database search drives a conditional branch that controls data persistence and presentation formatting. If the username is entirely new, the execution path triggers a registration workflow where File.AppendAllText writes the clean name to the bottom of the log file along with an introductory greeting payload. If the name is already registered, the logic safely forks away to bypass the expensive disk-write operation entirely, instantly switching the text context to a "welcome back" prompt before returning the active name string to the main application controller. Finally, this text payload is handed down to a visual rendering engine to be programmatically assembled into layout elements inside system RAM. By evaluating the sender's identity, the system dynamically assigns styling properties—such as blue themes for the bot and gray themes for the user—while enforcing TextWrapping on the text containers to prevent layout clipping before injecting the completed Border capsule straight into the live chat timeline.




respond.cs- The logic of the respond class operates as a lexicon configuration engine and a knowledge seed repository, populating empty data collections injected from the main application layer to establish a dictionary for a rule-based Natural Language Processing (NLP) pipeline. Its class constructor intercepts reference handles for two primary data lists and routes them to private seeding utilities. By modernizing this framework to use strongly typed List<string> structures instead of legacy ArrayList collections, the system avoids boxing and unboxing performance issues while enforcing type safety. Because C# passes these objects by reference, populating the lists inside this utility automatically updates the active data streams in the main window controller, creating an interconnected runtime memory architecture. To filter out conversational noise, the system maps everyday grammatical filler terms—such as prepositions, pronouns, and conjunctions—into a flat token filtration matrix. Populating this ignore list with terms like "and", "the", and "because" allows the chatbot's string parsing loop to strip away linguistic noise and isolate the user's true core intent. Concurrently, the knowledge base is built using a strict metadata pattern where every single string entry is structured with a categorical prefix key, such as "vpn" or "phishing", followed directly by its corresponding response value. This dual-engine database covers both technical informational modules and primitive sentiment adjustment hooks, allowing the main program's matching routine to effortlessly iterate through the rows, call a .Contains() search substring check, and pull categorized text blocks to pass back to the user interface.










  
