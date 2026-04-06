# Sportly: Dynamic Sports CMS & Technical Comparative Analysis 🏏⚽🏀

**Live Website:** [sportly-transiverse.xo.je](https://sportly-transiverse.xo.je/)  
**Full Comparative Analysis Report:** [📄 Read the 10-page PDF here](./docs/Sportly-Comparative-Analysis.pdf)

## 📌 Project Overview
This project involves the development of a dynamic sports blog website using WordPress, capable of managing content for Cricket, Football, and Basketball while supporting live match data integration via external APIs. 

Beyond just development, this repository serves as a comparative technical and architectural evaluation benchmarking our custom WordPress theme against large-scale industry platforms: Sportskeeda, Cricbuzz, and ESPNcricinfo.

## 🛠️ Architecture & Tech Stack
Our conceptual architecture follows a classic CMS model optimized for content publishing:
* **Frontend:** Custom HTML/CSS/JS, Elementor (UI Tooling)
* **Backend:** WordPress CMS, PHP (Server-Side Rendering)
* **Data Integration:** REST API for live sports data
* **Caching & Performance:** LiteSpeed Cache, WP REST Cache, Smush
* **Deployment:** Hosted on InfinityFree

*Flow:* `Frontend UI → WordPress Backend (PHP + WP Core) → Caching Layer → Data Sources (WP Database + External API)`

## 🚧 Challenges Solved
During development, we resolved several critical routing and dynamic rendering issues:
* **Routing & 404 Errors:** Updated permalink structure to "Post Name" and utilized `.htaccess` rewrite rules to map custom pages correctly.
* **Dynamic Rendering:** Converted static HTML into WordPress templates (`front-page.php`, `single.php`, etc.) and implemented the WordPress Loop to pull in the latest posts.
* **Link Management:** Removed hardcoded `.html` links, replacing them with dynamic WordPress functions like `home_url()` and `get_template_directory_uri()`.

## 📊 Performance Benchmarking (March 2026 Averages)
We audited Sportly against major platforms using PageSpeed Insights/Lighthouse. 

| Website | Platform | Performance Score | LCP (Largest Contentful Paint) |
| :--- | :--- | :--- | :--- |
| **SPORTLY** | Desktop | 84 | 1.4s |
| **SPORTLY** | Mobile | 60 | 1.9s |
| **Sportskeeda** | Desktop | 88 | 1.1s |
| **Cricbuzz** | Desktop | 92 | 0.8s |

**Key Insight:** While our WordPress CMS is highly effective for content-driven workflows, platforms like Cricbuzz achieve lower LCPs and faster live scoring at scale by utilizing distributed backend services, high-concurrency infrastructure, and Next.js Server-Side Rendering (SSR).

## 🚀 Version 2.0 Roadmap
For future iterations, we plan to implement:
1. **Infrastructure:** Adding a CDN (like Cloudflare) for static asset acceleration.
2. **Performance:** Converting images to WebP/AVIF and enforcing responsive sizing to boost mobile PageSpeed scores.
3. **Live Data:** Caching API responses using transients with controlled TTL and implementing lightweight AJAX polling for near real-time updates.

## 💻 Local Setup & Installation
To run this custom WordPress build locally:
1. Clone this repository into your `htdocs` (XAMPP) or `www` (WAMP) directory.
2. Import the database file (e.g., `sportly_db.sql`) into your local phpMyAdmin.
3. Update the `wp-config.php` file with your local database credentials (usually `root` and a blank password).
4. Log in to the local WP Admin dashboard, go to Settings > Permalinks, and click "Save Changes" (Post Name) to flush the rewrite rules and avoid 404 errors.

## 👥 Team
* **Shivraj Mule**
* **Vaibhav Anand**
* **Ayush Kumar Singh**
* **Amit Gadade**
