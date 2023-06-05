# InteRactiVized

![Interactiviz_Concept_Map](https://github.com/varun-spectre/readme_facepong/assets/31825973/9bd817fb-390d-4a86-8727-14cdb2924283)



## Project Description:

The present project, developed by the College of Health Solutions at Arizona State University, introduces an open-source platform tailored for researchers to discern the innate responses of users through an interactive 3D face pong game. This platform offers researchers the opportunity to explore diverse parameters and configurations that align with their particular research objectives. The platform incorporates the following technologies:

- ThreeJS: A framework utilized for constructing the game, facilitating a robust and interactive user experience.
- Media Pipe: A high-speed face detection system that enables rapid identification of facial features crucial for user engagement.
- MongoDB: An advanced database management system employed to securely store pertinent game information for further analysis and evaluation.
- Hosted on AWS server via Node JS: The platform is deployed on an Amazon Web Services server and employs Node.js for efficient and scalable server-side execution.

By amalgamating these technologies, the platform enables researchers to examine user reactions within a controlled environment, offering valuable insights for various research applications.

https://github.com/varun-spectre/readme_facepong/assets/31825973/69d57563-4616-4605-bf23-43ef5982171a


## Platform Description:

The platform enables researchers to modify various parameters within the game itself, such as game sounds, randomness, and difficulty levels. These adjustable parameters are set prior to launching the game on a single device. Users interact with the game directly on the same device, allowing researchers to capture user behavior data in real-time. The collected data can then be analyzed and visualized to derive meaningful insights about user engagement and responses.

### Game Details:

The 3D interactive pong game encompasses a game canvas as the primary playing field, consisting of a single ball and two paddles: a CPU paddle and a Player Paddle. The player's paddle is controlled by the movement of their nose, tracked via a webcam. The game operates on an event-based system, wherein the ball initiates from the CPU paddle, propelled in a randomized direction towards the player's paddle. The event concludes when the player successfully hits the ball or fails to do so.

#### Visual Aspects:

To enhance the visual experience, the game incorporates contrasting colors and shading techniques for each game object. The ball's position is dynamically updated by considering its x and y directions, along with the respective speeds in each direction, ensuring smooth and continuous movements throughout the game.

#### Audio Components:

In collaboration with The Sidney Poitier New American Film School at ASU, a variety of audio files have been created and seamlessly integrated into the game. These audio files simulate the sounds of the ball approaching and striking the paddles, generating distinct audio cues for left and right paddle interactions.

#### Game Modes:

The game offers distinct modes to cater to different user preferences:

1. Audio Visual Mode:
   In this mode, users are presented with the full game canvas, allowing them to visually observe the game elements while simultaneously experiencing simulated audio feedback. The audio cues are synchronized with the position and direction of the ball, enhancing the immersive gameplay experience.
2. Visual Mode:
   Designed for users who prefer a visual-centric experience, this mode provides the complete game canvas without any accompanying audio. Users can fully engage with the visual aspects of the game, focusing on strategic gameplay and visual cues.

3. Audio Mode:
   This mode caters to users who prefer an audio-oriented experience. Users will not be able to see the ball, while audio feedback is generated based on the ball's position and direction. This mode emphasizes auditory perception and allows users to rely on audio cues to make gameplay decisions.

By offering these distinct game modes, the platform accommodates individual preferences, providing users with customizable experiences tailored to their desired audio-visual engagement levels.

## Visualizing Game Data:

To facilitate data analysis and interpretation, the platform includes a notebook specifically designed for researchers. This notebook offers interactive visualization capabilities, allowing researchers to explore and analyze the collected game data.

Researchers can filter the data based on user ID and specify a desired time frame to focus on specific subsets of the data. By leveraging the visualization capabilities of Plotly, researchers can generate dynamic and interactive animations that present the game data in a visually engaging manner. These animations provide a comprehensive view of user behavior and interactions throughout the gameplay session. 


https://github.com/varun-spectre/readme_facepong/assets/31825973/f6265704-580a-41ef-9a63-943cb7e04e1d


The interactive nature of the visualization allows researchers to delve deeper into the data, identify patterns, and gain valuable insights into user behavior and performance. By combining the power of data filtering, time frame selection, and Plotly animations, the platform empowers researchers to effectively analyze and interpret the game data collected during the research study.

## Explanation of Platform Parameters:

1. Impact Audio:

   - This parameter requires a public Amazon S3 bucket object link to an audio file.
   - The specified audio will play when the ball makes contact with the player paddle.
   - By default, the platform utilizes audio provided by The Sidney Poitier New American Film School at ASU, but researchers have the flexibility to customize this sound.

2. Looming Audio:

   - Similar to the Impact Audio parameter, this parameter requires a public Amazon S3 bucket object link to an audio file.
   - The designated audio will play when the ball is launched and continues until the ball makes contact with any surface, such as the game table sides or the player paddle.
   - The default audio used in this parameter is also provided by The Sidney Poitier New American Film School at ASU, but researchers can replace it with their own audio selection.

3. Difficulty Parameter:

   - The Difficulty Parameter allows researchers to adjust the opponent paddle's movement based on a parameter value ranging from 0 to 1.
   - A value of 1 signifies that the opponent paddle will never miss hitting the ball, while a value of 0 means that the opponent paddle's position will not update, resulting in missed hits.
   - By default, the parameter is set to 0.2, providing a moderate level of difficulty.

4. Randomness Parameter:
   - The Randomness Parameter influences the ball's bounce behavior when it hits the left or right side of the game board.
   - The parameter value determines the level of randomness introduced to the bounce, making it unpredictable.
   - A value of 0 indicates no randomness, while a value of 1 introduces maximum randomness to the game.
   - Researchers can utilize this parameter to assess users' natural reactions to unexpected events.
   - The default value is set to 0, meaning no randomness is incorporated into the game.

By allowing researchers to adjust these parameters, the platform offers flexibility and customization, enabling the study of user responses under various audio, difficulty, and randomness settings.

## Data Privacy:

### Game Data Collection:

As part of the game data collection process, the platform records the following information for each frame:

1. Ball position
2. Opponent paddle position
3. User paddle position

### Data Privacy Measures:

To ensure data privacy, the platform adheres to strict data protection measures. The collected game data is treated with utmost confidentiality and is securely stored. Access to the data is limited to authorized personnel involved in the research study.

Additionally, any personally identifiable information (PII) of the users is not collected or stored as part of the game data. The focus is solely on capturing the positional data of the ball and paddles to analyze user behavior and interactions within the game.

### Compliance with Regulations:

It is important to note that the platform follows all relevant data privacy regulations and guidelines to safeguard the privacy and confidentiality of the collected data. The researchers are responsible for complying with ethical considerations and obtaining informed consent from participants prior to using the platform for data collection.

By prioritizing data privacy and implementing appropriate security measures, the platform ensures the protection and anonymity of users' data throughout the research process.

## Testing Locally:

To test the game locally, follow the steps below:

1. Clone the repository: Clone the repository containing the game files to your local machine.

2. Configure the server.js file: Open the server.js file and ensure that you have provided the appropriate MongoDB link to store the game information. This link should point to your own MongoDB instance.

3. Install dependencies: Install any required dependencies by running the necessary commands specified in the repository's documentation or README file. This may involve using package managers like npm or yarn.

4. Run the server: Execute the server.js file to start the game server. This will allow the game to be accessed locally on your machine.

5. Verify system requirements: Ensure that your local machine meets the minimum system requirements to run the game smoothly. The mentioned specifications, including 16 GB RAM, an i7 10th generation processor, and an NVIDIA GTX 1660 Ti 6GB GPU, were used for testing purposes and should provide satisfactory performance. However, it's important to note that the game may still run on machines with lower specifications, albeit potentially at a lower frame rate.

6. Test gameplay: Access the game on your local machine through a web browser or any specified local URL. Interact with the game and verify that it functions as intended.

During testing, it was observed that the game achieved an average frame rate of around 100 frames per second on the specified testing machine. Your own machine's performance may vary based on its specifications.

By following these steps, you can successfully test the game locally and ensure its functionality before deployment or further usage.

## Future Work:

There are several potential enhancements and extensions that can be considered for future development of the game:

1. Three-dimensional Gameplay:

   - Currently, the game is played in a two-dimensional space with mapping of the player's nose position to the x and y coordinates.
   - In future iterations, the game can be expanded to incorporate three dimensions, enabling a more immersive gaming experience.
   - For example, a 3D tennis game where players can move and interact in three-dimensional space.

2. Multiplayer Support:

   - Enhancing the game to support multiplayer functionality would enable players to compete against each other.
   - This could be implemented as either local multiplayer, allowing multiple players on the same device to play together, or online multiplayer, where players can compete remotely over the internet.
   - Multiplayer support adds an element of competitiveness and social interaction to the game.

3. Integration with Machine Learning Libraries:
   - Researchers can benefit from the ability to integrate their own machine learning libraries into the game platform.
   - This would allow for advanced analysis of the game data, enabling researchers to apply machine learning algorithms and techniques to gain deeper insights into user behavior and performance.
   - Integration with machine learning libraries would provide researchers with a powerful toolset for analyzing and interpreting the collected data.

By incorporating these future developments, the game can be expanded in terms of gameplay dimensions, multiplayer engagement, and integration with machine learning capabilities. These enhancements would provide researchers and players with a more comprehensive and dynamic gaming experience while enabling advanced analysis and research possibilities.
