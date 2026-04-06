# Sportly: Dynamic Sports CMS & Technical Comparative Analysis 🏏⚽🏀

[cite_start]**Live Website:** [sportly-transiverse.xo.je](http://sportly-transiverse.xo.je) 

## 📌 Project Overview
[cite_start]This project involves the development of a dynamic sports blog website using WordPress, capable of managing content for Cricket, Football, and Basketball while supporting live match data integration via external APIs[cite: 39, 41]. 

[cite_start]Beyond just development, this repository serves as a comparative technical and architectural evaluation benchmarking our custom WordPress theme against large-scale industry platforms: Sportskeeda, Cricbuzz, and ESPNcricinfo.

## 🛠️ Architecture & Tech Stack
Our conceptual architecture follows a classic CMS model optimized for content publishing:
* [cite_start]**Frontend:** Custom HTML/CSS/JS, Elementor (UI Tooling) [cite: 45, 63]
* [cite_start]**Backend:** WordPress CMS, PHP (Server-Side Rendering) [cite: 43, 44]
* [cite_start]**Data Integration:** REST API for live sports data [cite: 46]
* [cite_start]**Caching & Performance:** LiteSpeed Cache, WP REST Cache, Smush [cite: 59]
* [cite_start]**Deployment:** Hosted on InfinityFree [cite: 47]

[cite_start]*Flow:* `Frontend UI → WordPress Backend (PHP + WP Core) → Caching Layer → Data Sources (WP Database + External API)` [cite: 50]

## 🚧 Challenges Solved
[cite_start]During development, we resolved several critical routing and dynamic rendering issues[cite: 54, 55]:
* [cite_start]**Routing & 404 Errors:** Updated permalink structure to "Post Name" and utilized `.htaccess` rewrite rules[cite: 57].
* [cite_start]**Dynamic Rendering:** Converted static HTML into WordPress templates (`front-page.php`, `single.php`, etc.) and implemented the WordPress Loop[cite: 57].
* [cite_start]**Link Management:** Removed hardcoded `.html` links, replacing them with dynamic WordPress functions like `home_url()` and `get_template_directory_uri()`[cite: 57].

## 📊 Performance Benchmarking (March 2026 Averages)
[cite_start]We audited Sportly against major platforms using PageSpeed Insights/Lighthouse[cite: 17, 66]. 

| Website | Platform | Performance Score | LCP |
| :--- | :--- | :--- | :--- |
| **SPORTLY** | Desktop | 84 | [cite_start]1.4s | 
| **SPORTLY** | Mobile | 60 | [cite_start]1.9s | 
| **Sportskeeda** | Desktop | 88 | [cite_start]1.1s | 
| **Cricbuzz** | Desktop | 92 | [cite_start]0.8s | 

[cite_start]**Key Insight:** While our WordPress CMS is highly effective for content-driven workflows, platforms like Cricbuzz achieve lower LCPs and faster live scoring at scale by utilizing distributed backend services, high-concurrency infrastructure, and Next.js SSR[cite: 19, 118, 119].

## 🚀 Version 2.0 Roadmap
For future iterations, we plan to implement:
1. [cite_start]**Infrastructure:** Adding a CDN (like Cloudflare) for static asset acceleration[cite: 142].
2. [cite_start]**Performance:** Converting images to WebP/AVIF and enforcing responsive sizing[cite: 135].
3. [cite_start]**Live Data:** Caching API responses using transients with controlled TTL and implementing lightweight AJAX polling for near real-time updates[cite: 139, 140].

## 👥 Team
* [cite_start]Shivraj Mule [cite: 5]
* [cite_start]Vaibhav Anand [cite: 6]
* [cite_start]Ayush Kumar Singh [cite: 7]
* [cite_start]Amit Gadade [cite: 8]