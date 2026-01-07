# Dev Days 2026 Proposal

# Learning Bass with ML Stem Splitters

WIP Title

# Outline

## Questions

- What is a stem?
    - From Wikipedia:
        > In audio production, a stem is a discrete or grouped collection of audio sources mixed together, usually by one person, to be dealt with downstream as one unit. A single stem may be delivered in mono, stereo, or in multiple tracks for surround sound.
    - Fun fact: the ter "stem" comes from the film industry. It predates multi-track recording
- What is a stem splitter?
    - A stem splitter is a tool that takes a mixed audio track and separates the track into its individual tracks (or 'stems')
    - The most common form of stem splitting is separating the vocals from the instrumental
- Why use a stem splitter?
    - Based on the most common use, you probably guessed that the most common use is for karaoke
    - Another popular use is sampling, particularly drums
        - Other instruments like guitar, bass, & synths are not uncommon
    - DJs, producers, & musicians use stem separators for a capellas, remixes, and mashups
        - Mention stem splitting goes back a long time
        - Would love to go on, but this is meant to be about ML
- What do I use stem splitters for?
    - I use these tools to learn songs by ear, primarily for bass guitar.
        - Some songs have prominent bass lines that are easy to pick out
        - Other songs are mixed in such a way that the bass is buried, quiet, or difficult to pick out
            - Example: Densely mixed genres like grunge, shoegaze, & psychedelia
- How is this Dev Days related?
    - Machine Learning!
        - With the rise of machine learning, many free & paid tools for stem separation have emerged.
- What is Moises?
    - They describe themselves as:
        > Moises is the AI-powered suite for music makers of all styles to learn, practice, produce, and collaborate. Created by musicians, for musicians.
    - I was introduced to it by my previous bass teacher
        - There are other tools, but this is the one I was introduced to & it gets the job done
- What are the features of Moises I use?
    - Main feature: Stem separation
        - Free tier allows for:
            - 4 Tracks: Vocals, Drums, Bass, Other
            - 4 songs per month
            - 5 minute limit per song
            - *Note that term Free tier!
    - Tempo detection
        - While not always accurate, having a ballpark allows for the next feature to work
    - Tempo manipulation
        - Primarily for slowing down songs
    - Key detection
        - Useful for knowing what scales make sense in the key
    - Transposition
        - Use for changing the key of the tune
            - Only really use this if I don't want to change the tuning of my bass
                - Ex: Dead Souls by Joy Division has all strings tuned down a half step.
- Why abandon Moises?
    - Though they advertise having apps for every platform, they achieve this by being yet another electron app
    - Being an electron app alone isn't a deal breaker, but it does require a constant internet connection
    - The free tier is almost enough for me, but the 5 minute time limit is an issue for a lot of songs I'd like to learn
    - Additionally, being a software as a service, there is no guarantee that the service will be around in the future
    - The platform could also fall victim to enshittification, like **many** web apps before it
- Why do I want to recreate a stem splitter locally?
    - I don't want to rely on an always online service
    - Many of the "AI" music tools on the market are front-ends for free models from Google & Facebook
    - I daily drive an M1 MacBook Pro & have a gaming PC, therefore I *should* have plenty of GPU horsepower to run these models locally
- What tool will I use for stem splitting?
    - Stemroller!
- Why Stemroller?
    - The tool is free & open source
    - Stemroller runs the demucs model on your local machine
        - Allows you to choose between software & hardware acceleration
        - Also gives you the option to choose between three different separation types:
            - 4 tracks fast (voice, drums, bass, other)
            - 4 tracks slow (voice, drums, bass, other)
            - 6 tracks (experimental) (voice, drums, bass, piano, guitar, other)
    - Allows the user to set what file format they want the stems in (uses .WAV by default)
    - Includes yt-dlp for downloading songs from YouTube
        - Likely useful for many, but I am comfortable running yt-dlp on the CLI
- What tools will I use?
    - GarageBand
        - Place to drop the tracks, set key & tempo, & record my bass
    - [SongBPM](https://songbpm.com/)
        - Gets the tempo & key of the song, which I can then set in GarageBand

# Script

word