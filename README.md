AZURE AI LANGUAGE TEXT ANALYTICS APPLICATION

𝗢𝘃𝗲𝗿𝘃𝗶𝗲𝘄
This project demonstrates how to use the Azure AI Language service for text analytics. It includes functionality for language detection, sentiment analysis, key phrase extraction, entity recognition, and linked entity recognition from text documents, such as hotel reviews.

𝗙𝗲𝗮𝘁𝘂𝗿𝗲𝘀
• Language Detection: Identify the language of the input text.
• Sentiment Analysis: Classify the sentiment of the text as positive, neutral, or negative.
• Key Phrase Extraction: Extract key phrases that represent the main topics discussed in the text.
• Entity Recognition: Identify named entities such as people, places, and organizations in the text.
• Linked Entity Recognition: Detect entities with links to external data sources like Wikipedia.

𝗣𝗿𝗲𝗿𝗲𝗾𝘂𝗶𝘀𝗶𝘁𝗲𝘀
• An Azure subscription with access to the Azure AI Language service.
• Visual Studio Code installed on your machine.
• .NET SDK (for C#) or Python (for Python implementation) installed.

𝗚𝗲𝘁𝘁𝗶𝗻𝗴 𝗦𝘁𝗮𝗿𝘁𝗲𝗱
1. Provision Azure AI Language Resource
   • Log into the Azure portal and create an Azure AI Language resource.
   • Take note of the endpoint and keys provided after provisioning.
2. Clone the Repository
   Clone the repository to your local machine:git clone https://github.com/MicrosoftLearning/mslearn-ai-language
3. Set Up Your Development Environment
   • Open the cloned repository in Visual Studio Code.
   • Install the necessary packages:
   pip install azure-ai-textanalytics==5.3.0
   pip install python-dotenv
4. Configure the Application
   Update the configuration file with your Azure AI Language resource's endpoint and key:
   For Python: Edit .env
5. Run the Application
6. Observe the Output
    The application will analyze each review file and display the detected language, sentiment, key phrases, entities, and linked entities.


Code Explanation
The code is organized into the following sections:

Language Detection: Uses the Azure AI Language client to detect the language of the text.
Sentiment Analysis: Analyzes the sentiment of the text.
Key Phrase Extraction: Extracts key phrases from the text.
Entity Recognition: Identifies entities within the text.
Linked Entity Recognition: Recognizes entities with links to external data sources.

Example:
review3.txt

Good location and helpful staff, but on a busy road.
The Lombard Hotel, San Francisco, USA
8/16/2018
We stayed here in August after reading reviews. We were very pleased with location, just behind Chestnut Street, a cosmopolitan and trendy area with plenty of restaurants to choose from. The
Marina district was lovely to wander through, very interesting houses. Make sure to walk to the San Francisco Museum of Fine Arts and the Marina to get a good view of Golden Gate bridge and the city. On a bus route and easy to get into centre. Rooms were clean with plenty of room and staff were friendly and helpful. The only down side was the noise from Lombard Street so ask to have a room furthest away from traffic noise.

Language: English

Sentiment: mixed

Key Phrases:
        Golden Gate bridge
        The Lombard Hotel
        The Marina district
        San Francisco Museum
        Lombard Street
        busy road
        Chestnut Street
        trendy area
        interesting houses
        Fine Arts
        good view
        bus route
        down side
        Good location
        helpful staff
        traffic noise
        USA
        We
        August
        reviews
        cosmopolitan
        plenty
        restaurants
        city
        centre
        Rooms

Entities
        staff (PersonType)
        road (Location)
        Lombard Hotel (Location)
        San Francisco (Location)
        USA (Location)
        8/16/2018 (DateTime)
        August (DateTime)
        Chestnut Street (Location)
        restaurants (Location)
        Marina district (Location)
        houses (Location)
        San Francisco Museum of Fine Arts (Location)
        Marina (Location)
        Golden Gate bridge (Location)
        city (Location)
        centre (Location)
        Rooms (Location)
        staff (PersonType)
        Lombard Street (Address)
        room (Location)

Links
        Lombardy (https://en.wikipedia.org/wiki/Lombardy)
        Hotel (https://en.wikipedia.org/wiki/Hotel)
        San Francisco (https://en.wikipedia.org/wiki/San_Francisco)
        Chestnut Street (Philadelphia) (https://en.wikipedia.org/wiki/Chestnut_Street_(Philadelphia))  
        Marina District, San Francisco (https://en.wikipedia.org/wiki/Marina_District,_San_Francisco)  
        Museum of Fine Arts, Boston (https://en.wikipedia.org/wiki/Museum_of_Fine_Arts,_Boston)        
        Golden Gate Bridge (https://en.wikipedia.org/wiki/Golden_Gate_Bridge)
        Room (https://en.wikipedia.org/wiki/Room)
        Lombard Street (San Francisco) (https://en.wikipedia.org/wiki/Lombard_Street_(San_Francisco))  


