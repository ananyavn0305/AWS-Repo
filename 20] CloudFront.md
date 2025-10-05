## Easy Questions

1. What is Amazon CloudFront?  
   - A content delivery network (CDN) service for fast and secure content delivery.

2. What are edge locations in CloudFront?  
   - Data centers around the world where CloudFront caches content for low-latency delivery.

3. How does CloudFront reduce latency?  
   - By routing user requests to the nearest edge location.

4. What is a CloudFront distribution?  
   - A set of rules that tells CloudFront how to handle requests and deliver content.

5. Can CloudFront deliver dynamic content?  
   - Yes, it can deliver both static and dynamic content.

6. What protocol does CloudFront use for secure content delivery?  
   - HTTPS (SSL/TLS).

7. Does CloudFront store content permanently?  
   - No, it caches content temporarily at edge locations.

8. Can CloudFront be used with S3?  
   - Yes, S3 can be an origin for CloudFront distributions.

9. Is CloudFront a global or regional service?  
   - Global, using multiple edge locations worldwide.

10. What is the main benefit of using CloudFront?  
    - Improved content delivery speed and reduced latency for end-users.

## Moderate Questions

1. What is the difference between CloudFront origin and edge location?  
   - Origin is the source of content; edge locations cache content for delivery.

2. How does CloudFront handle cache expiration?  
   - Using TTL (Time-to-Live) settings defined in cache behavior or headers.

3. Can you restrict access to CloudFront content?  
   - Yes, using signed URLs, signed cookies, and origin access identity.

4. What is an origin in CloudFront?  
   - The source server or bucket from which CloudFront fetches content.

5. How do you invalidate cached content in CloudFront?  
   - By creating an **invalidation request** to remove objects from edge caches.

6. How does CloudFront integrate with AWS WAF?  
   - WAF can be associated with a distribution to protect against web attacks.

7. What is a CloudFront behavior?  
   - Rules that define how CloudFront processes requests for different URL patterns.

8. Can CloudFront serve content from multiple origins?  
   - Yes, a distribution can have multiple origins with different cache behaviors.

9. How does CloudFront support HTTPS for custom domains?  
   - By attaching an SSL/TLS certificate to the distribution.

10. What is the difference between standard and real-time logs in CloudFront?  
    - Standard logs are stored in S3 for batch analysis; real-time logs are streamed for instant insights.

## Hard Questions

1. Explain how CloudFront reduces load on the origin server.  
   - By caching content at edge locations, fewer requests reach the origin.

2. How does CloudFront work with Lambda@Edge?  
   - Lambda@Edge allows running functions to modify requests/responses at edge locations.

3. What is geo-restriction in CloudFront?  
   - It allows or blocks access to content based on the viewer's geographic location.

4. How does CloudFront handle dynamic content caching?  
   - By using **cache policies** and **origin request policies** for selective caching.

5. Can CloudFront work with non-AWS origins?  
   - Yes, it can use any publicly accessible HTTP/HTTPS origin.

6. How does CloudFront maintain content freshness across edge locations?  
   - Using TTL settings, invalidations, and origin fetch on cache miss.

7. What is the difference between a regional edge cache and an edge location?  
   - Regional edge caches are larger caches between origin and edge locations for frequently accessed content.

8. How do signed URLs and cookies work in CloudFront?  
   - They grant temporary, restricted access to private content based on time and policies.

9. Explain the use of origin access identity (OAI) with S3.  
   - OAI allows CloudFront to access private S3 buckets securely without exposing them publicly.

10. How does CloudFront optimize content delivery for global users?  
    - By routing requests to the nearest healthy edge location and caching content globally.
