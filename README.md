## PM & Engineer (100 Points)  
# (15 Multi choice, True/False questions, 45 min, 60 points)  
  
1. Load Balancer: Key Benefits  
(Multi-Choice)  
Which of the following are key benefits of using a Load Balancer?
A) Distributes traffic evenly across multiple servers  
B) Improves application fault tolerance  
C) Ensures that all requests are handled by a single server  
D) Allows horizontal scaling  
✅ Correct Answer: A, B, D  
📝 Explanation: Load balancers distribute traffic (A), improve fault tolerance (B), and support horizontal scaling (D).  They do not force all requests to a single server (C).

2. Load Balancer: Reverse Proxy vs Load Balancer (True/False)  
A Reverse Proxy can also act as a Load Balancer.  
Load Balancers always distribute traffic based on CPU utilization of backend servers.  
✅ Correct Answers:  
✅ True – Many reverse proxies (e.g., Nginx, HAProxy) have load balancing features.  
❌ False – Load balancers distribute traffic using different algorithms (e.g., round-robin, least connections), not just CPU utilization.  

3. Proxy: Forward vs Reverse Proxy  
(Optional - Single Choice)  
A forward proxy is typically used to:  
A) Load balance backend servers  
B) Hide client identities from the internet  
C) Improve API response times  
D) Secure backend microservices  
✅ Correct Answer: B) Hide client identities from the internet  
📝 Explanation: Forward proxies help users stay anonymous by routing requests through an intermediary.  

4. Microservices: Best Practices  
(Multi-Choice)  
Which are best practices when designing microservices?  
A) Each microservice should have its own database  
B) Services should be loosely coupled  
C) Directly calling database tables from another microservice improves performance  
D) Services should communicate via APIs  
✅ Correct Answer: A, B, D  
📝 Explanation: Microservices should have separate databases (A), loose coupling (B), and communicate via   APIs (D). Direct database access between services (C) creates tight coupling.  

5. Monolithic: Disadvantages  
(True/False)  
Monolithic applications are easier to scale than microservices.  
Debugging a monolithic application is usually simpler than debugging microservices.  
✅ Correct Answers:  
❌ False – Scaling a monolithic app requires upgrading the entire system, which is harder.  
✅ True – Debugging a monolith is easier since all components are in one place.  

6. API Gateway: Key Features  
(Multi-Choice)  
What features are commonly provided by API Gateways?  
A) Rate Limiting  
B) Authentication  
C) Direct database access  
D) Logging and Monitoring  
✅ Correct Answer: A, B, D  
📝 Explanation: API Gateways provide rate limiting (A), authentication (B), and logging/monitoring (D) but do not access databases directly (C).  

7. API Gateway: Rate Limiting  
(Optional - Single Choice)  
What is the main reason for rate limiting in an API Gateway?  
A) To prevent excessive load on backend services  
B) To improve SEO rankings  
C) To reduce API request latency  
D) To allow more users to send unlimited requests  
✅ Correct Answer: A) To prevent excessive load on backend services  
📝 Explanation: Rate limiting helps control traffic to prevent abuse and overload on backend services.  

8. Caching: Key Benefits  
(Multi-Choice)  
What are benefits of caching?  
A) Faster response times  
B) Lower database load  
C) Always up-to-date data  
D) Reduced API costs  
✅ Correct Answer: A, B, D  
📝 Explanation: Caching speeds up responses (A), reduces database load (B), and saves API costs (D), but may serve stale data (C).  

9. Horizontal Scaling: Challenges  
(True/False)  
Horizontal scaling is harder than vertical scaling because it requires distributing stateful data across multiple nodes.  
Vertical scaling always provides better performance than horizontal scaling.  
✅ Correct Answers:  
✅ True – Managing state in horizontal scaling is complex.  
❌ False – Horizontal scaling is often better for large-scale applications.  
  
10. JWT Authentication: Secure Handling  
(Multi-Choice)  
How should JWTs be securely stored?  
A) Store in HTTP-only cookies  
B) Store in localStorage  
C) Encrypt before storing in a database  
D) Send JWTs over HTTP instead of HTTPS  
✅ Correct Answer: A, C  
📝 Explanation: Store JWTs in HTTP-only cookies (A) and encrypt if stored (C). Never use localStorage (B) due to XSS risks.  
  
11. Websockets: When to Use  
(Optional - Single Choice)  
WebSockets are ideal for which application?  
A) Real-time stock price updates  
B) Static content websites  
C) Periodic batch processing  
D) Database backups  
✅ Correct Answer: A) Real-time stock price updates  
📝 Explanation: WebSockets allow low-latency real-time communication.  
  
12. Rate Limiting: Protection  
(True/False)  
Rate limiting helps prevent DDoS attacks.  
Rate limiting is ineffective if implemented at the API Gateway level.  
✅ Correct Answers:  
✅ True  
❌ False – API Gateways are effective for rate limiting.  
  
13. CORS: Importance  
(Multi-Choice)  
Which are true about CORS?  
A) Protects against Cross-Site Scripting (XSS) attacks  
B) Allows safe communication between different origins  
C) Can be configured using HTTP response headers  
D) Prevents all cross-origin requests  
✅ Correct Answer: B, C  
📝 Explanation: CORS enables secure cross-origin communication (B) and is configured via HTTP headers (C). It does not prevent all cross-origin requests (D).  
  
14. CORS: Browser Behavior  
(True/False)  
CORS is enforced by web browsers, not by backend servers.  
Adding Access-Control-Allow-Origin: * makes an API completely secure.  
✅ Correct Answers:  
✅ True  
❌ False – * allows any domain to access the API, reducing security.  
  
15. Scaling: Vertical vs Horizontal  
(Optional - Single Choice)  
Which statement about scaling is correct?  
A) Vertical scaling means adding more servers  
B) Horizontal scaling allows distributing load across multiple servers  
C) Vertical scaling is cheaper than horizontal scaling in cloud environments  
D) Horizontal scaling is always easier than vertical scaling  
✅ Correct Answer: B) Horizontal scaling allows distributing load across multiple servers  
  
# System architecture design  
(2 Open-Ended questions, 45 min, 40 points)  
  
### Problem 1: Design a Scalable Live Chat Application  
💡 Scenario:  
Your company wants to build a real-time live chat application where:  
Users can send and receive messages instantly.  The system should support 1 million concurrent users.  
Authentication should be secure and scalable.  Messages should be persisted for later retrieval.  
The architecture should handle high traffic spikes efficiently.  
  
Key Considerations to check:  
Scalability: How will the system handle increasing user traffic?  
WebSockets: How will the system maintain real-time communication?  
Authentication: How will users be authenticated (e.g., JWT)?  
Load Balancing: How will traffic be distributed among servers?  
Caching: Will messages be cached for faster access?  
Database Choice: What database(s) will store the messages?  
Rate Limiting: How will spam/malicious messages be prevented?  
CORS Considerations: How will cross-origin access be handled?  
  
### Problem 2: Design a High-Performance E-Commerce API  
💡 Scenario:  
Your company is launching a new e-commerce platform where:  
Users can browse products, add items to carts, and complete purchases.  
The system should handle 10,000 requests per second.  Authentication should be secure and allow third-party integrations.  
Product data should be fetched quickly for a smooth user experience.  The system should be highly available with minimal downtime.  
  
Key Considerations to check:  
Microservices vs Monolithic: Which approach is better and why?  
API Gateway: How will you manage API traffic and authentication?  
Caching Strategy: How will you cache product details to reduce database load?  
Database Design: Will you use SQL, NoSQL, or both? Why?  
Load Balancing: How will traffic be distributed?  
Rate Limiting: How will you prevent abuse of API requests?  
CORS Handling: How will frontend apps securely access the API?  
Horizontal Scaling: How will you ensure the system scales to millions of users?  
  
How to Evaluate the User’s Solution (Max Value: 20)  
You can assess their response based on the following criteria:  
  
| Category |  Criteria to Check |  Max Points 
|--------------|---------------------------------------------|------------|
| Scalability | Can the system handle high user traffic efficiently? | 3  
Load Balancing | Are load balancers used properly to distribute traffic? | 2  
WebSockets (Chat App) | Does the candidate understand real-time communication? | 2  
Microservices vs Monolith | Is the architecture choice justified with trade-offs? | 2  
Authentication | Are JWTs or secure authentication methods used? | 2  
Caching Strategy | Are caching mechanisms (e.g., Redis) proposed? | 2  
Database Choice | Is the database well-suited for performance and scalability? | 2  
Rate Limiting | Is rate limiting considered to protect the system? | 2  
CORS Handling | Does the solution address cross-origin security issues? | 1  
Deployment & Scaling | Is horizontal scaling implemented effectively? | 2  
  
  
  
