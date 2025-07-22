This is more or less a bunch of containers that should really be in a deployed alongside IaC cluster definition at this point... But we'll just pay the higher bill for now. Pulumi is fairly succinct if looking for recommendations.


Nextcloud AIO (the main setup piece) REQUIRES the IP to be used to connect to the main container to actually run the other containers. It will not connect through the domain.

Any other notes I'll add here, but generally after setting the .env up based on the sample.env you can run
`docker compose up -d` and you're golden. It is resource heavy though (which is why it should be broken up).


Some details to add, but Cloudflared is useful for allowing us to set up elegant SSH tunnels w/ Cloudflare's proxying so we don't have to expose our server IP. I've been trying to avoid ever having to share that with anyone who doesn't *need* it.

Super Productivity is our productivity tool that allows us to both use task scheduling and the pomodoro technique. The major benefit being that we can leverage our Nextcloud instance via WebDAV to save/sync our details in the same manner we were using Pomofocus. The upside here is that I can self-host and don't need to worry about somewhat intimate personal info being leaked. 