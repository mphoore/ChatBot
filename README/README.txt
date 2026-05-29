Part 2 
This part is enhanced with Graphical user interface where users can now visually see the application with beautiful user friendly design. Firstly page of the application is where the user sees the home page with the logo and button to proceed and takes them to the next page. The second page is where now where the user will enter their name in order for the application to store their name in the computer memory in the secondary storage device which is the RAM random access memory (RAM). Once the user has entered their name they will then come across the chats window where the user can now ask the AI chat bot questions regarding cybersecurity and how to protect themselves from cyber attacks. The chat bot can also respond to the user based on how their are feeling towards a certain topic which is making users to be worried about their safety online, this is a process called sentiment detection.

The following information will elaborate how all files integrated interact together cohesively:

MainWindow.xaml- is the front end design page of what the user will see when they use the application which are designs. Firstly there is the parent Grid which is the one that allows us to work on the whole application. then we have the child Grid which make up all the different page that the user will interact with as they using the application step by step.
The first child Grid is the home_Grid which is the home page that shows the user the logo and button to proceed this button has a event handler that will take the user to next page if the button is clicked.
The second child Grid is the username_grid page for capturing the username. This page is responsible for prompting the user for their name which will then store the name is a file for future reference as the application must remember the name of the user and constantly respond to the user's questions using their name. then the user can click the button which has a event handler to take the user to the next page.
The third Grid is the chats_grid page, the user will be taken to a page where they can then have a conversation and the user can ask questions related to cyber security. The user will ask a question in the textbox below then click on the send button which is also handled by the event handler, the AI chatbot will then respond to those questions, speech bubble are used to show what the user and the BOT are talking about.








  