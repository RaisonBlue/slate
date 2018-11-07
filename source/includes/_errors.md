# Errors

The Jitips API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid.
401 | Unauthorized -- Your API key is wrong.
403 | Forbidden -- Not enough privileges.
404 | Not Found -- Requested resource could not be found.
405 | Method Not Allowed -- You tried to access a resource with an invalid method.
406 | Not Acceptable -- You requested a format that isn't json.
410 | Gone -- The resource requested has been removed from our servers.
418 | I'm a teapot.
429 | Too Many Requests -- You're requesting too many resources! Slow down!
500 | Internal Server Error -- We had a problem with our server. Sorry, gonna fix it! Try again later.
501 | Not Implemented Yet -- We haven't dev that part yet, sorry about that.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
