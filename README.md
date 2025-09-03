## Please briefly describe what your app does.

Mayflower is an end-to-end solution for job searching, resume development and mock interview prep. Our app caters to single parents, low income area inhabitants, immigrants, high school students and anyone else looking for work that needs instant guidance for resumes and interviews.

After signing up, users can browse popular and nearby jobs sourced from the JSearch API, which often includes the job description, reviews, salary and links to apply. We have created a 15-question onboarding quiz to make proper recommendations based on interest, demographic and past employment history.

Our OpenAI-powered resume builder creates CVs in real time simply by having a conservation. Applications are rejected because they fail to stand out. Through research such as the 7 Second CV (James Reed) and feedback from Nina Chung, a developer at Citi, we have given our users the bleeding edge through unique descriptions informed by the job description, most successful phrases for the profession, ATS-friendly resume templates and easy export to email or print.

Using OpenAI’s GPT-3.5 and Whisper for speech to text, and Eleven Labs for text to speech, we provide an immersive interview prep experience with a 3D model taking on the role of interviewer. It facilitates conversation by listening to the user speak, generating a response and speaking in a natural voice, with interview content once again informed from the job description. Of course, so much of an interview is unspoken, unfolding as body language and nonverbal communication. A Tensorflow model, trained on a public dataset of 15k images, performs facial recognition and emotion detection to keep the user aware of how they are being perceived.

## What inspired you to create this app? *

Ethan’s mother, May, had been experiencing firsthand the difficulty of assimilating into the workforce of a new country. Our app’s name serves as a tribute to her and the app itself to the millions out there who have ever struggled with finding employment.

We aim to bridge the gap in representation and resources—the so-called “networking gap”—by helping people who can’t write professional resumes or receive targeted interview prep. Current job apps like Linkedin and Glassdoor largely overlook this demographic and fail to provide instant help, promoting networking only for those with polished CVs and perfect interview skills.

We came across the job preparation app Monster through our friends and family who alleged that it accomplished much of what we were trying to do. We discovered, however, that the articles they provide can be difficult to synthesize, an inefficient solution in light of the powerful technology available today. Technology can truly recover from the crevice those low income area inhabitants, immigrants, high school students, single parents, and returnees to the workforce who might have slipped in. Overall, our app wants to simplify the job application process by catering to those who have less experience in the job market through instant guidance using AI.

What technical difficulties did you face programming your app? *

Creating Mayflower was truly a journey for us, and we are proud to have turned our dreams into a tangible reality that could even make it onto app stores one day. One challenge was simply becoming acclimated to all the new technologies. We wanted to incorporate the power of generative AI while remaining synchronized with the employment zeitgeist, which led us to think about creating immersive experiences through chatbots and 3D models.

Because we don’t have access to expensive developer programs like Apple Developer and because of our emphasis on cross-platform compatibility, we built Mayflower in React Native, using Expo Go for development. Expo Go makes it easy to build, test and tweak during the design process, but it prevents us from using some native device capabilities such as speech to text or face detection. We implemented a workaround by leveraging open-source or cloud APIs such as OpenAI’s Whisper model, which turns audio recordings of the user’s interview responses into text that GPT-3.5 can parse. 

We had a lot of fun working with interactive experiences and 3D models, but it was difficult getting multiple platforms to cooperate. For instance, the Three.js loader left our interviewer naked by failing to load textures, a problem that other users of the framework seem to have had as well. We successfully implemented a workaround by importing the textures separately and sharing our findings on our GitHub, hopefully alleviating the headache of anyone who runs into the same problem in the future!

Finally, we had difficulty prompt-engineering the resume builder. We instruct the AI to parse the user’s responses and return a JSON object with any new information to update the HTML resume template, something which was notoriously difficult to perfect. The AI was often picky and delivered the correct response sometimes while completely ignoring the directions other times. Through continuous tweaking, we were able to achieve an acceptable level of consistency by testing the builder numerous times. 

On a similar note, we often ran into rate limit issues that blocked us from using the API too much due to us being on the free tier. We hope to take our app to the next level and generate a revenue stream to fix this for good!

## What improvements would you make if you were to create a 2.0 version of your app? *

If we were to make a 2.0 version of our app, first and foremost, we would like to create a more advanced AI which would be trained even more to become more accurate by training it with many more images. This way, the AI would be able to hold a genuine conversation which would be far superior to the simplistic prefaces it provides in response to statements the user makes in the interview section. 
