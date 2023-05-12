# gpt-go
A gpt4 system selector + one-shot prompt gui

The provided code is a Tkinter-based interface that interacts with OpenAI's GPT-4(or 3.5-turbo) model by sending text prompts and displaying the generated responses. 
Users can choose from a list of predefined systems (code, text, or data systems), enter their input and context, and receive a generated output based on the selected system and input.

Code Structure:
1. Import necessary libraries: tkinter, openai, datetime, and ttkthemes.
2. Set the OpenAI API key.
3. Define variables for different types of systems (text_systems, code_systems, and data_systems). Each system has a specific purpose and functionality that can be requested by the user.
4. Define the function 'button_clicked()' which takes the option selected by the user and the group it belongs to as input. This function uses the selected option to construct a prompt for GPT and calls the function 'run_gpt()' to obtain a response.
5. Define the function 'save_to_history()' which saves the timestamp, prompt, response, and system used for each query.
6. Define the function 'run_gpt()' which takes the user's prompt and the selected system type, sends a request to the OpenAI GPT model, prints the response, and saves the output to the history file.
7. Define utility functions for file manipulation, text entry, and clipboard operations for easy input/output handling in the GUI.
8. Initialize the main tkinter GUI window and set its title.
9. Set up the GUI layout and style for input, context, and output frames.
10. Create widgets (Labels, Entries, Buttons, Text, and Scrollbar) for each frame and configure them for proper display and functionality.
11. Define the main event loop which waits for user actions and updates the GUI accordingly.
12. Close the tkinter window when the user finishes interacting with the chatbot.

Limitations:
1. GUI becomes unresponsive after submitting a request, and only becomes responsive again after the response is received. Multiple requests can be sent simultaneously by opening multiple GUIs however. 
2. Can be expensive due to the cost of GPT-4. This code structure can also use the GPT 3.5 turbo model, which is cheaper but less powerful and has a smaller token limit.
3. Speaking of token limits, GPT 4 has a token limit of 8000. This can limit its ability to summarize larger amounts of text sufficiently.
4. Something else I can't think of right now...
