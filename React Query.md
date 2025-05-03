a powerful library for fetching data and managing state in react applications

useQuery itself is a react hook 
- when component rerenders the use query automatically executes
- React query processes the new network request in the background but caches your old data.
	- What this means: you see the old data that was cached until you get a response with the new data 
- gcTime in react query allows you to clear cache in specified amount of time. how long it will be stored in the cache
- staleTime tells react query how long the cached data is valid. how long until you fetch a new copy



