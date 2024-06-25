# alexa
## Build an Artificial Assistant
## build your own alexa

## Installation
### For windows users

For the robot to listen to our voice/speech
`pip install speechRecognition`

To speak out, or text to speech
`pip install pyttsx3`

For advance control on browser
`pip install pywhatkit`

To get wikipedia data
`pip install wikipedia`

To get funny jokes
`pip install pyjokes`


if you are unable to install pyaudio you have to lower down your python version to <3.6 version 

This script is a good starting point for creating a basic voice assistant like Alexa. Here's a step-by-step explanation and improvements to ensure it works smoothly:

### Explanation and Improvements

1. **Voice Setup**:
   - The `pyttsx3` library is used for text-to-speech. You are setting the voice to the second voice available on your system.

2. **Listening for Commands**:
   - `take_command()` uses the `SpeechRecognition` library to listen to the user's command and process it. It listens for the keyword "alexa" to filter commands meant for the assistant.

3. **Command Execution**:
   - `run_alexa()` interprets the commands and performs actions like playing YouTube videos, telling the time, fetching information from Wikipedia, telling jokes, and responding to certain queries.

### Improvements and Fixes

1. **Handle Unrecognized Commands**:
   - Improve exception handling in `take_command()` to ensure the assistant can recover gracefully from errors.
   
2. **Fix the Command Flow**:
   - Ensure that commands are executed only if they contain the word "alexa".

3. **Loop Structure**:
   - The main loop should run continuously to listen for new commands.




### Notes
1. **Error Handling**:
   - Enhanced error handling in `take_command()` to provide appropriate feedback when speech recognition fails.

2. **Ambient Noise Adjustment**:
   - Adjust the microphone for ambient noise using `listener.adjust_for_ambient_noise(source)` to improve recognition accuracy.

3. **Continuous Listening**:
   - The assistant will continuously listen for commands in an infinite loop.

### Running the Assistant
1. **Install Dependencies**:
   Ensure you have installed all necessary libraries:
   ```bash
   pip install SpeechRecognition pyttsx3 pywhatkit wikipedia pyjokes
   ```

2. **Run the Script**:
   Execute the script in your Python environment.

This setup should provide a basic yet functional voice assistant that can be further enhanced with additional features and improved NLP capabilities.
