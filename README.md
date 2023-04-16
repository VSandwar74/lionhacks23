# Near.Social Analytics Dashboard

Check it out at: https://near.social/#/vishakhs.near/widget/social-analytics

### Sentiment Analysis Pie Chart
This project is a simple React component that displays a pie chart representing the sentiment analysis results. 
The pie chart is generated using SVG and the values are fetched from an external API. The component also includes 
a tooltip feature that displays the value when you hover over a segment of the pie chart.

### Top Posters Table
This component shows the most extensive posters on the platform, within the last couple hours and builds upon widgets created by social.near to allow for a "gateway"-type access point on-chain/

## Views:

![Table](https://i.postimg.cc/KKXtJ0y7/Screenshot-2023-04-16-at-3-53-41-PM.png "Screenshot 1")
![VADER-Based Sentiment Analysis](https://i.postimg.cc/Z9rpg6TG/Screenshot-2023-04-16-at-6-29-47-AM.png "Screenshot 2")

## Workflow:

### Off-Chain Chron Job Ran Through .sh file

1. API: https://docs.flipsidecrypto.com/

- Used flipside crypto API to get last 500 posts on near.social
- Converted into a csv file

2. Data processing

- Used Python to clean and process the data and extract any relevant analyses using VaderSentimentAnalyzer (plan to add additional metrics)
- Convert to json file

### On-Chain Widget

3. Personal API: https://github.com/VSandwar74/near-social-api

- Imports json files from local and sends when a get request is called
- Used Hono to build api and hosted on railway.
- More information available in linked repo

4. The Near.Social widget

- Uses fetch hook to get jsons files from the API
- Visualizes the given data
- Uses UserID information as props for pre-built widgets to allow live links and on-chain functionalities

Cred for inspo and models: https://github.com/AUT-Twitter-Analytics/Streamlit-Dashboard

Made by [Vishakh](https://github.com/VSandwar74), [Shreyaas](https://github.com/Shreyaas14), Soham, [David](https://github.com/JackBliss-bit) for LionHacks '23


