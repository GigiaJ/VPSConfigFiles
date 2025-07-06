This is more or less a bunch of containers that should really be in a deployed alongside IaC cluster definition at this point... But we'll just pay the higher bill for now. Pulumi is fairly succinct if looking for recommendations.


Nextcloud AIO (the main setup piece) REQUIRES the IP to be used to connect to the main container to actually run the other containers. It will not connect through the domain.

Any other notes I'll add here, but generally after setting the .env up based on the sample.env you can run
`docker compose up -d` and you're golden. It is resource heavy though (which is why it should be broken up).