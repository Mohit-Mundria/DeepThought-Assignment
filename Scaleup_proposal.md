# PART B: Sourcing Strategy & 1,000-Company Scale-Up Proposal

## Question 1: Advanced Sourcing Methods Beyond Simple Search

To consistently find true "Federer" companies across India without relying on basic Google search queries, I will utilize four specific, high-signal data vectors:

### 1. Ministry of Corporate Affairs (MCA) Registry Filings via Bulk Scraping
* **Why it works:** Every registered company in India must file monthly and annual reports with the Registrar of Companies (RoC). By isolating companies registered under specific National Industrial Classification (NIC) codes (e.g., **NIC 29: Manufacture of motor vehicles, trailers, and semi-trailers** or **NIC 28: Manufacture of machinery and equipment**), we capture the entire baseline of potential producers.
* **ICP Signal:** Filtering for companies with authorized capital between ₹5 Crore and ₹50 Crore instantly isolates the ₹50Cr–₹500Cr revenue mid-market sweet spot.
* **Limitations:** MCA filings don't show qualitative data like systems maturity or active hiring trends. It works as an excellent top-of-funnel filter, but requires secondary qualification stages.

### 2. Tier-1 OEM Supplier Portals and Vendor Directory Scraping
* **Why it works:** Massive OEMs (such as Tata Motors, Mahindra, Maruti Suzuki, and Bajaj) maintain strict vendor directories. Companies listed as Tier-1 or Tier-2 components suppliers are guaranteed physical producers (passing Gate E1) and already operate at a baseline level of structural accountability.
* **ICP Signal:** If a company supplies precision powertrain castings or specialized CNC transmission components to a major OEM, they inherently possess a capability-based moat.
* **Limitations:** These lists are frequently gated behind secure partner networks, requiring custom scraping tools or session tokens to extract.

### 3. Industrial Expo Exhibitor Registries (e.g., Auto Expo Components, IMTEX)
* **Why it works:** Companies exhibiting at premier manufacturing trade shows like IMTEX (Indian International Machine Tool Exhibition) or the Auto Expo Components show are actively looking to scale up and capture new markets.
* **ICP Signal:** Spending capital on a booth at a major industrial expo is a strong indicator of a growth mindset (C6 Growth Signals) and an active investment in expansion.
* **Limitations:** Exhibitor directories are only updated once or twice a year, meaning secondary verification is required to check their current revenue bands.

### 4. Specialized Certification Registries (AS9100, IATF 16949, DSIR Recognition)
* **Why it works:** Getting certified under aerospace standards (AS9100) or high-level automotive quality systems (IATF 16949) takes months of preparation. Similarly, obtaining formal recognition from the Department of Scientific and Industrial Research (DSIR) requires proving real innovation.
* **ICP Signal:** A company with an IATF or DSIR certification automatically scores highly on **C3 (Differentiation)** and **C7 (Systems Maturity)** because these certifications cannot be achieved without rigid, documented workflows and asset tracking systems.
* **Limitations:** These public registries are highly fragmented, requiring specialized extraction scripts to scrape data from individual certifying body websites.

---

## Question 2: The 1,000-Company Scale-Up Strategy (30-Day Execution Blueprint)

To build a verified dataset of 1,000 true "Federer" companies within 30 days, we must combine high-speed programmatic scraping with an active, automated LLM verification layer.

### 1. Sourcing the Initial Universe (Week 1 Target: 4,000 Names)
* **Strategy:** Use programmatic API loops targeting corporate database registries (ZaubaCorp, Tofler, Tracxn) alongside specialized NIC industrial codes to extract all manufacturing entities across our selected 11 Indian cities.
* **Filters Applied:** Limit the search to entities with active corporate standings, operational timelines greater than 3 years, and an estimated capital size matching the ₹50Cr–₹500Cr revenue bracket.
* **Expected Stage Yield:** Start with roughly **4,000 raw matches**.

### 2. Automated Qualification Layer (Week 2 Target: 1,800 Clean Profiles)
* **Strategy:** Run a multi-threaded Python script to scrape the website links discovered during Week 1. This pipeline converts raw HTML data into structured text blocks and passes them to an LLM context window (using Claude-3.5-Haiku or Gemini-1.5-Flash) for evaluation.
* **The LLM Prompt Protocol:** * *“Examine this scraped company text. Is this entity a physical producer or a trader/distributor? Locate explicit mentions of manufacturing sites, plant locations, or machinery assets.”*
    * *“Scan for mentions of enterprise resource software (SAP, Oracle, ERP, MRP) or advanced machinery types.”*
* **Expected Stage Yield:** Roughly 55% of companies will fail due to lacking an active web footprint, operating as pure traders, or breaching the revenue ceiling, narrowing the list down to **1,800 valid candidates**.

### 3. Quality Control and Validation Gates (Week 3 Target: 1,100 Verified Profiles)
* **Strategy:** Run automated LinkedIn API lookups to verify operational health and leadership transitions:
    * **Systems Check:** Search for internal IT support titles, SAP administrators, or ERP coordinators inside the company's employee list to verify systems maturity.
    * **Succession Check:** Cross-reference active director names on the board to spot same-surname Gen-2 appointments or recent executive hires from outside the family.
    * **Growth Check:** Check the total number of open job roles on platforms like Naukri or LinkedIn over the past 180 days.
* **Expected Stage Yield:** This phase filters out stagnant companies or firms without clear organizational systems, bringing us down to **1,100 high-probability targets**.

### 4. Human-In-The-Loop Validation & Delivery (Week 4 Target: 1,000 Final Passes)
* **Strategy:** Dedicate the final week to human spot-checking, focusing on the highest scoring prospects and borderline cases flagged by the automated script.
* **Sanity Checks:** Verify that the primary operations are physically based within the target cities, and manually confirm that the personalization hooks align with the company's latest real-world announcements.
* **Final Yield:** Yields a verified, high-value dataset of **1,000 true Federer companies** ready for outreach.

---

### Week-by-Week Operational Execution Plan

[Week 1] ────────────────> [Week 2] ────────────────> [Week 3] ────────────────> [Week 4]
Top-of-Funnel Extraction   Automated LLM Scraping     LinkedIn API Auditing     Human-in-the-Loop QC
• Target: 4,000 names      • Target: 1,800 profiles   • Target: 1,100 verified  • Target: 1,000 final assets
• MCA & B2B Registries     • Web Scraping Processing  • ERP/Succession Checking • Manual Spot Checks
• Size & Location Filters  • Elimination of Traders   • Open Job Role Tracking  • Schema Delivery

### Expected Yield Performance Matrix

| Production Phase | Inputs Managed | Filters Applied | Target Outputs | Conversion Yield |
| :--- | :--- | :--- | :--- | :--- |
| **Week 1: Extraction** | 4,000 Companies | Location boundaries + Revenue brackets | 4,000 Names | 100% Top-of-Funnel |
| **Week 2: Gate Analysis** | 4,000 Names | Gate E1 (Producer check) + Website audit | 1,800 Profiles | 45% Yield |
| **Week 3: Deep Evaluation** | 1,800 Profiles | C7 Systems Validation + C6 Growth Metrics | 1,100 Profiles | 61% Yield |
| **Week 4: Final Verification** | 1,100 Profiles | Edge case resolution + Hook checking | 1,000 Targets | 91% Yield |
