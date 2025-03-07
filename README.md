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
  
  

# Developer (100 Points)  
## 10 Multi choice questions, 30 min (25 points)  
1. Node.js: Event Loop Behavior  
Which of the following statements about the Node.js Event Loop are correct?  
A) It enables Node.js to handle multiple concurrent requests efficiently.  
B) It allows JavaScript to run on multiple CPU cores by default.  
C) It is responsible for managing asynchronous operations.  
D) It always executes code in a synchronous manner.  
✅ Correct Answer: A, C  
📝 Explanation: The event loop allows non-blocking operations (A) and manages async tasks (C). However, Node.js runs on a single thread by default (B is incorrect) and does not force synchronous execution (D is incorrect).  
    
2. React: State Management  
Which of the following are valid ways to manage state in a React app?  
A) Using React Context API for deep component trees  
B) Using Redux for centralized state management  
C) Storing state inside a component with React.useState  
D) Managing state in localStorage for performance improvements  
✅ Correct Answer: A, B, C  
📝 Explanation: Context API (A) and Redux (B) are for state management, while useState (C) is for component-level state. localStorage (D) is not a state management tool, and reading from it can cause performance issues.  
    
3. PHP: Security Practices  
Which of the following improve PHP security?  
A) Using password_hash() to store passwords securely  
B) Using htmlspecialchars() to prevent XSS attacks  
C) Using mysql_real_escape_string() to prevent SQL injection  
D) Using session_regenerate_id() to prevent session fixation  
✅ Correct Answer: A, B, D  
📝 Explanation:  
password_hash() (A) securely hashes passwords.  
htmlspecialchars() (B) prevents XSS attacks.  
session_regenerate_id() (D) prevents session fixation.  
mysql_real_escape_string() (C) is deprecated and not safe; use prepared statements instead.  
    
4. Node.js: Performance Optimization  
Which techniques help optimize performance in a Node.js application?  
A) Using clustering to utilize multiple CPU cores  
B) Using caching layers like Redis to reduce database load  
C) Handling async operations with synchronous functions  
D) Enabling compression like Gzip to reduce response size  
✅ Correct Answer: A, B, D  
📝 Explanation:  
Clustering (A) improves performance on multi-core machines.  
Caching (B) reduces database queries.  
Compression (D) reduces payload sizes.  
Handling async with synchronous functions (C) blocks the event loop and degrades performance.  
    
5. React: Performance Optimization  
Which methods can improve performance in a React app?  
A) Using React.memo to prevent unnecessary re-renders  
B) Using lazy loading to split large components  
C) Keeping all application state in Redux for consistency  
D) Debouncing input fields to reduce unnecessary renders  
✅ Correct Answer: A, B, D  
📝 Explanation:  
React.memo (A) prevents unnecessary re-renders.  
Lazy loading (B) improves page load time.  
Debouncing (D) prevents rapid state updates.  
Keeping all state in Redux (C) can degrade performance when overused.  
    
6. Android: Networking & APIs  
Which libraries are commonly used for handling network requests in Android?  
A) Retrofit  
B) Glide  
C) OkHttp  
D) Volley  
✅ Correct Answer: A, C, D  
📝 Explanation:  
Retrofit (A), OkHttp (C), and Volley (D) are all used for network requests.  
Glide (B) is for image loading, not API requests.  
    
7. API Design: REST vs GraphQL  
Which of the following statements about REST and GraphQL are correct?  
A) REST APIs use multiple endpoints, whereas GraphQL typically has a single endpoint.  
B) REST APIs always return only the requested fields to optimize bandwidth.  
C) GraphQL allows clients to request only the data they need.  
D) GraphQL is always faster than REST APIs for every use case.  
✅ Correct Answer: A, C  
📝 Explanation:  
REST uses multiple endpoints (A) while GraphQL uses one.  
GraphQL allows clients to select fields (C), reducing over-fetching.  
REST APIs often return unnecessary data (B is incorrect).  
GraphQL is not always faster than REST (D is incorrect).  
    
8. Android: Activity Lifecycle  
Which of the following methods are part of the Android Activity Lifecycle?  
A) onCreate()  
B) onDestroy()  
C) onStartService()  
D) onResume()  
✅ Correct Answer: A, B, D  
📝 Explanation:  
onCreate() (A), onDestroy() (B), and onResume() (D) are lifecycle methods.  
onStartService() (C) is incorrect; it’s used for services, not activities.  
    
9. Security: Cross-Origin Resource Sharing (CORS)  
Which statements about CORS are correct?  
A) CORS is enforced by web browsers, not backend servers.  
B) Enabling Access-Control-Allow-Origin: * ensures maximum security.  
C) Preflight requests are sent for certain HTTP methods like PUT and DELETE.  
D) CORS policies are defined in HTTP response headers.  
✅ Correct Answer: A, C, D  
📝 Explanation:  
CORS is enforced by browsers (A).  
Preflight requests (C) occur for PUT/DELETE.  
CORS headers (D) define access policies.  
Allowing * (B) is insecure, as it grants unrestricted access.  
    
10. Full-Stack: Database Scaling Strategies  
Which methods improve database scalability?  
A) Using read replicas to distribute read queries  
B) Adding more CPU and RAM to the database server for horizontal scaling  
C) Caching frequently accessed queries  
D) Database sharding to distribute data across multiple instances  
✅ Correct Answer: A, C, D  
📝 Explanation:  
Read replicas (A) reduce load on the primary database.  
Sharding (D) distributes data to improve performance.  
Caching (C) speeds up repeated queries.  
Adding CPU/RAM (B) is vertical scaling, not horizontal.  
    
## Coding Problem 1: Algorithm – Longest Consecutive Sequence  
(Any Coding Language is OK, Console log or command line log display ok)  
⏳ Estimated Time: 30 minutes  
💻 Difficulty Level: Medium  
Problem Statement:  
Given an unsorted array of integers, find the length of the longest consecutive elements sequence.  
You must solve it in O(n log n) time complexity.  
The sequence must be continuous in terms of numbers, not indices.  
"longest consecutive" means:  
A sequence of numbers in the array that appear in order without gaps (but not necessarily adjacent in the array).  
The sequence must be incremented by 1 each time.  
Example of "Longest Consecutive Sequence" Meaning  
Valid Consecutive Sequence:  
✅ [1, 2, 3, 4] (Numbers appear in order)  
✅ [100, 101, 102]  
    
Example Input & Output:  
Example 1:  
Input: nums = [100, 4, 200, 1, 3, 2]  
Output: 4  
Explanation: The longest consecutive sequence is [1, 2, 3, 4].  
    
Example 2:  
Input: nums = [9, 1, 8, 3, 4, 2, 5, 7, 6]  
Output: 9  
Explanation: The longest consecutive sequence is [1, 2, 3, 4, 5, 6, 7, 8, 9].  
    
Expected Complexity:  
✅ O(n * log n) time complexity  
    
✅ Max Score: 25 Points  
Category | Criteria | Marks  
|-------|----------|---------|
Correctness  | The function correctly finds the longest consecutive sequence in various test cases.  |10  
Efficiency  | Uses O(n * log n) time complexity with sorting or set instead of brute force (O(n^2)).  | 6  
Edge Case Handling  | Handles cases like empty array, all duplicates, single element, and scattered numbers.  | 5  
Code Readability  | Well-structured logic, meaningful variable names, proper indentation, and comments.  | 4  
    
    

## Coding Problem 2 (Backend): API for Product Search with Pagination  
⏳ Estimated Time: 30 minutes  
💻 Difficulty Level: Medium  
Problem Statement:  
Create an API endpoint that allows searching for products with pagination.  
The endpoint should accept search keywords and return matching products.  
Results should be paginated with limit and offset parameters.  
Example API Call:  
GET /api/products?search=phone&limit=10&offset=20  
    
Expected Output:  
json  
{  
    "products": [  
    { "id": 21, "name": "iPhone 13", "price": 799 },  
    { "id": 22, "name": "Samsung Galaxy S23", "price": 999 }  
    ],  
    "total": 200  
}  
    
Requirements:  
✅ Use any backend language (Node.js, PHP, etc.)  
✅ Implement SQL Query for Filtering & Pagination  
✅ Consider security (e.g., SQL injection protection)  
Hints:  
Use a WHERE clause for filtering.  
Use LIMIT & OFFSET for pagination.  
Make sure to return the total product count for frontend pagination.  
✅ Max Score: 25 Points  
Category | Criteria | Marks  
|-------|----------|---------|
Correctness | API returns correct filtered & paginated results. | 10  
SQL Query Optimization | Uses LIMIT & OFFSET efficiently, avoids SELECT *. | 5  
Security | Prevents SQL injection (uses prepared statements). | 4  
Error Handling | Properly handles invalid queries (e.g., missing parameters).  |3  
Code Readability | Clean endpoint design, structured query building. | 3  
    
    
    
## Coding Problem 3 (Frontend): Countdown Timer App   
⏳ Estimated Time: 30 minutes  
💻 Difficulty Level: Medium  
🚀 Technology: React or Vanilla JavaScript + HTML + CSS  
📌 No third-party libraries allowed  
    
Problem Statement:  
Create a Countdown Timer App where:  
The user enters a time (in seconds) and starts the countdown.  
The countdown displays the remaining time and updates every second.  
The user can pause, resume, or reset the timer.  
    
Requirements:  
✅ A number input to set the countdown time  
✅ A Start button to begin the countdown  
✅ Pause & Resume buttons  
✅ A Reset button to stop and reset the timer  
✅ The countdown should reach 0 and then stop  
    
Example UI Behavior:  
User enters 60 and clicks Start → Timer counts down from 60 → 59 → 58 → ... → 0.  
User clicks Pause → Timer stops at the current value.  
User clicks Resume → Timer continues counting down.  
User clicks Reset → Timer resets to the original value.  
    
✅ Max Score: 25 Points  
Category  | Criteria  | Marks  
|-------|----------|---------|
Correctness  | Timer starts, pauses, resumes, and resets correctly.  | 10  
State Management  | Uses React useState/useEffect or JS setInterval properly.  | 5  
User Experience  | Prevents negative numbers, disables inappropriate buttons.  | 4  
Persistence (Optional Bonus)  | Stores last timer state in localStorage (React/VanillaJS).  | 3  
Code Readability  | Clean component logic, well-commented code.  | 3  
     
     
   
