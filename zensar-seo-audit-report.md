# SEO Audit Report: zensar.com

**Audit Date**: May 10, 2026  
**Scope**: Technical SEO (Full Site)  
**Site Type**: Global B2B IT Services/Consulting Company  
**Access**: Visual audit (no Search Console data)

---

## Important Context Clarification

⚠️ **Site Type Mismatch**: You indicated this is a "Local Business" targeting "footfall enhancement," but **zensar.com is a global B2B IT services and consulting company**, not a local business. Local business schema and footfall strategies don't apply here. SEO recommendations below focus on B2B SaaS/Services companies instead.

---

## Executive Summary

**Overall Health**: **GOOD** ✓

Zensar's site demonstrates solid technical SEO fundamentals with proper crawlability, indexation setup, and on-page optimization. The site is well-structured, mobile-responsive, and implements analytics tracking. However, several optimization opportunities exist, particularly around resource loading and schema markup completeness.

**Top Priorities**:
1. Resolve 401 resource loading errors
2. Expand and verify schema markup (currently minimal)
3. Test and optimize Core Web Vitals
4. Address permissions policy violations

---

## Technical SEO Findings

### 1. Crawlability & Indexation ✓

| Finding | Status | Evidence | Priority |
|---------|--------|----------|----------|
| **Robots.txt** | ✓ Good | Present and properly configured; allows all crawlers; references sitemap | Low |
| **XML Sitemap** | ✓ Good | Accessible at `/sitemap.xml`; uses correct schema; updated regularly (lastmod: 2026-05-10) | Low |
| **Site Architecture** | ✓ Good | Clear hierarchy; 127 internal links on homepage; important pages linked within 2 clicks | Low |
| **Canonical Tags** | ✓ Good | Self-referencing canonicals on tested pages; consistent across domain | Low |

**Verdict**: Crawlability is well-configured. No blocks preventing Googlebot access.

---

### 2. URL Structure ✓

| Finding | Status | Evidence |
|---------|--------|----------|
| **Readability** | ✓ Good | Descriptive, keyword-rich URLs (e.g., `/tech-services/artificial-intelligence`) |
| **Consistency** | ✓ Good | Lowercase, hyphenated, no unnecessary parameters |
| **HTTPS** | ✓ Good | Full site uses HTTPS with valid SSL certificate |

---

### 3. On-Page SEO ✓

**Homepage ("Digital Transformation...") Page:**
- ✓ **Title Tag**: 56 characters - optimal length, keyword-focused, includes brand name
- ✓ **Meta Description**: 155 characters - compelling, includes value proposition
- ✓ **H1**: Single, descriptive "Experiences, Thoughtfully Reimagined"
- ✓ **Heading Hierarchy**: Proper structure (1 H1 → 8 H2 → 6 H3) on service pages tested

**AI Services Page Example:**
- ✓ **Title**: "AI Services | Artificial Intelligence Solutions" (48 chars)
- ✓ **Meta Description**: Descriptive with keywords and value promise
- ✓ **H1**: Present and unique "Artificial Intelligence"
- ✓ **Structure**: Logical hierarchy maintained

**Issue**: Titles truncate at ~60 characters in SERPs; some are at the limit. No immediate action needed but room to optimize for CTR.

---

### 4. Schema Markup & Structured Data ⚠️ NEEDS REVIEW

| Finding | Status | Evidence | Fix |
|---------|--------|----------|-----|
| **Schema Present** | ✓ Yes | 1 JSON-LD schema detected with `@graph` structure | Good - complex sites benefit from Graph format |
| **Schema Type** | ⚠️ Unverified | Schema detected but specific type unclear (marked as "unknown"); likely Organization or WebSite | **REVIEW**: Use Google Rich Results Test or Screaming Frog to verify schema includes: Organization details (name, logo, contact), WebSite (searchAction), possibly BreadcrumbList |
| **LocalBusiness Schema** | ✓ Not Present | Correctly absent (site is global B2B, not local) | No action needed |

**Priority: MEDIUM** — Verify schema markup is complete and includes:
- `Organization` with logo, contact info, social profiles
- `WebSite` with `potentialAction` for search
- `BreadcrumbList` on product/service pages (detected on navigation)

**Action**: Use [Google Rich Results Test](https://search.google.com/test/rich-results) and enter https://www.zensar.com/ to validate schema is proper and no errors present.

---

### 5. Mobile-Friendliness ✓

| Finding | Status | Evidence |
|---------|--------|----------|
| **Viewport Meta Tag** | ✓ Present | `width=device-width, initial-scale=1` configured |
| **Responsive Design** | ✓ Good | No horizontal scroll; layout adapts to screen size |
| **Mobile-First Indexing** | ✓ Ready | Same content served to all devices (no separate m. domain) |

---

### 6. Core Web Vitals & Performance ⚠️ NEEDS TESTING

**Status**: Not tested in this audit (requires Google PageSpeed Insights or Chrome DevTools)

**What to check**:
- **LCP** (Largest Contentful Paint): Target < 2.5s
- **INP** (Interaction to Next Paint): Target < 200ms
- **CLS** (Cumulative Layout Shift): Target < 0.1

**Action**: Run [Google PageSpeed Insights](https://pagespeed.web.dev/) on these key pages:
- Homepage: https://www.zensar.com/
- AI Services: https://www.zensar.com/tech-services/artificial-intelligence
- Contact: https://www.zensar.com/contact-us

---

### 7. Resource Loading Errors ⚠️ ISSUE FOUND

**Issue**: Console shows multiple 401 errors and permissions policy violations

```
✗ Failed to load resource: the server responded with a status of 401 (3x)
✗ Potential permissions policy violation: autoplay (3x)
✗ Potential permissions policy violation: cross-origin-isolated (3x)
✗ Potential permissions policy violation: keyboard-map (3x)
```

**Impact**: **LOW** — Errors are not blocking page functionality; appear to be related to video player or embedded content permissions

**Recommendation**: 
1. Investigate which resources are returning 401 — likely API calls or protected resources
2. Review Permissions-Policy header to ensure it allows necessary features
3. Suppress autoplay if not critical to UX

---

### 8. Security & HTTPS ✓

| Finding | Status |
|---------|--------|
| **HTTPS** | ✓ Yes, site-wide |
| **SSL Certificate** | ✓ Valid |
| **Mixed Content** | ✓ None detected |

---

### 9. Analytics & Tracking ✓

| Finding | Status |
|---------|--------|
| **Google Analytics** | ✓ Implemented (gtag detected) |
| **Search Console** | ✓ Verified (meta tag present: `google-site-verification`) |

---

### 10. Open Graph & Social Meta Tags ✓

| Finding | Status |
|---------|--------|
| **OG:title** | ✓ Present |
| **OG:description** | ✓ Present |
| **OG:url** | ✓ Present |
| **Twitter Card** | ✓ Configured |

---

## Common Issues by Site Type: B2B Services

**Not applicable to this site (not an issue):**
- ✓ No thin content detected on service pages
- ✓ No keyword cannibalization observed (each page has distinct focus)
- ✓ Service page structure follows best practices

---

## Prioritized Action Plan

### Priority 1: Critical (Do immediately)
None identified — no crawlability or indexation blockers found.

### Priority 2: High Impact (1-2 weeks)

1. **Verify & expand schema markup** (if not already comprehensive)
   - Use Rich Results Test to validate
   - Ensure Organization + WebSite + BreadcrumbList schemas are present
   - **Impact**: Improves Rich Results eligibility, knowledge panels

2. **Test Core Web Vitals performance**
   - Run PageSpeed Insights on 5-10 key pages
   - If any page exceeds thresholds, identify bottlenecks (LCP, CLS, INP)
   - **Impact**: Mobile rankings, user experience

3. **Resolve 401 resource errors**
   - Identify source of 401 failures
   - Ensure protected resources aren't critical to SEO rendering
   - **Impact**: Cleaner crawl logs, better monitoring

### Priority 3: Quick Wins (1 week)

1. **Optimize meta descriptions for CTR**
   - Review descriptions under 150 characters on key pages
   - Add compelling value propositions where generic
   - Target: 150-160 characters per page
   - **Impact**: Higher CTR from SERP

2. **Audit internal linking**
   - Ensure key service pages (Application Services, AI, Cloud, etc.) are linked from homepage and main nav
   - Review anchor text for optimization opportunities
   - **Impact**: Better link equity distribution

---

## Performance Recommendations (Not Technical SEO, but Related)

### Image Optimization
- **Current**: 77 images on homepage
- **Issue**: Likely some unoptimized for web
- **Action**: 
  - Convert to WebP format where possible
  - Implement lazy loading (appears partially done)
  - Compress images to <100KB each
  - **Tools**: TinyPNG, ImageOptim, WebP converters

### Video Content
- **Status**: Videos embedded (YouTube/Vimeo)
- **Good**: Offloads hosting; videos improve engagement
- **Check**: Ensure videos have transcripts for accessibility + SEO

---

## Data Summary

| Metric | Value |
|--------|-------|
| **Total Sitemap URLs** | ~100+ (contains case studies, white papers, insights) |
| **Internal Links** | 127 on homepage |
| **External Links** | 22 (to careers portal, partner sites) |
| **Total Images** | 77 on homepage |
| **Schema Schemas** | 1 (JSON-LD @graph) |
| **Meta Tags** | All critical ones present (viewport, description, OG, Twitter) |
| **Heading Levels** | Proper 1→2→3 hierarchy on tested pages |

---

## Related Skills / Next Steps

- **📊 Analytics Tracking**: If you want to set up conversion tracking for specific user journeys (webinar signups, demo requests, case study downloads), see the analytics-tracking skill

- **🎯 Page CRO**: If you want to optimize specific pages for lead generation or demo requests, see page-cro skill

- **📝 Schema Markup**: For detailed schema implementation (Organization, FAQPage, Article, etc.), see schema-markup skill

- **🔍 AI-SEO**: If you want to optimize this content for AI search engines (ChatGPT, Perplexity, Claude), see ai-seo skill

---

## Audit Conclusion

**Zensar's website is technically sound for SEO.** No critical issues block visibility or indexing. The site has:
- ✓ Clean crawlability and indexation
- ✓ Proper on-page optimization
- ✓ Mobile-responsive design
- ✓ Analytics & tracking set up
- ✓ Secure HTTPS throughout

**Next phase**: Focus on performance testing (Core Web Vitals), schema markup verification, and on-page content optimization to drive higher rankings for target keywords in your industry verticals.

---

**Report Generated**: May 10, 2026  
**Auditor**: GitHub Copilot  
**Site**: https://www.zensar.com/
