`Response: {"error":"Invalid header value b'Bearer luma-a9b75194-ad81-4694-854e-aae9c581e830-249ba154-a4dc-4f25-9767-884d2bf37774\\n'","status":500}`

I was getting this error when trying to call my google cloud function. You can see at the end of the API key that there is a new line character. 
**Bug:** I accidentally added a new line to the bearer token, so it was invalid