# Awesome-Product-Catalog-Price-Book-Management

## Top Product Catalog & Price Book Management Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Product Information Management (PIM), Price Books & Self-Hosted Catalog Platforms*  

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Product Catalog & Price Book Management**. These tools enable organizations to centralize product data—attributes, descriptions, images, pricing, and channel-specific variations—so that catalogs stay consistent across ecommerce, marketplaces, sales quotes, and ERP systems.



**Examples** include HubSpot Product Library, Akeneo PIM, Plytix, Salsify, inriver, Katana Cloud, DealHub Catalog, Salesforce Price Books, Pimcore, and Bluestone PIM (the category leaders).



**Open-source emphasis**: Product Catalog & Price Book Management is a domain where open-source tooling is **genuinely mature for PIM but fragmented for price-book-specific workflows**. **UnoPim** is the strongest actively developed open-source PIM—a Laravel-based system with centralized product management, AI content generation, multi-channel/multi-currency support, REST APIs, and proven scalability to **10 million+ products** . **Pimcore** offers an open-core platform combining PIM, DAM, and MDM, though its Community Edition moved to a revenue-restricted license in 2025 . **AtroPIM** provides a GPLv3 alternative with a configurable data model that lets business users create entities beyond products (suppliers, certificates, spare parts) without developer intervention . **Akeneo Community Edition** has been **paused by its vendor**—no new releases since 2023, with support ending September 2026—though the community fork **LibrePIM** provides ongoing maintenance . The critical caveat: **no open-source project provides a dedicated price-book abstraction** comparable to Salesforce Price Books—price management exists as product attributes or custom entities rather than a first-class pricing object .



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[HubSpot Product Library](https://www.hubspot.com/)**  

  Centralized product catalog within HubSpot's CRM; stores product properties, pricing, and descriptions that can be referenced in deals, quotes, and invoices.



- **[Akeneo PIM](https://www.akeneo.com/)**  

  The benchmark for enterprise PIM; product-centric data model with families, attributes, and reference entities; native Asset Manager; Data Quality Insights; and 2026 AI additions in the Serenity cloud (Ask Ziggy, AI-generated descriptions, attribute extraction) . **Critical caveat**: **Community Edition development is paused**—no new releases since 2023, with support ending September 30, 2026 .



- **[Plytix](https://www.plytix.com/)**  

  PIM and DAM platform positioned for SMB and mid-market; focused on centralized product data with channel syndication.



- **[Salsify](https://www.salsify.com/)**  

  Product experience management (PXM) platform; centralizes product content and syndicates to retailers and marketplaces.



- **[inriver](https://www.inriver.com/)**  

  Enterprise PIM with strong syndication and channel management capabilities.



- **[Katana Cloud](https://katanamrp.com/)**  

  Cloud inventory and manufacturing platform with product catalog capabilities; positioned for small manufacturers and makers.



- **[DealHub Catalog](https://dealhub.io/)**  

  CPQ and catalog management within DealHub's revenue platform; focused on quote-to-cash workflows.



- **[Salesforce Price Books](https://www.salesforce.com/)**  

  Native price book abstraction within Salesforce; supports multiple price books (standard and custom) with products assigned to specific price books and currencies.



- **[Pimcore](https://pimcore.com/)**  

  Open-core platform combining PIM, MDM, DAM, and DXP; **Community Edition licensing changed in 2025**—now free only for non-production, non-profit, and companies below EUR/USD 5 million annual revenue .



- **[Bluestone PIM](https://www.bluestonepim.com/)**  

  Cloud-native PIM built on a graph data model; focused on flexibility and API-first architecture.



## Open-Source GitHub Projects



### Full PIM Platforms (Product Catalog Focus)



- **[UnoPim](https://github.com/unopim/unopim)**  

  The **most actively developed open-source PIM** available (Laravel/PHP, open-source) . Features: **centralized product management** with configurable attributes and families; **Magic AI** for content generation across 10+ AI providers; **AI Agent Chat** for natural-language product management (search, create, update, bulk edit) ; **multi-channel and multi-currency** support; **localization** for 33 languages; **import/export** via CSV/XLSX with real-time progress tracking; **version control** for product data history; **REST API** with Postman collection; **DAM extension** for digital assets; and **Shopify/Bagisto connectors** for channel sync . **Scalability**: engineered for **10 million+ products** . **Requirements**: PHP 8.4.1+, MySQL/MariaDB/PostgreSQL, 8GB RAM . **Best for organizations wanting a production-grade open-source PIM** with active development and AI features—the closest open-source equivalent to Akeneo or Plytix.



- **[Pimcore (Community Edition)](https://github.com/pimcore/pimcore)**  

  Open-core PIM/MDM/DAM/DXP platform (PHP/Symfony, MySQL, Elasticsearch) . Features: **developer-defined data models** via class editor—unlimited flexibility for non-standard catalogs ; **native DAM** treating assets as first-class citizens with 200+ format previews ; **REST and GraphQL APIs** via Data Hub; and integration with commerce and CMS. **Critical licensing caveat**: since Platform Version 2025.1, the Community Edition uses the **Pimcore Open Core License**—free use is limited to non-production, non-profit, and companies below EUR/USD 5 million annual revenue . Professional at $9,900/year, Enterprise at $29,900/year . **Best for large platform projects with dedicated development teams** who need PIM + DAM + CMS in one system—but verify licensing fits your organization's revenue.



- **[AtroPIM](https://github.com/atrocore/atropim)**  

  Open-source PIM built on the AtroCore platform (GPLv3, no revenue threshold) . Features: **any entity, attribute, and relation created in the UI**—business users can model suppliers, certificates, spare parts, and other non-product entities without developer intervention ; **hierarchical product variants** with inherited values; **channel-specific attributes** for multi-shop/marketplace catalogs; **product classifications** with shared attribute sets; **bidirectional associations** (upsell, cross-sell); **product listings** for curated collections; and **custom text blocks** for reusable content. Tech: PHP/Symfony, PostgreSQL/MySQL/MariaDB, REST API with OpenAPI . **Best for companies with complex, non-standard data models** where business users need to shape the schema—especially organizations wary of Pimcore's revenue-threshold licensing.



### Specialized & Emerging Projects



- **[catalogue-server](https://pypi.org/project/catalogue-server/)**  

  Reusable **Django product catalogue** (Python package) with public pages, read-only JSON API, country-aware availability, and optional shop synchronization . Data model: **ProductGroup** (variants), **Product** (title, type, identifier, descriptions, image, JSON attributes, default price), **ProductCountryInfo** (country-specific price/availability), **Distributor**, and **Offer** (shop listings with price/stock) . **Shop sync**: built-in parsers for WooCommerce, Shopify, Squarespace, and Wix—scans preserve manual product assignments . **Best for Django developers** wanting a lightweight, reusable catalog foundation with country-specific pricing—not a full PIM with rich attribute management.



- **[LibrePIM](https://github.com/librepim/librepim)**  

  Community fork of **Akeneo Community Edition** created to provide long-term support after Akeneo paused CE development . Provides ongoing security patches and dependency updates (PHP, Elasticsearch, database components) to keep existing Akeneo CE instances secure and stable . **Best for organizations already running Akeneo CE** that need continued maintenance without migrating to the commercial Serenity cloud—but it is a fork, not a new platform.



### Additional Strong Open-Source Options



- **Odoo Product & Pricelists** — The Odoo ERP (LGPLv3 Community) includes product catalog management with **pricelists**—a native price-book abstraction supporting multiple currencies, tiered pricing, and customer-specific rules. **Best for organizations already on Odoo** wanting catalog and pricing integrated with sales, inventory, and accounting—but it is ERP-first, not a dedicated PIM.



**Frameworks for building custom systems**: For a **production-grade open-source PIM with AI features and active development**, UnoPim provides the strongest foundation . For **developer-led PIM + DAM + CMS with unlimited modeling flexibility**, Pimcore CE (verifying licensing) . For **business-user-shaped schemas with non-product entities**, AtroPIM . For **Django developers wanting a reusable catalog with country-specific pricing**, catalogue-server . **No open-source project provides a dedicated price-book abstraction** comparable to Salesforce Price Books—pricing is modeled as product attributes or custom entities, not a first-class object with its own assignment rules and currency handling.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Product catalog and PIM platforms handling product data and pricing must comply with applicable regulations and organizational data governance policies; **self-hosted solutions place full responsibility for security patches, backups, and uptime on the operator**.

- **Open-source PIM is mature but carries licensing and maintenance caveats**—**Akeneo Community Edition is paused** with support ending September 2026 , **Pimcore CE licensing changed in 2025** to restrict free use for larger companies , and **no open-source project provides a dedicated price-book abstraction** comparable to Salesforce Price Books. Choose based on whether you need a full PIM (UnoPim, Pimcore, AtroPIM) or a lightweight catalog (catalogue-server, Odoo).

- Verify license terms for commercial use; UnoPim is open-source (check repository) , Pimcore CE uses the Pimcore Open Core License , and AtroPIM uses GPLv3 .



---



**Made for product data managers, ecommerce operations teams, and organizations choosing their catalog and pricing infrastructure.**  

Let's make product catalog management more open, but with clear eyes about the Akeneo CE pause, Pimcore's licensing shift, and the price-book abstraction gap that commercial platforms still fill.
