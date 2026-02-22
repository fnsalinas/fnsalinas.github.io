---
description: Setup and verify Google Analytics 4 and Meta Pixel integration.
---

# Setup Analytics Workflow

This workflow guides the verification and installation of analytics tracking codes.

## Steps

1.  **Verify Init Scripts**
    - Check `index.html` for GA4 (`G-JL2WGMRMLP`) and Meta (`1175207061175553`) initialization scripts.
    - Ensure they are in the `<head>` tag.

2.  **Verify SPA Routing**
    - Check if there is a component (e.g., `src/components/MetaPixel.tsx` or similar) handling page views on route changes.
    - If missing, create one using the patterns in the `analytics-integration` skill.

3.  **Audit Key Conversions**
    - Identify key user actions:
        - Sign Up
        - Subscription/Purchase
        - Bank Connection (Lead)
    - Verify that `gtag` and `fbq` calls exist for these actions.

4.  **Validation**
    - Run the application locally.
    - Use the browser console to simulate events if needed.
    - Confirm network requests are being sent.
