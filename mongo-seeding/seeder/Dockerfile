FROM mongo:5.0
 # Will be set through Environment Files
 ARG DATABASE_URI
 ARG USERNAME
 ARG PASSWORD

 ENV DATABASE_URI ${DATABASE_URI}
 ENV USERNAME ${USERNAME}
 ENV PASSWORD ${PASSWORD}

 COPY addresses.json /addresses.json

 CMD mongoimport --username ${USERNAME} --password ${PASSWORD} --uri ${DATABASE_URI} --collection addresses --drop --file /addresses.json