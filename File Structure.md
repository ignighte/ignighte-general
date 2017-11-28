## Ignighte : Interactive Playlist for a Party

## File Structure

---

#### 

- [ ] #### 📁 account (All pages pertaining to user account)

  - [x] :page_with_curl:register : register a new user
    - [ ] if exist, error message
    - [ ] write to DB (Post)
  - [ ] :page_with_curl:log in  : log in a existing user 
    - [ ] if not, error message

    - [ ] read from DB

          ​

- [ ] #### 📁 home (All pages concerning home and landing page)

      - [x] :page_with_curl:home-page : Initial page without login

            - [x] Register router
            - [x] Login router
            - [x] Create Playlist router
                  - [ ] Only create public with default time 6 hr
            - [ ] View Playlist router

      - [ ] :page_with_curl:landing-page : Initial page when logged in

            - [ ] View Playlist router
            - [ ] Create Playlist router
                  - [ ] Have option - private and time
            - [ ] Manage Playlist router
            - [ ] Log Out router

            ​

- [ ] #### 📁 page (Mostly Deprecated -> Use video for crossouts)

      - [ ] ~~:page_with_curl:add-playlist (creating a new playlist -> use Create Playlist)~~

      - [ ] ~~:page_with_curl:add-video (adding a video -> integrate with search-video)~~

      - [ ] ~~:page_with_curl:search-song (search for a video -> use search-video)~~

      - [ ] ~~:page_with_curl:view-video (play the video -> use video-player)~~

      - [ ] :page_with_curl:view-playlist (View list of playlists)

            - [ ] requires connection to db for entire list of playlists

            ​

- [ ] #### 📁 video (All pages pertaining to video and playlist)

  - [ ] :page_with_curl:Create Playlist : Create a new playlist 
    - [x] Have a search for videos built in
    - [x] have add button for adding videos
    - [ ] be able to choose private vs public
    - [ ] Autogenerate Passcode
    - [ ] Have duration (auto set at 6 hours, can change)
    - [ ] Need to add "isActive" boolean
  - [ ] :page_with_curl:Manage Playlist : Alter a existing playlist
    - [ ] Drag and move playlist order
    - [x] add and delete songs (Search built in, x button for delete)
    - [ ] Extend a playlist duration
    - [ ] Share my playlist function -> On SNS
  - [ ] :page_with_curl:Delete Playlist : Delete a playlist
    - [ ] Delete Playlist and set the duration = 0, and therefore change the isActive boolean to False
  - [ ] :page_with_curl:Search Video : In Browser Search Function for Youtube parsing
    - [x] display the search function
    - [x] Add Video Button
  - [ ] :page_with_curl:Video Player : player functionality in app
    - [x] play/pause : Be able stop and play using my buttons
    - [x] **prev/next : Traverse Playlist**
    - [x] repeat/shuffle
    - [ ] ~~player size setting~~ -> Deprecated for time being
    - [ ] ~~Initially minimized~~ -> Deprecated for time being
  - [x] :page_with_curl:Search Result : Display results from the search
    - [x] Organize by top searches with scroll bar
  - [ ] :page_with_curl:View Playlist: Simply play the music
        - [ ] My Playlist (all that's mine)

        - [ ] Accessible Playlist (ones you have passcode to + myplaylist)

        - [ ] public playlist

              ​

- [ ] #### 📁 model : Classes Exporting Single Model

  - [x] :page_with_curl:user : A single registered User
    - [x] Has username
    - [x] Has email
    - [x] Has password

  - [ ] :page_with_curl:playlist : A single playlist 

        - [ ] You don't have to be a user to create a playlist
        - [ ] Only a user can create private playlist
        - [ ] Has a passcode
        - [ ] Has Expiration Date
        - [ ] Has isActive
        - [ ] Has isPrivate

  - [x] :page_with_curl:api-key : YOUTUBE_API_KEY

        ​

- [ ] #### 📁 service (Classes Handling Functions)

      - [ ] :page_with_curl:authentication
            - [ ] Register
            - [ ] Verify
            - [ ] Session
      - [x] :page_with_curl:youtube interaction
      - [ ] :page_with_curl:Mock API : Stand Alone Service for GUI