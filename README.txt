1. Briefly describe the conceptual approach you chose! What are the trade-offs?
	a. ubuntu:16.04 image created on google cloud using Infrastructure as a Code Templates
	b. Docker images created using Docker file, uploaded by me on GitHub at https://github.com/chandrasekhar-DevOps/QuarticCodeChallenge.git
	c. Kubernetes Cluster and Load Balancer created
	d. using uWSGI to communicate with Django application

2. What are the operational limits to your approach?
	Heavy SQL queries are hard to execute
	Complex architecture to maintain 


3. What will be the annual cost of hosting this solution for 1 year for 10K concurrent users. Describe your method.

	Considering low offerings of storage cost by varies cloud providers, I am focusing more on compute and IO costs
	Below cost calculated based on AWS Total Cost of Ownership (TCO) Calculator
	Assume we pay 0.05$ for a GB of storage, 0.15$ for each MB of RAM, 0.06$ for each Kbps of uplink and 0.008$ for each MHz of CPU per user
	Per user cost = 0.05$ for a GB of storage+ 0.15$ for each MB of RAM + 0.06$ for each Kbps of uplink + 0.008$ for each MHz of CPU = 0.268 USD
	Per user cost per year = 0.268*365 = $97.82
	Total cost for 10K users = $978200



4. If you had more time, what improvements would you make, and in what order of priority?
	Implementing caching strategy to increase performance efficiency 
	Configure DR's
