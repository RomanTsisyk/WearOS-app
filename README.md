## PRD for Motivational Application on Wear OS

Developing a motivational app for Wear OS watches that uses a database of motivational words stored in JSON format on GitHub. The app will send users motivational messages hourly, with the ability to set periods when messages should not be sent.

### Problem Statement
Users need continual motivational encouragement throughout the day, but existing solutions require active engagement or are not integrated with their daily devices like watches.

### Objectives
- **Business Objectives**: Engage users interested in self-improvement through regular motivational messages.
- **User Objectives**: Receive regular motivational reminders without needing to interact with a phone.

### Non-Objectives
- Sending types of messages other than motivational.
- Integration with platforms other than Wear OS.

### User Stories
1. As a user, I want to receive motivational messages every hour to keep feeling motivated.
2. As a user, I want to be able to set "quiet hours" so I don’t receive messages at inconvenient times.

### User Experience
1. **Installation and Setup**: Users download the app from the Google Play Store. During the initial setup, the user configures times they do not wish to receive messages.
2. **Usage**: The app runs in the background, pulling data from GitHub and displaying messages at the designated times.
3. **Updates**: Upon detection of a new JSON version, the app automatically updates the local database with new entries.

### JSON Data Structure
- **GitHub Repository**: Motivational words are stored in JSON format and hosted in a public GitHub repository.
- **Versioning**: JSON files are versioned, allowing the app to retrieve updates automatically without user intervention.
  - Example structure:
    ```json
    {
      "version": "1",
      "messages": ["Word1", "Word2", ...]
    }
    ```
- **Database Updates**: When a new JSON version is detected, the app automatically adds new messages to the local database.

### Success Metrics
- **User Engagement**: Percentage of users who regularly use the app.
- **Message Count**: Average number of messages viewed by users per day.
- **User Satisfaction**: User satisfaction rating through surveys and feedback.

### Technical Considerations
- **GitHub API**: Use of GitHub API to access JSON files on GitHub.
- **Local Database**: Use of SQLite to store data on the device.
- **Optimization for Wear OS**: Special design and development requirements for wearable devices, including resource minimization and interface adaptation for small screens.
- **Diagram illustrating the basic architecture**:
- 
  <img width="422" alt="image" src="https://github.com/RomanTsisyk/WearOS-app/assets/25310063/3cd9f0d9-88cf-4cac-b00e-30fb03de1328">


### Milestones
1. **Prototype Development**: Creating a basic version of the app with core functionality (3 weeks).
2. **GitHub Integration**: Implementing functionality for downloading and updating data from GitHub (3 weeks).
3. **Testing and Implementation**: Conducting comprehensive testing and collecting feedback from initial users (3 weeks).
4. **Official Release**: Launching the app on Wear OS (3 weeks).

### The timeline diagram illustrating the development phase

<img width="1778" alt="image" src="https://github.com/RomanTsisyk/WearOS-app/assets/25310063/6e17769c-883b-4649-92fb-321aa691b2fd">
