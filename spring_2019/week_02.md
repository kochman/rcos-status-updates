## This week

I didn't work on Hazel Heaters because I got distracted by Shuttle Tracker. Seems to be a theme of my time in RCOS...

I dug into how [Go's new modules](https://github.com/golang/go/wiki/Modules) work and I opened a PR to turn Shuttle Tracker into a Go module ([#198](https://github.com/wtg/shuttletracker/pull/198)). I discussed some of the motivations for doing this in a comment on that PR, but the biggest is that it should be much easier for people to get working on Shuttle Tracker if they're new to Go, since they won't have to figure out what a GOPATH is or figure out how to change their environment variables. 

Then got to work on Shuttle Tracker Fusion, which aims to augment the data we receive from the GPS trackers mounted on the shuttles with geolocation data from people who are using the Shuttle Tracker. The first step is a PR ([#200](https://github.com/wtg/shuttletracker/pull/200)) that gathers the geolocation data so we can analyze it and see if Fusion is even feasible. The PR does several things: adds a WebSocket server for receiving client geolocation updates, has clients initiate connections to that server and push their geolocation updates, and also discloses this information gathering in Shuttle Tracker's privacy policy.

## Next week

After #200 gets merged, the next step is to see if the "tracks" (lists of client positions) can be useful for augmenting the GPS data. It's difficult to test this without real client data. If there's something to work with, then the step after that will be figuring out how to combine the client and GPS data for presentation on the map. 

## Blockers

Waiting on those PRs to get merged or kicked back to me for changes.
