# Class 12 - CRUD
Status Codes Based on REST Messages
# 1. In your own words, describe what each group of status code represents
100’s = these provide information, usually that the server has received the request and will try to fulfill it
200’s = these mean the request was successfully received (not necessarily that the server will process the request)
300’s = the thing the client asked for isn't available on this server anymore and the client needs to make a new request elsewhere
400’s = the client has made an error in its request, like a wrong URI or incorrect authentication
500’s = these are server errors - either the server is down, or the request caused an error on the server
# 2. What is a status code 202?
If a request is processed asynchronously, a 202 status code means that the request has been received successfully but has not yet been processed (and might throw an error later).

# 3. What is a status code 308?
The resource has been permanently moved to another URL and the client should use that one instead.

# 4. What code would you use if an update didn’t return data to a client?
Code 204

# 5. What code would you use if a resource used to exist but no longer does?
204 (or 202 first if the request is processed asynchronously)

# 6. What is the ‘Forbidden’ status code?
403

# Build a REST API
# 1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
So that the local and deployed versions of the app can use different values for the path.

# 2. What is middleware?
# 3. What does app.use(express.json()) do?
Allows the server to accept json requests and puts the data in the request body.

# 4. What does the /:id mean in a route?
It gives us access to whatever gets passed in, which can then be used as variables.

# 5. What is the difference between PUT and PATCH?
PUT would update the entire record, while PATCH would only update the parts that have changed.

# 6. How do you make a default value in a schema?
Add the default property using the "default" key.

# 7. What does a 500 error status code mean?
The request was received correctly, but there's an error in the server.

# 8. What is the difference between a status 200 and a status 201?
201 is a more specific version of 200, and tells the client that something was created.

## Things I want to know more about
All the different server creation/management/search tools and terms are blending together - I'd like to have a better handle on what each thing is and how to use it.