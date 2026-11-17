# A/B Test Plan: Hawkeye Grind Guide Homepage CTA

## 1. Page and Tested Element
* **Page Tested:** Homepage (`index.html` vs. `index-b.html`)
* **Element Changed:** The primary Call-to-Action (CTA) button text inside the main hero introduction section.
* **Version A (Control):** The existing CTA button text reads "Find Your Perfect Iowa City Study Environment".
* **Version B (Variant):** The updated CTA button text reads "Browse Verified Quiet Cafes".
* **SEO Protection:** Variant B (`index-b.html`) is shielded from indexing via `<meta name="robots" content="noindex, nofollow">` and exclusion from the sitemap.

## 2. Hypothesis and Reasoning
* **Hypothesis:** Changing the homepage hero CTA text from a broad prompt ("Find Your Perfect Iowa City Study Environment") to a specific, benefit-driven prompt ("Browse Verified Quiet Cafes") will significantly increase the proportion of AI simulated visitors who state they would click through to explore the directory.
* **Reasoning:** User persona research shows that students visiting study guides under time constraints are specifically trying to solve a pain point around ambient noise and finding distraction-free zones. A specific prompt sets immediate expectations and reduces cognitive friction compared to a generic call to action, leading to higher engagement.

## 3. Visitor Persona, Prompt, and Assignment Method
* **AI Model:** GPT-4o (maintained consistently across all 100 trials).
* **Visitor Persona Prompt (Calibrated for Realistic Variance & Selective Friction):**
  > "You are a senior undergraduate student at the University of Iowa looking for an off-campus coffee shop to study for 2 hours this afternoon. You are tired of wasting time walking to crowded cafes with no outlets, so you will only click on a directory if the main call-to-action button convinces you it has specific, reliable data rather than generic fluff. Read the following homepage text from Hawkeye Grind Guide and answer this single question: Would you click the primary button to explore this directory further? Answer strictly 'Yes' or 'No', followed by one single sentence of reasoning."
* **Assignment Method:** Pre-generated pseudo-random sequence (50 Version A trials and 50 Version B trials) locked via spreadsheet paste-values to ensure a strict 50/50 split and prevent mid-test sequence shuffling.

## 4. Primary Outcome and Measurement
* **Primary Outcome:** Binary click-intent decision ("Yes" vs. "No") recorded in response to the persona prompt.
* **Measurement Scale:** Count of "Yes" responses divided by total trials per version ($n = 50$ each) to calculate the conversion intent percentage.

## 5. Sample Size and Timeline
* **Target Sample Size:** 50 trials for Version A and 50 trials for Version B, totaling 100 independent trials.
* **Execution Timeline:** Data collection and logging finalized by November 18, 2026.

## 6. Comparison and Success Criteria
* **Statistical Comparison:** A two-proportion $z$-test will be conducted on completion to compare conversion intent rates between Version A and Version B ($p_A$ vs. $p_B$).
* **Success Criteria:** Version B will be considered supportive of the hypothesis if it achieves a statistically higher "Yes" response rate at a significance level of $p < 0.10$, backed by qualitative reasoning patterns indicating stronger user clarity regarding noise and study suitability.
