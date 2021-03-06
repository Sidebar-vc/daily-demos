# Daily Prebuilt UI demo

This demo highlights [Daily's prebuilt UI](https://www.daily.co/blog/prebuilt-ui/), and how it can be used to embed a video chat widget in a website or app. The demo also illustrates how to use [daily-js methods](https://docs.daily.co/reference#instance-methods) and [events](https://docs.daily.co/reference#events) to build custom interfaces outside of the callframe that control the call.

The demo's custom controls use these Daily methods:

- [`.setLocalVideo()`](https://docs.daily.co/reference#%EF%B8%8F-setlocalvideo)
- [`.setLocalAudio()`](https://docs.daily.co/reference#%EF%B8%8F-setlocalaudio)
- [`.startScreenShare()`](https://docs.daily.co/reference#%EF%B8%8F-startscreenshare)
- [`.stopScreenShare()`](https://docs.daily.co/reference#%EF%B8%8F-stopscreenshare)
- [`.startRecording()`](https://docs.daily.co/reference#%EF%B8%8F-startrecording)
- [`.stopRecording()`](https://docs.daily.co/reference#%EF%B8%8F-stoprecording)
- [`.requestFullscreen()`](https://docs.daily.co/reference#requestfullscreen)
- [`.participants()`](https://docs.daily.co/reference#%EF%B8%8F-participants)
- [`.getNetworkStats()`](https://docs.daily.co/reference#%EF%B8%8F-getnetworkstats)
- [`.setSubscribeToTracksAutomatically()`](https://docs.daily.co/reference#%EF%B8%8F-setsubscribetotracksautomatically)

![Video call takes up the left side of the screen, call controls on the right](./assets/prebuilt-ui-demo.gif)

## Prerequisites

- [Sign up for a Daily account](https://dashboard.daily.co/signup) if you'd like to insert your own URL into the Room URL input field.

## How the demo works

The participant either clicks the "Create demo room" button, triggering a helper function that generates a temporary demo room, or enters their own Daily room URL into the input field.

Once a room has been created, the participant can click "Join call." This button calls the Daily [`.join()`](https://docs.daily.co/reference#%EF%B8%8F-join) method, letting the participant into the call. The app listens for this `meeting-joined` event, and displays the control panel when the event fires. Each button in the panel triggers a corresponding Daily method when clicked.

## Running locally

1. `cd daily-demos`
2. `cd static-demos`
3. `npm run start` or `npm run dev`
4. Then open your browser and go to `localhost:<port>/static-demos/prebuilt-ui-demo/index.html`

## Contributing and feedback

Let us know how experimenting with this demo goes! Reach us any time at `help@daily.co`.

## What's next

This demo shows off the [Daily prebuilt UI](https://www.daily.co/blog/prebuilt-ui/), but it's also possible to build an entirely custom video chat interface using [the Daily call object](https://docs.daily.co/docs/build-a-custom-video-chat-interface). Have a look at our [React tutorial](https://www.daily.co/blog/building-a-custom-video-chat-app-with-react/) to get started.
