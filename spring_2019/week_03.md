I worked on a feature called "bus button" for Shuttle Tracker. When enabled, it allows users to send bus emojis to other users. They show up on the map at the user's current location. The infrastructure to do this was somewhat extensive:

- There is a WebSocket connection from clients to the server. This allows Shuttle Tracker to push bus buttons down to clients whenever another client sends one. In the future, we will use this to push vehicle locations and ETAs to clients in real-time so that they don't have to poll endpoints over HTTP.
- The server keeps track of clients and associates them with specific topics that they should be notified of.
- There is a debug page that authenticated administrators can view to see how many Fusion/WebSocket clients are currently connected, when the last message was received, and what the user agent is.

