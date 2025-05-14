==I saw leetcode kept track of all my submissions from the past for every question, so I was curious what the data model for this looked like==

*User Table*:
``` json
User {
	id: UUID,
	username: string,
	email: string,
}
```

*Problem Table*:
``` json
Problem {
	id: UUID,
	title: string,
	difficulty: enum('Easy', 'Medium', 'Hard')
}
```

*Submission Table*:
``` json
Submission {
	id: UUID, 
	user_id: UUID (Foreign key to user),
	problem_id: UUID (Foreign key to problem),
	code: text,
	language: enum('Java', 'Python', 'Go', ...),
	status: enum('Accepted', 'TLE', 'MLE', ...),
	runtime_ms: int,
	timestamp: datetime
}
```

*Get a user's most recent submissions for a problem*:
``` sql
SELECT * FROM Submission
WHERE user_id = 'joe123' AND problem_id = 'p456'
ORDER BY timestamp desc
```

