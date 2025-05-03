*Pages*
- Folder where root level pages live (Home.tsx, Login.tsx)
- Skeleton of react app

*Components*
- Small, modular components (buttons, textfield, [[modal]])
- is not made up of smaller components
	- *ui*
		- Subfolder in components 
		- It is comprised of smaller components 
		- visual difference between smaller components and general components

*Hooks*
- extract custom hook logic into this folder
- Examples:
	- useDebounce (delay updating of a value for a certain amount of time)
	- useCountdown
	- useCurrentUser

*Services*
- Api folder
- [[i18n]] folder
- state folder (redux, zustand, etc)
- providers folder

*utils*
- helpers.ts
	- any function that is small and useful used throughout application
- formatting.ts
	- formatting dates, text, etc