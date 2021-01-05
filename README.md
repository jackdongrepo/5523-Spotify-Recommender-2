# Spotify Recommender System

Install requirements such as spotipy

run preprocessing notebook, skipping the cells that it says takes forever. This is because we already ran and saved that info for you to make it faster

Run the notebook for the corresponding model you want to recommend based on. This will do hyperparameter optimization and create graphs for analysis

Note you must have spotify premium to use their api for this.

Go to spotify for developers and create a new app, name it whatever you want

Click edit settings on your new app. Add this url http://example.com as a redirect url

Create 3 environment variables like below, fill them in with your corresponding app client id and client secret. Leave the SPOTIPY_REDIRECT_URI as is.

```sh
export SPOTIPY_CLIENT_ID='your-spotify-client-id'
export SPOTIPY_CLIENT_SECRET='your-spotify-client-secret'
export SPOTIPY_REDIRECT_URI='http://example.com'
```

The recommender is in a notebook. You can use the recommend_playlist function to automatically upload a recommended playlist of music to your spotify. It is setup so you can run any model that you want. We have kmeans in it right now. You will have to paste in the proper parameters into this function to use it that are specific to your spotify profile. They are all explained in the docstring of the recommender. Note that you can get your playlist_uri by right clicking a playlist in spotify, going to share, then to copy playlist uri. Be sure to not use a album and to use a playlist.

When you run the recommender it is going to open some windows. When this happens, accept the permissions, and it will perform a redirect to a page. Now copy the url of where you are redirected and the notebook will be waiting for your input. Paste this url into the text box of the notebook. Repeate this each time it asks.
 
Now at the end you should have a new playlist uploaded into your spotify based on the model you picked.

