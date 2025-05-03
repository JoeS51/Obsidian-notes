
**Don't use useState for everything**:
- For example, instead of using state to store api result data, use [[React Query]] 
- Url data can be directly accessed with react router so dont use state for this

**Dervied value without state**:
``` javascript
function Date({date}) {
	const formatted = new Date(date).toLocaleDateString()

	return <p>Date: {formatted}</p>
}
```
==Will rerender when props change anyways==

**Use useEffect last**:
- For example, fetching data in useEffect means you are fetching data only after the component renders
	- this is very bad for UX because users have to wait for the data to render even though they see the component 
	- use [[React Query]] instead!