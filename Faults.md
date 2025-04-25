things that can go wrong or one component of the system deviating from its spec. It is not the same as a failure where the system as a whole stops providing the required service to the user
- Systems that can anticipate faults can cope with them are called fault-tolerant or [[Resilient]]

*There are different kinds of faults like*
1. Hardware faults: hard disk crash, RAM becomes faulty, blackout, etc
	1. Solution for this is usually redundancy(introducing extra components)
2. Software errors: usually lie dormant for a long time until they are triggered by an unusual set of circumstances
		The solution for this is to carefully think about assumptions and interactions in the system, thorough testing, process isolation, etc.
3. Human errors: humans are unreliable
	1. Solutions are design systems in a way that minimizes opportunities for error, create fully feature non-production sandbox environments, test thoroughly at all levels