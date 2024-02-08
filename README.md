# ovos-media-plugin-simple

simple plugin for [ovos-media](https://github.com/OpenVoiceOS/ovos-media)

tries to use the best command line utility available to play audio, `sox` is recommended

## Install

`pip install ovos-media-plugin-simple`

## Configuration


```javascript
{
 "media": {

    // keys are the strings defined in "audio_players"
    "preferred_audio_services": ["mplayer", "vlc", "simple"],

    // PlaybackType.AUDIO handlers
    "audio_players": {
        // simple player uses a slave simple instance to handle uris
        "simple": {
            // the plugin name
            "module": "ovos-media-audio-plugin-simple",

            // users may request specific handlers in the utterance
            // using these aliases
            "aliases": ["Simple Player", "Command line"],

            // deactivate a plugin by setting to false
            "active": true
        }
    }
}
```