# Spotify Connected App

End product of the "Build a Spotify Connected App" newline course

## Go here to view the Live Project

https://spotifyappvf.onrender.com/

## Local Installation & Set Up

1. Register a Spotify App in your [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/) and add `http://localhost:8888/callback` as a Redirect URI in the app settings

2. Create a `.env` file at the root of the project based on `.env.example` and add your unique `CLIENT_ID` and `CLIENT_SECRET` from the Spotify dashboard

3. Ensure [nvm](https://github.com/nvm-sh/nvm) and [npm](https://www.npmjs.com/) are installed globally

4. Install the correct version of Node

    ```shell
    nvm install
    ```

5. Install dependencies

    ```shell
    npm install
    ```

6. Run the React app on <http://localhost:3000> and the Node server on <http://localhost:8888>

    ```shell
    npm start
    ```
       
## Deploying to Render with Git

1. Create a [Render](https://www.render.com/) app

2. Add your render app as a git remote (https://render.com/docs/github)

    ```shell
    heroku git:remote -a your-app-name
    ```

3. Add `http://your-app-name.render.com/callback` as a Redirect URI in your Spotify app's settings

4. In your app's **Environment** tab in the Render App dashboard, add [environmental variables] (https://render.com/docs/configure-environment-variables)

   Based on the values in your `.env` file, the `CLIENT_ID`, `CLIENT_SECRET`, `REDIRECT_URI`, and `FRONTEND_URI` key value pairs. Make sure to replace the `localhost` URLs with your heroku app's URL.

   ```env
   REDIRECT_URI: http://your-app-name.render.com/callback
   FRONTEND_URI: http://your-app-name.render.com
   ```

5. Push to render

    ```shell
    git push render main
    ```
    
Alternatively connect Github to Render using the Web GUI (https://render.com/docs/github)    
