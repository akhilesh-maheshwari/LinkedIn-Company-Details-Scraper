# 🏢 LinkedIn Company Details Scraper (No Cookies) ✅ Bulk

Extract complete company information from public LinkedIn company pages in bulk. Designed for B2B lead generation, account research, market analysis, CRM enrichment, and company database building — **no LinkedIn login cookies required**.

---

## 📋 Overview

Provide one or more LinkedIn company URLs and receive structured company data including:

- Company name, description & slogan
- Industry, organization type & company size
- LinkedIn follower count & employee count
- Website, headquarters & office locations
- Specialties, logo & cover image

---

## ⚙️ Input

| Field | Description | Example |
|-------|-------------|---------|
| `companies` | One or more LinkedIn company URLs | `https://www.linkedin.com/company/google` |
| `fileName` | Name used for the exported file | `my-companies` |

### Single Company

```json
{
  "companies": [
    "https://www.linkedin.com/company/google"
  ],
  "fileName": "my-companies"
}
```

### Bulk Input

```json
{
  "companies": [
    "https://www.linkedin.com/company/google",
    "https://www.linkedin.com/company/microsoft",
    "https://www.linkedin.com/company/salesforce"
  ],
  "fileName": "target-companies"
}
```

---

## 📌 Data Fields

### URL & Scrape Status

| Field | Description |
|-------|-------------|
| `input_url` | Original LinkedIn company URL submitted |
| `normalized_url` | Cleaned and standardized version of the URL |
| `correct_url` | Final LinkedIn company URL identified by the scraper |
| `data_status` | Whether company data was found |
| `url_status` | HTTP status returned for the company URL |
| `url_source` | Source used to resolve or validate the URL |

### Company Details

| Field | Description |
|-------|-------------|
| `company_id` | LinkedIn's numeric company identifier |
| `company_slug` | Public LinkedIn company page slug |
| `name` | Company name |
| `slogan` | Company tagline or slogan |
| `about` | LinkedIn About section text |
| `specialties` | Listed company specialties |
| `industries` | LinkedIn industry classification |
| `organization_type` | e.g., Public Company, Non-profit |
| `company_size` | LinkedIn company-size range |
| `type` | Company or organization type |
| `sphere` | Additional organization classification |
| `website` | Company website URL |
| `website_simplified` | Simplified domain value |
| `company_url` | Direct LinkedIn company page URL |
| `crunchbase_url` | Crunchbase company URL (when available) |
| `headquarters` | Primary headquarters location |
| `country_code` | Two-letter country code |
| `followers` | Number of LinkedIn page followers |
| `employees_in_linkedin` | LinkedIn members associated with the company |
| `founded` | Company founding year (when available) |
| `description` | Company description |
| `is_school` | Whether the page represents a school |

### Locations & Media

| Field | Description |
|-------|-------------|
| `locations` | Detailed list including street, address, locality, primary status & directions URL |
| `formatted_locations` | Simplified list of company addresses |
| `logo` | Company logo URL |
| `image` | Company cover image URL |

### Processing Metadata

| Field | Description |
|-------|-------------|
| `request_id` | Identifier for the main scraping request |
| `child_request_id` | Identifier for the individual company request |
| `order_id` | Internal identifier for the run |
| `processed_at` | Date and time the record was processed |

> **Note:** Fields may be empty when the information is not publicly available on the LinkedIn company page.

---

## 📊 Sample Output

```json
{
  "input_url": "https://www.linkedin.com/company/google",
  "normalized_url": "https://www.linkedin.com/company/google",
  "correct_url": "https://www.linkedin.com/company/google",
  "data_status": "found",
  "url_status": 200,
  "company_id": "1441",
  "company_slug": "google",
  "name": "Google",
  "about": "A problem isn't truly solved until it's solved for all...",
  "specialties": "search, ads, mobile, android, online video, machine learning, AI...",
  "industries": "Software Development",
  "organization_type": "Public Company",
  "company_size": "10,001+ employees",
  "website": "https://goo.gle/3DLEokh",
  "headquarters": "Mountain View, CA",
  "country_code": "US",
  "followers": 42430676,
  "employees_in_linkedin": 297958,
  "locations": [
    {
      "street": "1600 Amphitheatre Parkway",
      "address": "1600 Amphitheatre Parkway, Mountain View, CA 94043, US",
      "locality": "Mountain View, CA 94043, US",
      "is_primary": true
    }
  ],
  "logo": "https://media.licdn.com/dms/image/.../google_logo",
  "image": "https://media.licdn.com/dms/image/.../google_cover",
  "is_school": false,
  "processed_at": "2026-09-30T07:52:54.094Z"
}
```

---

## 📁 How to Use

1. Create a free [Apify](https://apify.com) account.
2. Open the **LinkedIn Company Details Scraper** actor.
3. Add one or more LinkedIn company page URLs to the `companies` list.
4. Enter a name in the `fileName` field.
5. Run the actor.
6. Download the structured output in **JSON**, **CSV**, or **Excel** format.

---

## ✅ Common Use Cases

- Enrich company and account lists for sales outreach
- Build targeted B2B company databases
- Collect LinkedIn follower and employee counts
- Research company size, industry, and headquarters
- Find company websites and office locations
- Enrich CRM company records (Salesforce, HubSpot, etc.)
- Analyze competitors and target accounts
- Collect company logos and LinkedIn page images

---

## ⚠️ Data Availability

This scraper collects **publicly available** company information only. Some fields may be blank when they are not displayed on a company's LinkedIn page. Values such as follower counts, employee counts, and descriptions can change over time.
