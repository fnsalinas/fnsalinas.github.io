---
name: analytics-integration
description: Implementation guide for Google Analytics 4 and Meta Pixel integration.
---

# Analytics Integration Skill

This skill provides the standard implementation details for tracking in the Finly application.

## Configuration Constants

| Platform | ID | Variable Name |
| :--- | :--- | :--- |
| **Google Analytics 4** | `G-JL2WGMRMLP` | `GA_MEASUREMENT_ID` |
| **Meta Pixel** | `1175207061175553` | `FB_PIXEL_ID` |

## Implementation Patterns

### 1. Initialization (index.html)

The head of `index.html` should contain the base scripts.

**GA4:**
```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-JL2WGMRMLP"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-JL2WGMRMLP');
</script>
```

**Meta Pixel:**
```html
<!-- Meta Pixel Code -->
<script>
!function(f,b,e,v,n,t,s)
{if(f.fbq)return;n=f.fbq=function(){n.callMethod?
n.callMethod.apply(n,arguments):n.queue.push(arguments)};
if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
n.queue=[];t=b.createElement(e);t.async=!0;
t.src=v;s=b.getElementsByTagName(e)[0];
s.parentNode.insertBefore(t,s)}(window, document,'script',
'https://connect.facebook.net/en_US/fbevents.js');
fbq('init', '1175207061175553');
fbq('track', 'PageView');
</script>
<noscript><img height="1" width="1" style="display:none"
src="https://www.facebook.com/tr?id=1175207061175553&ev=PageView&noscript=1"
/></noscript>
<!-- End Meta Pixel Code -->
```

### 2. React Component Tracking (SPA)

For a Single Page Application, extensive use of `useEffect` or a specialized hook/component is recommended to track page views on route changes.

**Example `MetaPixel.tsx`:**
```tsx
import React, { useEffect } from 'react';
import { useLocation } from 'react-router-dom';

const MetaPixel: React.FC = () => {
  const location = useLocation();

  useEffect(() => {
    import('react-facebook-pixel')
      .then((x) => x.default)
      .then((ReactPixel) => {
        ReactPixel.init('1175207061175553');
        ReactPixel.pageView();
      });
  }, [location.pathname]);

  return null;
};
```

### 3. Event Tracking Reference

**Common Events to Track:**

| Event Type | GA4 Event Name | Meta Event Name | Trigger |
| :--- | :--- | :--- | :--- |
| **Page View** | `page_view` (auto) | `PageView` | Route change |
| **Sign Up** | `sign_up` | `CompleteRegistration` | User creates account |
| **Login** | `login` | `Contact` (or Custom) | User logs in |
| **View Connect** | `view_bank_connect` | `ViewContent` | User views bank connection screen |
| **Connect Bank** | `connect_bank` | `Lead` | User successfully links bank |
| **Subscribe** | `purchase` | `Subscribe` | User buys a plan |

**Code Examples:**

*   **GA4 Event:**
    ```javascript
    gtag('event', 'sign_up', {
      method: 'Google'
    });
    ```

*   **Meta Event:**
    ```javascript
    fbq('track', 'CompleteRegistration', {
      content_name: 'Signup Flow', 
      status: true
    });
    ```

## Verification Checklist
- [ ] Verify `G-JL2WGMRMLP` is present in `gtag('config')`.
- [ ] Verify `1175207061175553` is present in `fbq('init')`.
- [ ] Check Network tab for requests to `google-analytics.com` and `facebook.com/tr`.
- [ ] Ensure no PII is passed in params.
