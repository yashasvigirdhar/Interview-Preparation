
Some important points in Design round



* Coming up with the use cases by yourself. You are given only an abstract problem/product at the start. By use cases, I mean all the possible scenarios in which the user will interact with the app. This is the requirements gathering part. Very important to be on the same page with your interviewer before proceeding with the next steps.
*   What all screens you’d have and interactions between them for each use case.
*   What are the server apis you’ll need and when do you call those apis
    *   You might need server push functionality to serve use cases where app is killed.
    *   If possible, speak a bit about error cases in all use cases. Not necessarily deep dive into it but mention it so that the interviewer knows you are aware of these cases.
*   Think of caching too. 
    *   What all be cached
    *   How will you cache it
        *   Format
        *   Storage type
    *   In what way this cache will be consumed.
    *   How this cache is updated
    *   How do you solve the problem for stale cache
*   Is there any api where you can optimize the network payload.
    *   If fetching a list of items, subsequent calls can only fetch the diff from the last version, not the complete list.
*   Handling adverse conditions such as bad network connection, app killed in low memory situations.
    *   You might want to provide offline UX experience in case of network issues OR block the user there itself.
    *   In case of low memory situation, you might want to persist the app state so you don’t lose it.
*   Is there anything which might drain battery. If yes, how do you optimize?
    *   Something which requires polling will drain the battery too.
*   After we are done with high level architecture, low level architecture of the codebase.
    *   How will the layers look like (for eg in MVVM, what is M, V and VM)
    *   How are you persisting data
    *   How are you making the network calls
    *   How are you updating UI with new data.
    *   How are you handling user input.
