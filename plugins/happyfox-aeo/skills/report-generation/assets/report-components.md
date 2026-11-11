# HappyFox AEO report components

Use these illustrative components with the selected report template. Wrap each snippet in its `scope` class (`hf-op` or `hf-lf`) and include the scoped CSS below. Use Inter throughout the report. If unavailable, use a system sans-serif fallback. Replace all fictional sample data and follow the report guide’s evidence rules. Component selection is optional and should support the agreed story.

## Component catalog

```json
{
  "name": "HappyFox AEO report components",
  "version": "1.0.0",
  "generated": "2026-10-21T04:08:59.757Z",
  "stylesheet": "#scoped-stylesheet",
  "font": "Inter 400/500/600/700",
  "usage": "Wrap snippet html in an element with class equal to its scope (hf-lf or hf-op), include the CSS from the Scoped stylesheet section.",
  "tokens": [
    {
      "name": "--ink",
      "value": "#0a0a0a",
      "use": "Primary text, dark panels"
    },
    {
      "name": "--ink-prose",
      "value": "#3f3f3f",
      "use": "Body prose"
    },
    {
      "name": "--ink2",
      "value": "#5c5c5c",
      "use": "Secondary text, labels"
    },
    {
      "name": "--ink3",
      "value": "#a3a3a3",
      "use": "Muted, ordinals, secondary bars"
    },
    {
      "name": "--bd-2",
      "value": "#e7e7e5",
      "use": "Hairlines, card borders"
    },
    {
      "name": "--s-raised",
      "value": "#f8f8f7",
      "use": "Raised cards"
    },
    {
      "name": "--s-page",
      "value": "#edeae5",
      "use": "Page background"
    },
    {
      "name": "--hf-orange",
      "value": "#ff5a00",
      "use": "Accent: logo, bars, kicker dots, section numbers"
    },
    {
      "name": "--hf-orange-dark",
      "value": "#c74600",
      "use": "Accent deep"
    },
    {
      "name": "--hf-orange-tint",
      "value": "#fff1e8",
      "use": "Highlighted rows"
    },
    {
      "name": "--green",
      "value": "#047857",
      "use": "Positive deltas"
    },
    {
      "name": "--risk",
      "value": "#b42318",
      "use": "Risk / absent results"
    }
  ],
  "components": [
    {
      "id": "hf-logo",
      "title": "HappyFox AEO logo lockup",
      "type": "Branding / Logo",
      "scope": "hf-lf",
      "source": [
        "long-form",
        "one-page"
      ],
      "tags": [
        "branding",
        "logo",
        "header",
        "shared"
      ],
      "usage": "Publisher mark placed at the right of every masthead. Wordmark inherits currentColor for text; fox mark stays #ff5a00.",
      "html": "<div class=\"publisher\"><span class=\"hf-publisher\"><svg class=\"hf-wordmark\" viewBox=\"0 0 2046 389\" fill=\"none\" role=\"img\" aria-label=\"HappyFox\"><g clip-path=\"url(#clip0_9381_2616)\"><path fill=\"currentColor\" d=\"m1990.08 305.059-57.58-84.695-8.34-7.509-77.61-108.059h55.49l51.32 74.264 7.93 7.093 83.86 118.906zm-147.28 0 80.94-112.231 26.7 32.96-54.24 79.271zm122.66-93.039-27.12-32.543 50.07-74.681h52.98zM1748.81 309.235c-19.47 0-37.14-4.59-52.99-13.768-15.86-9.457-28.51-22.113-37.97-37.967q-13.77-23.78-13.77-52.987 0-29.205 13.77-52.569c9.46-15.576 22.11-27.953 37.97-37.132 15.85-9.457 33.52-14.185 52.99-14.185q29.61 0 53.4 13.768c15.85 9.179 28.37 21.695 37.55 37.549 9.46 15.576 14.18 33.099 14.18 52.569s-4.72 37.133-14.18 52.987c-9.18 15.854-21.7 28.51-37.55 37.967q-23.79 13.768-53.4 13.768m0-44.225q17.1 0 30.03-7.51c8.91-5.285 15.72-12.517 20.45-21.695 5-9.179 7.51-19.609 7.51-31.292s-2.51-21.973-7.51-30.874c-5.01-8.9-11.82-15.854-20.45-20.86q-12.93-7.927-30.03-7.927c-11.13 0-21.14 2.642-30.04 7.927-8.63 5.006-15.44 11.96-20.45 20.86-4.73 8.901-7.09 19.192-7.09 30.874 0 11.683 2.36 22.113 7.09 31.292 5.01 9.178 11.82 16.41 20.45 21.695 8.9 5.006 18.91 7.51 30.04 7.51M1545.77 305.062V78.514c0-15.298 3.34-28.788 10.01-40.47 6.96-11.682 16.41-20.861 28.37-27.536 12.24-6.676 26.29-10.014 42.14-10.014q18.36 0 31.29 6.259c8.63 4.172 16.69 10.152 24.2 17.94l-29.62 29.622c-3.34-3.337-6.95-5.98-10.85-7.927-3.89-1.947-8.9-2.92-15.02-2.92-11.12 0-19.75 3.06-25.87 9.178q-8.76 8.762-8.76 25.45v226.966zm9.97-158.542v-41.722h96.42v41.722zM1410.55 307.145l-85.53-202.349h50.49l58.41 148.529h-14.61l61.75-148.529h50.9l-93.04 202.349zm-59.66 81.358 62.17-128.086 25.86 46.728-37.13 81.358zM1233.45 309.235c-15.29 0-28.92-3.199-40.88-9.596-11.96-6.676-21.42-15.715-28.37-27.119q-10.02-17.106-10.02-38.801v-57.576c0-14.464 3.48-27.397 10.43-38.801 6.96-11.404 16.41-20.305 28.38-26.702 11.96-6.676 25.45-10.013 40.46-10.013 18.08 0 34.36 4.728 48.82 14.185 14.74 9.179 26.28 21.695 34.63 37.549q12.93 23.365 12.93 52.987 0 29.205-12.93 52.986c-8.35 15.576-19.89 27.954-34.63 37.133-14.46 9.178-30.74 13.768-48.82 13.768m-7.5-43.391c11.12 0 20.86-2.503 29.2-7.51 8.62-5.284 15.3-12.516 20.03-21.695 5-9.179 7.51-19.748 7.51-31.708s-2.51-22.53-7.51-31.709c-4.73-9.178-11.41-16.271-20.03-21.278-8.34-5.284-18.08-7.927-29.2-7.927-11.13 0-21 2.643-29.63 7.927-8.62 5.007-15.3 12.1-20.02 21.278-4.73 9.179-7.1 19.749-7.1 31.709s2.37 22.529 7.1 31.708c4.72 9.179 11.4 16.411 20.02 21.695 8.63 5.007 18.5 7.51 29.63 7.51m-99.72 122.662V104.799h45.89v53.821l-7.92 48.814 7.92 48.397v132.675zM1010.77 309.235q-22.952 0-40.892-9.596-17.94-10.013-28.37-27.119-10.014-17.106-10.013-38.801v-57.576q0-21.695 10.43-38.801t28.371-26.702q17.939-10.014 40.474-10.013c18.07 0 34.35 4.728 48.81 14.185 14.74 9.179 26.28 21.695 34.63 37.549q12.93 23.365 12.93 52.987 0 29.205-12.93 52.986c-8.35 15.576-19.89 27.954-34.63 37.133-14.46 9.178-30.74 13.768-48.81 13.768m-7.51-43.391c11.12 0 20.86-2.503 29.2-7.51 8.62-5.284 15.3-12.516 20.03-21.695 5-9.179 7.51-19.748 7.51-31.708s-2.51-22.53-7.51-31.709c-4.73-9.178-11.41-16.271-20.03-21.278-8.34-5.284-18.08-7.927-29.2-7.927q-16.694 0-29.627 7.927-12.933 7.51-20.026 21.278-7.093 13.769-7.093 31.709t7.093 31.708q7.092 13.769 20.026 21.695 12.933 7.51 29.627 7.51m-99.719 122.662V104.799h45.894v53.821l-7.927 48.814 7.927 48.397v132.675zM764.695 309.235q-27.119 0-49.231-13.768-21.696-13.769-34.629-37.133-12.517-23.781-12.517-52.986 0-29.622 12.517-52.987 12.933-23.78 34.629-37.549 22.112-14.185 49.231-14.185 22.947 0 40.47 10.013 17.94 9.596 28.371 26.702t10.43 38.801v57.576q0 21.695-10.43 38.801-10.013 17.106-27.954 27.119-17.94 9.596-40.887 9.596m7.51-43.391q25.45 0 40.887-17.106 15.855-17.106 15.854-43.807 0-17.94-7.092-31.709-7.093-13.767-20.027-21.278-12.516-7.926-29.622-7.927-16.689 0-29.622 7.927-12.517 7.51-20.027 21.278-7.092 13.769-7.092 31.709t7.092 31.708q7.51 13.769 20.027 21.695 12.933 7.51 29.622 7.51m53.821 39.219v-53.821l7.927-48.815-7.927-48.397v-49.231h45.894v200.264zM607.629 305.059V189.49q0-20.027-12.933-32.96-12.517-12.934-32.543-12.934-13.351 0-23.782 5.841T522.1 165.709q-5.841 10.43-5.841 23.781l-17.94-10.013q0-22.947 10.013-40.47 10.013-17.94 27.536-27.954 17.94-10.43 40.053-10.43 22.53 0 40.053 10.013t27.536 27.954q10.013 17.523 10.013 40.887v125.582zm-137.264 0V4.663h45.894V305.06z\"></path><g fill=\"#ff5a00\" clip-path=\"url(#clip1_9381_2616)\"><path d=\"M50.236 157.311a41.35 41.35 0 0 0 22.232-6.472l80.282-50.936-112.74-82.16C23.36 5.59-.008 17.498-.008 38.05v86.259l20.948 20.849c7.855 7.806 18.23 12.104 29.346 12.104z\"></path><path d=\"m8.786 238.662 115.359 99.056 39.128 33.595c9.14 7.855 22.528 8.102 31.965.642l164.318-129.587c6.027-4.793 9.585-12.055 9.585-19.762V36.253c0-20.206-22.677-32.211-39.376-20.8L178.49 118.71l-90.163 57.21c-11.709 7.46-24.95 11.066-38.09 11.066-18.33 0-36.51-7.064-50.245-20.749v53.356c0 7.361 3.211 14.327 8.794 19.07\"></path></g></g><defs><clipPath id=\"clip0_9381_2616\"><path fill=\"#fff\" d=\"M0 0h2045.14v389H0z\"></path></clipPath><clipPath id=\"clip1_9381_2616\"><path fill=\"#fff\" d=\"M-.008 11.031H369.14v366.332H-.008z\"></path></clipPath></defs></svg><span class=\"aeo\">AEO</span></span></div>"
    },
    {
      "id": "lf-review-bar",
      "title": "Review / section navigation bar",
      "type": "Navigation / Toolbar",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "navigation",
        "toolbar",
        "interactive",
        "screen-only"
      ],
      "usage": "Sticky top bar for multi-section reports: section jump select, prev/next, counter, show-all and print. Hidden in print.",
      "html": "<nav class=\"reviewbar\" aria-label=\"Report navigation\">\n  <span class=\"label\">Template preview</span>\n  <select id=\"section\" aria-label=\"Jump to report section\">\n    <option value=\"0\">01 · The 60-second read</option><option value=\"1\">02 · Segment opportunities</option><option value=\"2\">03 · Competitive landscape</option><option value=\"3\">04 · Brand perception &amp; accuracy</option><option value=\"4\">05 · Citation &amp; content opportunities</option><option value=\"5\">06 · Engines &amp; change over time</option><option value=\"6\">07 · Prioritized action plan</option><option value=\"7\">08 · Evidence &amp; methodology</option>\n  </select>\n  <button id=\"previous\" aria-label=\"Previous section\">←</button><button id=\"next\" aria-label=\"Next section\">→</button>\n  <span id=\"counter\" class=\"counter\" aria-live=\"polite\">1 of 8</span><span class=\"spacer\"></span>\n  <button id=\"all\" aria-pressed=\"false\">All sections</button><button id=\"print\" class=\"printbutton\">Print report</button>\n</nav>"
    },
    {
      "id": "lf-intro-strip",
      "title": "Sample disclaimer strip",
      "type": "Text / Meta strip",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "meta",
        "disclaimer",
        "screen-only"
      ],
      "usage": "Small two-sided line above the report: bold disclaimer left, date/context right.",
      "html": "<div class=\"intro\"><strong>Fictional sample · All brands, answers, sources, and numbers are invented.</strong><span>Illustrative reference · October 6, 2026</span></div>"
    },
    {
      "id": "lf-masthead",
      "title": "Sheet masthead",
      "type": "Layout / Header",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "header",
        "branding",
        "layout"
      ],
      "usage": "Top of each report sheet: client brand mark + name, section tag, HappyFox AEO logo. Bottom hairline separates it from content.",
      "html": "<header class=\"masthead\"><div class=\"brand\"><span class=\"brandmark\" aria-hidden=\"true\">N</span>Northstar Desk</div><span class=\"sectiontag\">The 60-second read</span><div class=\"publisher\"><span class=\"hf-publisher\"><svg class=\"hf-wordmark\" viewBox=\"0 0 2046 389\" fill=\"none\" role=\"img\" aria-label=\"HappyFox\"><g clip-path=\"url(#clip0_9381_2616)\"><path fill=\"currentColor\" d=\"m1990.08 305.059-57.58-84.695-8.34-7.509-77.61-108.059h55.49l51.32 74.264 7.93 7.093 83.86 118.906zm-147.28 0 80.94-112.231 26.7 32.96-54.24 79.271zm122.66-93.039-27.12-32.543 50.07-74.681h52.98zM1748.81 309.235c-19.47 0-37.14-4.59-52.99-13.768-15.86-9.457-28.51-22.113-37.97-37.967q-13.77-23.78-13.77-52.987 0-29.205 13.77-52.569c9.46-15.576 22.11-27.953 37.97-37.132 15.85-9.457 33.52-14.185 52.99-14.185q29.61 0 53.4 13.768c15.85 9.179 28.37 21.695 37.55 37.549 9.46 15.576 14.18 33.099 14.18 52.569s-4.72 37.133-14.18 52.987c-9.18 15.854-21.7 28.51-37.55 37.967q-23.79 13.768-53.4 13.768m0-44.225q17.1 0 30.03-7.51c8.91-5.285 15.72-12.517 20.45-21.695 5-9.179 7.51-19.609 7.51-31.292s-2.51-21.973-7.51-30.874c-5.01-8.9-11.82-15.854-20.45-20.86q-12.93-7.927-30.03-7.927c-11.13 0-21.14 2.642-30.04 7.927-8.63 5.006-15.44 11.96-20.45 20.86-4.73 8.901-7.09 19.192-7.09 30.874 0 11.683 2.36 22.113 7.09 31.292 5.01 9.178 11.82 16.41 20.45 21.695 8.9 5.006 18.91 7.51 30.04 7.51M1545.77 305.062V78.514c0-15.298 3.34-28.788 10.01-40.47 6.96-11.682 16.41-20.861 28.37-27.536 12.24-6.676 26.29-10.014 42.14-10.014q18.36 0 31.29 6.259c8.63 4.172 16.69 10.152 24.2 17.94l-29.62 29.622c-3.34-3.337-6.95-5.98-10.85-7.927-3.89-1.947-8.9-2.92-15.02-2.92-11.12 0-19.75 3.06-25.87 9.178q-8.76 8.762-8.76 25.45v226.966zm9.97-158.542v-41.722h96.42v41.722zM1410.55 307.145l-85.53-202.349h50.49l58.41 148.529h-14.61l61.75-148.529h50.9l-93.04 202.349zm-59.66 81.358 62.17-128.086 25.86 46.728-37.13 81.358zM1233.45 309.235c-15.29 0-28.92-3.199-40.88-9.596-11.96-6.676-21.42-15.715-28.37-27.119q-10.02-17.106-10.02-38.801v-57.576c0-14.464 3.48-27.397 10.43-38.801 6.96-11.404 16.41-20.305 28.38-26.702 11.96-6.676 25.45-10.013 40.46-10.013 18.08 0 34.36 4.728 48.82 14.185 14.74 9.179 26.28 21.695 34.63 37.549q12.93 23.365 12.93 52.987 0 29.205-12.93 52.986c-8.35 15.576-19.89 27.954-34.63 37.133-14.46 9.178-30.74 13.768-48.82 13.768m-7.5-43.391c11.12 0 20.86-2.503 29.2-7.51 8.62-5.284 15.3-12.516 20.03-21.695 5-9.179 7.51-19.748 7.51-31.708s-2.51-22.53-7.51-31.709c-4.73-9.178-11.41-16.271-20.03-21.278-8.34-5.284-18.08-7.927-29.2-7.927-11.13 0-21 2.643-29.63 7.927-8.62 5.007-15.3 12.1-20.02 21.278-4.73 9.179-7.1 19.749-7.1 31.709s2.37 22.529 7.1 31.708c4.72 9.179 11.4 16.411 20.02 21.695 8.63 5.007 18.5 7.51 29.63 7.51m-99.72 122.662V104.799h45.89v53.821l-7.92 48.814 7.92 48.397v132.675zM1010.77 309.235q-22.952 0-40.892-9.596-17.94-10.013-28.37-27.119-10.014-17.106-10.013-38.801v-57.576q0-21.695 10.43-38.801t28.371-26.702q17.939-10.014 40.474-10.013c18.07 0 34.35 4.728 48.81 14.185 14.74 9.179 26.28 21.695 34.63 37.549q12.93 23.365 12.93 52.987 0 29.205-12.93 52.986c-8.35 15.576-19.89 27.954-34.63 37.133-14.46 9.178-30.74 13.768-48.81 13.768m-7.51-43.391c11.12 0 20.86-2.503 29.2-7.51 8.62-5.284 15.3-12.516 20.03-21.695 5-9.179 7.51-19.748 7.51-31.708s-2.51-22.53-7.51-31.709c-4.73-9.178-11.41-16.271-20.03-21.278-8.34-5.284-18.08-7.927-29.2-7.927q-16.694 0-29.627 7.927-12.933 7.51-20.026 21.278-7.093 13.769-7.093 31.709t7.093 31.708q7.092 13.769 20.026 21.695 12.933 7.51 29.627 7.51m-99.719 122.662V104.799h45.894v53.821l-7.927 48.814 7.927 48.397v132.675zM764.695 309.235q-27.119 0-49.231-13.768-21.696-13.769-34.629-37.133-12.517-23.781-12.517-52.986 0-29.622 12.517-52.987 12.933-23.78 34.629-37.549 22.112-14.185 49.231-14.185 22.947 0 40.47 10.013 17.94 9.596 28.371 26.702t10.43 38.801v57.576q0 21.695-10.43 38.801-10.013 17.106-27.954 27.119-17.94 9.596-40.887 9.596m7.51-43.391q25.45 0 40.887-17.106 15.855-17.106 15.854-43.807 0-17.94-7.092-31.709-7.093-13.767-20.027-21.278-12.516-7.926-29.622-7.927-16.689 0-29.622 7.927-12.517 7.51-20.027 21.278-7.092 13.769-7.092 31.709t7.092 31.708q7.51 13.769 20.027 21.695 12.933 7.51 29.622 7.51m53.821 39.219v-53.821l7.927-48.815-7.927-48.397v-49.231h45.894v200.264zM607.629 305.059V189.49q0-20.027-12.933-32.96-12.517-12.934-32.543-12.934-13.351 0-23.782 5.841T522.1 165.709q-5.841 10.43-5.841 23.781l-17.94-10.013q0-22.947 10.013-40.47 10.013-17.94 27.536-27.954 17.94-10.43 40.053-10.43 22.53 0 40.053 10.013t27.536 27.954q10.013 17.523 10.013 40.887v125.582zm-137.264 0V4.663h45.894V305.06z\"></path><g fill=\"#ff5a00\" clip-path=\"url(#clip1_9381_2616)\"><path d=\"M50.236 157.311a41.35 41.35 0 0 0 22.232-6.472l80.282-50.936-112.74-82.16C23.36 5.59-.008 17.498-.008 38.05v86.259l20.948 20.849c7.855 7.806 18.23 12.104 29.346 12.104z\"></path><path d=\"m8.786 238.662 115.359 99.056 39.128 33.595c9.14 7.855 22.528 8.102 31.965.642l164.318-129.587c6.027-4.793 9.585-12.055 9.585-19.762V36.253c0-20.206-22.677-32.211-39.376-20.8L178.49 118.71l-90.163 57.21c-11.709 7.46-24.95 11.066-38.09 11.066-18.33 0-36.51-7.064-50.245-20.749v53.356c0 7.361 3.211 14.327 8.794 19.07\"></path></g></g><defs><clipPath id=\"clip0_9381_2616\"><path fill=\"#fff\" d=\"M0 0h2045.14v389H0z\"></path></clipPath><clipPath id=\"clip1_9381_2616\"><path fill=\"#fff\" d=\"M-.008 11.031H369.14v366.332H-.008z\"></path></clipPath></defs></svg><span class=\"aeo\">AEO</span></span></div></header>"
    },
    {
      "id": "lf-section-opener",
      "title": "Section opener (kicker, headline, dek, scope)",
      "type": "Typography / Heading block",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "heading",
        "typography",
        "text"
      ],
      "usage": "Opens every sheet. Kicker \"NN / Section name\" with orange dot, h1 (sheet 1) or h2 (later sheets), dek paragraph, optional scope meta line.",
      "html": "<div class=\"kicker\">01 / Executive summary</div>\n<h1>AI recommends you for retail.<br>Healthcare is the blind spot.</h1>\n<p class=\"dek\">Northstar earns recommendations in one-third of tested retail answers, but just one in twelve healthcare answers. The difference points to a focused area to investigate.</p>\n<p class=\"scope\">Customer support software · 48 non-branded questions · 192 audited answers · 4 engines</p>"
    },
    {
      "id": "lf-stat-cards",
      "title": "Stat cards (3-up)",
      "type": "Data / Metric cards",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "metric",
        "kpi",
        "cards",
        "data"
      ],
      "usage": "Three headline KPIs: uppercase label, large value, detail line. Use .gain for positive deltas.",
      "html": "<div class=\"stats\">\n    <div class=\"stat\"><div class=\"value\" data-bind=\"visibility\">37.5%</div><div class=\"name\">Discovered without being named</div><div class=\"detail\">72 of 192 answers mention Northstar<br><span class=\"gain\">+6.3 pp versus previous sample</span></div></div>\n    <div class=\"stat\"><div class=\"value\">25.0%</div><div class=\"name\">Explicitly recommended</div><div class=\"detail\">48 of 192 answers recommend Northstar<br><span class=\"gain\">+6.3 pp versus previous sample</span></div></div>\n    <div class=\"stat\"><div class=\"value\" data-bind=\"absenceCompetitor\">71.7%</div><div class=\"name\">Competitors fill the gap</div><div class=\"detail\">86 of 120 answers without Northstar recommend at least one tracked rival</div></div>\n  </div>"
    },
    {
      "id": "lf-bar-list",
      "title": "Horizontal bar list",
      "type": "Data viz / Bar chart",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "data-viz",
        "chart",
        "bars"
      ],
      "usage": "Ranked rates per segment. Label, track with orange .fill.own, right-aligned value, caption below.",
      "html": "<div><h3>Where you earn a place</h3><div class=\"bars\" id=\"summary-bars\"><div class=\"barrow\"><span>SaaS</span><div class=\"track\"><div class=\"fill own\" style=\"width:37.5%\"></div></div><span class=\"barvalue\">37.5%</span></div><div class=\"barrow\"><span>Retail</span><div class=\"track\"><div class=\"fill own\" style=\"width:33.333333333333336%\"></div></div><span class=\"barvalue\">33.3%</span></div><div class=\"barrow\"><span>Professional services</span><div class=\"track\"><div class=\"fill own\" style=\"width:20.833333333333332%\"></div></div><span class=\"barvalue\">20.8%</span></div><div class=\"barrow\"><span>Healthcare</span><div class=\"track\"><div class=\"fill own\" style=\"width:8.333333333333334%\"></div></div><span class=\"barvalue\">8.3%</span></div></div><p class=\"caption\">Northstar recommendation rate. Each industry: 12 questions × 4 engines.</p></div>"
    },
    {
      "id": "lf-keyline-list",
      "title": "Keyline rows + narrative",
      "type": "Data / Key-value list",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "list",
        "key-value",
        "text"
      ],
      "usage": "Label/value pairs separated by hairlines, followed by narrative prose and fine print.",
      "html": "<div><h3>Discovery ≠ recognition</h3><div class=\"keyline\"><span>Questions naming Northstar</span><strong>87.5% visibility</strong></div><div class=\"keyline\"><span>Questions without its name</span><strong>37.5% visibility</strong></div><p class=\"narrative\">AI usually recognizes Northstar when asked about it. It introduces the brand much less often when answering category questions.</p><p class=\"fine\">Branded results use a separate sample of 12 questions / 48 answers and are excluded from discovery metrics.</p></div>"
    },
    {
      "id": "lf-two-column",
      "title": "Two-column split",
      "type": "Layout / Split",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "layout",
        "grid",
        "columns"
      ],
      "usage": "Two equal columns (.split) for pairing a chart with commentary. Collapses to one column under 700px.",
      "html": "<div class=\"split\"><div><div class=\"researchlabel\">Additional input · fictional page inspection</div><h3 style=\"margin-top:10px\">A comparison page worth reviewing</h3><p class=\"narrative\">The fictional Support Atlas healthcare comparison lists ResolveWorks and ServiceForge, but omits Northstar. Inclusion is worth considering only after confirming that Northstar meets the page’s criteria.</p><p class=\"fine\">Page contents are a separate research input, not inferred from the citation count.</p></div><div><div class=\"researchlabel\">Additional input · fictional content inventory</div><h3 style=\"margin-top:10px\">An owned page needs clearer qualifiers</h3><p class=\"narrative\">Northstar’s security overview covers audit logs and SSO but does not clearly identify which plan includes each capability. This supports a specific documentation review.</p><p class=\"fine\">This proposed update relies on supplied page contents.</p></div></div>"
    },
    {
      "id": "lf-evidence-quote",
      "title": "Evidence card (quote)",
      "type": "Callout / Evidence",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "evidence",
        "quote",
        "callout",
        "cards"
      ],
      "usage": "Raised card with eyebrow, quoted question/answer, outcome line (.result) and explanatory text. Optional link button.",
      "html": "<div class=\"evidence\"><div class=\"eyebrow\">One question behind the gap</div><p class=\"quote\">“Which help desk platforms suit a healthcare team that needs SSO and audit logs?”</p><p class=\"result\">Northstar is absent across all four sampled engine answers.</p><p class=\"answer\">Synthetic ChatGPT excerpt: “ResolveWorks is worth evaluating for teams prioritizing access controls and auditability.” This is fictional evidence, not a verified product claim.</p><button class=\"linkbutton\" data-go=\"7\">Inspect the supporting evidence →</button></div>"
    },
    {
      "id": "lf-fact-pair",
      "title": "Fact check pair",
      "type": "Callout / Comparison",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "evidence",
        "comparison",
        "accuracy",
        "cards"
      ],
      "usage": "Side-by-side claim vs approved fact (.fact.correct tinted green), inside an evidence card with narrative.",
      "html": "<div class=\"evidence\"><div class=\"eyebrow\">A verifiable claim</div><h3>SSO availability is described incorrectly.</h3><div class=\"factpair\"><div class=\"fact\"><div class=\"eyebrow\">Synthetic answer claim</div>“Northstar Desk does not currently offer SSO.”<span class=\"sub\">Gemini · Branded question sample</span></div><div class=\"fact correct\"><div class=\"eyebrow\">Fictional approved fact sheet</div>“SAML SSO is available on the Enterprise plan.”<span class=\"sub\">Brand brief · version October 1, 2026</span></div></div><p class=\"narrative\">Proposed response: verify the current plan documentation and relevant third-party listings. The available evidence does not identify the origin of the incorrect claim.</p></div>"
    },
    {
      "id": "lf-action-panel",
      "title": "Action panel (dark)",
      "type": "Callout / CTA",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "cta",
        "callout",
        "emphasis",
        "dark"
      ],
      "usage": "Dark emphasis block for the single recommended move at the end of a sheet.",
      "html": "<div class=\"actionpanel\"><div class=\"eyebrow\">The first move</div><h3>Investigate healthcare requirements before expanding content.</h3><p>Validate Northstar’s fit, review the pages cited for these questions, then decide whether a requirements page or a third-party inclusion request is warranted.</p></div>"
    },
    {
      "id": "lf-data-table",
      "title": "Data table",
      "type": "Data / Table",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "table",
        "data"
      ],
      "usage": "Bordered rounded table with raised uppercase header, .subject first column with .sub note, .num right-aligned tabular cells.",
      "html": "<div class=\"tablewrap\"><table><thead><tr><th>Industry</th><th class=\"num\">Answers</th><th class=\"num\">Mentioned</th><th class=\"num\">Recommended</th><th class=\"num\">Recommendation rate</th></tr></thead><tbody id=\"industry-table\"><tr><td class=\"subject\">SaaS<span class=\"sub\">12 questions</span></td><td class=\"num\">48</td><td class=\"num\">26</td><td class=\"num\">18</td><td class=\"num\">37.5%</td></tr><tr><td class=\"subject\">Healthcare<span class=\"sub\">12 questions</span></td><td class=\"num\">48</td><td class=\"num\">10</td><td class=\"num\">4</td><td class=\"num\">8.3%</td></tr><tr><td class=\"subject\">Retail<span class=\"sub\">12 questions</span></td><td class=\"num\">48</td><td class=\"num\">20</td><td class=\"num\">16</td><td class=\"num\">33.3%</td></tr><tr><td class=\"subject\">Professional services<span class=\"sub\">12 questions</span></td><td class=\"num\">48</td><td class=\"num\">16</td><td class=\"num\">10</td><td class=\"num\">20.8%</td></tr></tbody></table></div>"
    },
    {
      "id": "lf-table-highlight",
      "title": "Data table with highlighted row",
      "type": "Data / Table",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "table",
        "data",
        "comparison",
        "highlight"
      ],
      "usage": "Competitor comparison; tr.highlight marks the client brand row with an orange tint.",
      "html": "<div class=\"tablewrap\"><table><thead><tr><th>Brand</th><th class=\"num\">Recommended answers</th><th class=\"num\">Rate / 192</th><th class=\"num\">Recommended when Northstar is absent / 120</th></tr></thead><tbody id=\"competitor-table\"><tr><td class=\"subject\">ResolveWorks</td><td class=\"num\">68</td><td class=\"num\">35.4%</td><td class=\"num\">56/120 · 46.7%</td></tr><tr><td class=\"subject\">QueuePilot</td><td class=\"num\">56</td><td class=\"num\">29.2%</td><td class=\"num\">44/120 · 36.7%</td></tr><tr><td class=\"subject\">ServiceForge</td><td class=\"num\">20</td><td class=\"num\">10.4%</td><td class=\"num\">8/120 · 6.7%</td></tr><tr class=\"highlight\"><td class=\"subject\">Northstar Desk<span class=\"sub\">Your brand</span></td><td class=\"num\">48</td><td class=\"num\">25.0%</td><td class=\"num\">—</td></tr></tbody></table></div>"
    },
    {
      "id": "lf-heatmap",
      "title": "Heatmap table",
      "type": "Data viz / Heatmap",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "data-viz",
        "table",
        "heatmap"
      ],
      "usage": "Matrix of rates; each .heat chip background is color-mix(ink N%, white) scaled to the value.",
      "html": "<div class=\"block\"><h3>Industry × use case</h3><div class=\"tablewrap\"><table><thead><tr><th>Recommendation rate</th><th class=\"num\">Ticket routing</th><th class=\"num\">Self-service</th><th class=\"num\">Omnichannel</th><th class=\"num\">Access controls</th></tr></thead><tbody id=\"heatmap\"><tr><td>SaaS</td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 30.7%,var(--s-main))\">66.7%</span><span class=\"sub\">8 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 24.0%,var(--s-main))\">50.0%</span><span class=\"sub\">6 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 14.0%,var(--s-main))\">25.0%</span><span class=\"sub\">3 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 7.3%,var(--s-main))\">8.3%</span><span class=\"sub\">1 / 12</span></td></tr><tr><td>Healthcare</td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 14.0%,var(--s-main))\">25.0%</span><span class=\"sub\">3 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 7.3%,var(--s-main))\">8.3%</span><span class=\"sub\">1 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 4.0%,var(--s-main))\">0.0%</span><span class=\"sub\">0 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 4.0%,var(--s-main))\">0.0%</span><span class=\"sub\">0 / 12</span></td></tr><tr><td>Retail</td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 24.0%,var(--s-main))\">50.0%</span><span class=\"sub\">6 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 24.0%,var(--s-main))\">50.0%</span><span class=\"sub\">6 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 14.0%,var(--s-main))\">25.0%</span><span class=\"sub\">3 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 7.3%,var(--s-main))\">8.3%</span><span class=\"sub\">1 / 12</span></td></tr><tr><td>Professional services</td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 17.3%,var(--s-main))\">33.3%</span><span class=\"sub\">4 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 14.0%,var(--s-main))\">25.0%</span><span class=\"sub\">3 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 14.0%,var(--s-main))\">25.0%</span><span class=\"sub\">3 / 12</span></td><td class=\"num\"><span class=\"heat\" style=\"background:color-mix(in srgb,var(--ink) 4.0%,var(--s-main))\">0.0%</span><span class=\"sub\">0 / 12</span></td></tr></tbody></table></div><p class=\"caption\">Each cell contains 3 questions / 12 answers. Small groups are directional; inspect examples before assigning priority.</p></div>"
    },
    {
      "id": "lf-journey",
      "title": "Buying journey stages",
      "type": "Data viz / Stage strip",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "data-viz",
        "journey",
        "stages",
        "cards"
      ],
      "usage": "Six equal tiles: stage label, big rate, answer count. Becomes 3 columns on mobile.",
      "html": "<div class=\"block\"><h3>Coverage through the buying journey</h3><div class=\"journey\" id=\"journey\"><div class=\"stage\"><span class=\"stagelabel\">Realization</span><b>46.9%</b><span>15 / 32 answers</span></div><div class=\"stage\"><span class=\"stagelabel\">Define needs</span><b>15.6%</b><span>5 / 32 answers</span></div><div class=\"stage\"><span class=\"stagelabel\">Explore options</span><b>31.3%</b><span>10 / 32 answers</span></div><div class=\"stage\"><span class=\"stagelabel\">Shortlist</span><b>6.3%</b><span>2 / 32 answers</span></div><div class=\"stage\"><span class=\"stagelabel\">Decision</span><b>37.5%</b><span>12 / 32 answers</span></div><div class=\"stage\"><span class=\"stagelabel\">Validation</span><b>12.5%</b><span>4 / 32 answers</span></div></div><p class=\"caption\">Explicit recommendation rate by buying stage. Each stage contains 8 questions / 32 answers.</p></div>"
    },
    {
      "id": "lf-outcome-bar",
      "title": "Stacked outcome bar + legend",
      "type": "Data viz / Stacked bar",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "data-viz",
        "stacked-bar",
        "legend"
      ],
      "usage": "Single 100% stacked bar of outcome shares with keyline legend and narrative.",
      "html": "<div><h3>How Northstar appears</h3><div id=\"outcome-bar\" class=\"outcomebar\" role=\"img\" aria-label=\"Northstar answer outcomes\"><span style=\"width:9.375%;background:var(--ink)\"></span><span style=\"width:15.625%;background:var(--blue)\"></span><span style=\"width:12.5%;background:var(--ink3)\"></span><span style=\"width:62.5%;background:var(--s-hover2)\"></span></div><div id=\"outcome-legend\"><div class=\"keyline\"><span>First-position recommendation</span><strong>18 / 192</strong></div><div class=\"keyline\"><span>Other recommendation</span><strong>30 / 192</strong></div><div class=\"keyline\"><span>Mentioned, not recommended</span><strong>24 / 192</strong></div><div class=\"keyline\"><span>Absent</span><strong>120 / 192</strong></div></div><p class=\"narrative\">A mention is weaker evidence than an explicit recommendation. First-position recommendations are a narrower subset, shown separately.</p></div>"
    },
    {
      "id": "lf-finding",
      "title": "Finding callout",
      "type": "Callout / Finding",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "callout",
        "insight",
        "text"
      ],
      "usage": "Key insight with orange left rule: bold statement + supporting paragraph.",
      "html": "<div class=\"finding\"><strong>Healthcare has the weakest recommendation coverage.</strong><p>Northstar is mentioned in 10 of 48 healthcare answers and recommended in only 4. Its absence in the other 38 is worth investigating against the customer’s healthcare priorities.</p></div>"
    },
    {
      "id": "lf-note",
      "title": "Note box",
      "type": "Callout / Note",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "callout",
        "note",
        "text"
      ],
      "usage": "Raised box for context, caveats or inputs required. Lead with a bold phrase.",
      "html": "<div class=\"note\"><strong>Business context changes the priority.</strong> In this fictional brief, healthcare expansion and midmarket retail are the brand’s priorities. Low visibility in a non-target industry would deserve less attention.</div>"
    },
    {
      "id": "lf-pills",
      "title": "Pill tags",
      "type": "Element / Pill",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "tag",
        "badge",
        "status"
      ],
      "usage": "Rounded meta tags. Variants: .pill, .pill.risk (red tint), .pill.good (green tint).",
      "html": "<div class=\"actionmeta\"><span class=\"pill\">Observation</span><span class=\"pill\">Selected example · not a prevalence estimate</span></div>"
    },
    {
      "id": "lf-action-item",
      "title": "Numbered action item",
      "type": "List / Action item",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "list",
        "action",
        "plan"
      ],
      "usage": "Ordinal (orange) + title, pill meta row, then Evidence / Task / Check afterward paragraphs.",
      "html": "<article class=\"actionitem\"><div class=\"ordinal\">01</div><div><h3>Correct the SSO description at its source.</h3><div class=\"actionmeta\"><span class=\"pill risk\">First priority</span><span class=\"pill\">Product marketing + documentation</span><span class=\"pill\">Estimated effort: small</span></div><p><strong>Evidence:</strong> The SSO answer contradicts the supplied fact sheet. The security page lacks clear plan-level qualifiers.</p><p><strong>Task:</strong> confirm the approved SSO statement, clarify the security and plan documentation, then inspect relevant cited listings for outdated information.</p><p><strong>Check afterward:</strong> rerun the affected branded questions and record the exact claim across engines. Success means accurate plan-qualified descriptions; improved discovery is a separate measure.</p></div></article>"
    },
    {
      "id": "lf-method-grid",
      "title": "Methodology grid",
      "type": "Layout / Two-column list",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "methodology",
        "list",
        "layout"
      ],
      "usage": "Two columns of h3 + bullet list describing sample and inputs.",
      "html": "<div class=\"methodgrid\"><div><h3>Measured sample</h3><ul><li>48 non-branded questions; 192 audited answers.</li><li>12 branded questions; 48 audited answers, reported separately.</li><li>Four engines, one answer per question per engine.</li><li>Latest sample: October 6, 2026. Previous: September 22, 2026.</li><li>All 240 synthetic answers are available; no missing-engine fixture.</li></ul></div><div><h3>Additional fictional inputs</h3><ul><li>Business brief: healthcare expansion and midmarket retail priorities.</li><li>Approved product fact sheet, dated October 1.</li><li>Security-page content inventory.</li><li>Support Atlas page inspection.</li><li>Three configured competitors. No demand, traffic, or CRM data.</li></ul></div></div>"
    },
    {
      "id": "lf-disclosure",
      "title": "Evidence disclosure",
      "type": "Element / Details",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "interactive",
        "disclosure",
        "evidence"
      ],
      "usage": "Native <details> record with summary and labelled paragraphs. Auto-opened for print.",
      "html": "<details open=\"\"><summary>Healthcare requirements · Non-branded sample</summary><p><strong>Question:</strong> Which help desk platforms suit a healthcare team that needs SSO and audit logs?</p><p><strong>Outcomes:</strong> Northstar absent in all four synthetic answers. ChatGPT recommends ResolveWorks; the excerpt is reproduced on pages 1 and 3.</p><p>ChatGPT · October 6, 2026. Answer text is an authored illustration.</p></details>"
    },
    {
      "id": "lf-footer",
      "title": "Sheet footer",
      "type": "Layout / Footer",
      "scope": "hf-lf",
      "source": [
        "long-form"
      ],
      "tags": [
        "footer",
        "meta",
        "layout"
      ],
      "usage": "Hairline footer: scope note left, \"HappyFox AEO / NN\" page marker right.",
      "html": "<footer class=\"footer\"><span>Fictional sample</span><span>HappyFox AEO / 01</span></footer>"
    },
    {
      "id": "op-preview-bar",
      "title": "Preview bar",
      "type": "Navigation / Toolbar",
      "scope": "hf-op",
      "source": [
        "one-page"
      ],
      "tags": [
        "toolbar",
        "screen-only",
        "print"
      ],
      "usage": "Screen-only bar above the page: title + context and Print / Save PDF button.",
      "html": "<div class=\"preview-bar\">\n    <div><strong>One-page report reference</strong><span>Fictional brand and illustrative data · US Letter print layout</span></div>\n    <div class=\"preview-tools\"><button type=\"button\" onclick=\"window.print()\">Print / Save PDF</button></div>\n  </div>"
    },
    {
      "id": "op-masthead",
      "title": "One-page masthead",
      "type": "Layout / Header",
      "scope": "hf-op",
      "source": [
        "one-page"
      ],
      "tags": [
        "header",
        "branding",
        "layout"
      ],
      "usage": "Client name with uppercase subtitle left; HappyFox AEO logo with report label right.",
      "html": "<header class=\"masthead\">\n      <div class=\"brand\">Northstar Desk<span>AI visibility brief</span></div>\n      <div class=\"publisher\"><span class=\"hf-publisher\"><svg class=\"hf-wordmark\" viewBox=\"0 0 2046 389\" fill=\"none\" role=\"img\" aria-label=\"HappyFox\"><g clip-path=\"url(#clip0_9381_2616)\"><path fill=\"currentColor\" d=\"m1990.08 305.059-57.58-84.695-8.34-7.509-77.61-108.059h55.49l51.32 74.264 7.93 7.093 83.86 118.906zm-147.28 0 80.94-112.231 26.7 32.96-54.24 79.271zm122.66-93.039-27.12-32.543 50.07-74.681h52.98zM1748.81 309.235c-19.47 0-37.14-4.59-52.99-13.768-15.86-9.457-28.51-22.113-37.97-37.967q-13.77-23.78-13.77-52.987 0-29.205 13.77-52.569c9.46-15.576 22.11-27.953 37.97-37.132 15.85-9.457 33.52-14.185 52.99-14.185q29.61 0 53.4 13.768c15.85 9.179 28.37 21.695 37.55 37.549 9.46 15.576 14.18 33.099 14.18 52.569s-4.72 37.133-14.18 52.987c-9.18 15.854-21.7 28.51-37.55 37.967q-23.79 13.768-53.4 13.768m0-44.225q17.1 0 30.03-7.51c8.91-5.285 15.72-12.517 20.45-21.695 5-9.179 7.51-19.609 7.51-31.292s-2.51-21.973-7.51-30.874c-5.01-8.9-11.82-15.854-20.45-20.86q-12.93-7.927-30.03-7.927c-11.13 0-21.14 2.642-30.04 7.927-8.63 5.006-15.44 11.96-20.45 20.86-4.73 8.901-7.09 19.192-7.09 30.874 0 11.683 2.36 22.113 7.09 31.292 5.01 9.178 11.82 16.41 20.45 21.695 8.9 5.006 18.91 7.51 30.04 7.51M1545.77 305.062V78.514c0-15.298 3.34-28.788 10.01-40.47 6.96-11.682 16.41-20.861 28.37-27.536 12.24-6.676 26.29-10.014 42.14-10.014q18.36 0 31.29 6.259c8.63 4.172 16.69 10.152 24.2 17.94l-29.62 29.622c-3.34-3.337-6.95-5.98-10.85-7.927-3.89-1.947-8.9-2.92-15.02-2.92-11.12 0-19.75 3.06-25.87 9.178q-8.76 8.762-8.76 25.45v226.966zm9.97-158.542v-41.722h96.42v41.722zM1410.55 307.145l-85.53-202.349h50.49l58.41 148.529h-14.61l61.75-148.529h50.9l-93.04 202.349zm-59.66 81.358 62.17-128.086 25.86 46.728-37.13 81.358zM1233.45 309.235c-15.29 0-28.92-3.199-40.88-9.596-11.96-6.676-21.42-15.715-28.37-27.119q-10.02-17.106-10.02-38.801v-57.576c0-14.464 3.48-27.397 10.43-38.801 6.96-11.404 16.41-20.305 28.38-26.702 11.96-6.676 25.45-10.013 40.46-10.013 18.08 0 34.36 4.728 48.82 14.185 14.74 9.179 26.28 21.695 34.63 37.549q12.93 23.365 12.93 52.987 0 29.205-12.93 52.986c-8.35 15.576-19.89 27.954-34.63 37.133-14.46 9.178-30.74 13.768-48.82 13.768m-7.5-43.391c11.12 0 20.86-2.503 29.2-7.51 8.62-5.284 15.3-12.516 20.03-21.695 5-9.179 7.51-19.748 7.51-31.708s-2.51-22.53-7.51-31.709c-4.73-9.178-11.41-16.271-20.03-21.278-8.34-5.284-18.08-7.927-29.2-7.927-11.13 0-21 2.643-29.63 7.927-8.62 5.007-15.3 12.1-20.02 21.278-4.73 9.179-7.1 19.749-7.1 31.709s2.37 22.529 7.1 31.708c4.72 9.179 11.4 16.411 20.02 21.695 8.63 5.007 18.5 7.51 29.63 7.51m-99.72 122.662V104.799h45.89v53.821l-7.92 48.814 7.92 48.397v132.675zM1010.77 309.235q-22.952 0-40.892-9.596-17.94-10.013-28.37-27.119-10.014-17.106-10.013-38.801v-57.576q0-21.695 10.43-38.801t28.371-26.702q17.939-10.014 40.474-10.013c18.07 0 34.35 4.728 48.81 14.185 14.74 9.179 26.28 21.695 34.63 37.549q12.93 23.365 12.93 52.987 0 29.205-12.93 52.986c-8.35 15.576-19.89 27.954-34.63 37.133-14.46 9.178-30.74 13.768-48.81 13.768m-7.51-43.391c11.12 0 20.86-2.503 29.2-7.51 8.62-5.284 15.3-12.516 20.03-21.695 5-9.179 7.51-19.748 7.51-31.708s-2.51-22.53-7.51-31.709c-4.73-9.178-11.41-16.271-20.03-21.278-8.34-5.284-18.08-7.927-29.2-7.927q-16.694 0-29.627 7.927-12.933 7.51-20.026 21.278-7.093 13.769-7.093 31.709t7.093 31.708q7.092 13.769 20.026 21.695 12.933 7.51 29.627 7.51m-99.719 122.662V104.799h45.894v53.821l-7.927 48.814 7.927 48.397v132.675zM764.695 309.235q-27.119 0-49.231-13.768-21.696-13.769-34.629-37.133-12.517-23.781-12.517-52.986 0-29.622 12.517-52.987 12.933-23.78 34.629-37.549 22.112-14.185 49.231-14.185 22.947 0 40.47 10.013 17.94 9.596 28.371 26.702t10.43 38.801v57.576q0 21.695-10.43 38.801-10.013 17.106-27.954 27.119-17.94 9.596-40.887 9.596m7.51-43.391q25.45 0 40.887-17.106 15.855-17.106 15.854-43.807 0-17.94-7.092-31.709-7.093-13.767-20.027-21.278-12.516-7.926-29.622-7.927-16.689 0-29.622 7.927-12.517 7.51-20.027 21.278-7.092 13.769-7.092 31.709t7.092 31.708q7.51 13.769 20.027 21.695 12.933 7.51 29.622 7.51m53.821 39.219v-53.821l7.927-48.815-7.927-48.397v-49.231h45.894v200.264zM607.629 305.059V189.49q0-20.027-12.933-32.96-12.517-12.934-32.543-12.934-13.351 0-23.782 5.841T522.1 165.709q-5.841 10.43-5.841 23.781l-17.94-10.013q0-22.947 10.013-40.47 10.013-17.94 27.536-27.954 17.94-10.43 40.053-10.43 22.53 0 40.053 10.013t27.536 27.954q10.013 17.523 10.013 40.887v125.582zm-137.264 0V4.663h45.894V305.06z\"></path><g fill=\"#ff5a00\" clip-path=\"url(#clip1_9381_2616)\"><path d=\"M50.236 157.311a41.35 41.35 0 0 0 22.232-6.472l80.282-50.936-112.74-82.16C23.36 5.59-.008 17.498-.008 38.05v86.259l20.948 20.849c7.855 7.806 18.23 12.104 29.346 12.104z\"></path><path d=\"m8.786 238.662 115.359 99.056 39.128 33.595c9.14 7.855 22.528 8.102 31.965.642l164.318-129.587c6.027-4.793 9.585-12.055 9.585-19.762V36.253c0-20.206-22.677-32.211-39.376-20.8L178.49 118.71l-90.163 57.21c-11.709 7.46-24.95 11.066-38.09 11.066-18.33 0-36.51-7.064-50.245-20.749v53.356c0 7.361 3.211 14.327 8.794 19.07\"></path></g></g><defs><clipPath id=\"clip0_9381_2616\"><path fill=\"#fff\" d=\"M0 0h2045.14v389H0z\"></path></clipPath><clipPath id=\"clip1_9381_2616\"><path fill=\"#fff\" d=\"M-.008 11.031H369.14v366.332H-.008z\"></path></clipPath></defs></svg><span class=\"aeo\">AEO</span></span><small>The 60-second read</small></div>\n    </header>"
    },
    {
      "id": "op-headline",
      "title": "Eyebrow + headline + dek",
      "type": "Typography / Heading block",
      "scope": "hf-op",
      "source": [
        "one-page"
      ],
      "tags": [
        "heading",
        "typography",
        "text"
      ],
      "usage": "Two-sided eyebrow row, h1 with <em> second line in grey, dek paragraph.",
      "html": "<div class=\"eyebrow\"><span>Customer support software · October 6, 2026</span><span class=\"sample\">Illustrative sample</span></div>\n<h1>AI recommends you for retail.<br><em>Healthcare is the blind spot.</em></h1>\n<p class=\"dek\">Northstar earns recommendations in one-third of tested retail answers, but just one in twelve healthcare answers. The difference points to a focused area to investigate.</p>"
    },
    {
      "id": "op-scope-strip",
      "title": "Scope strip",
      "type": "Text / Meta strip",
      "scope": "hf-op",
      "source": [
        "one-page"
      ],
      "tags": [
        "meta",
        "scope"
      ],
      "usage": "Bordered top/bottom line of bolded counts describing the sample.",
      "html": "<div class=\"scope\"><span><b>60</b> tracked questions</span><span><b>240</b> analyzed answers</span><span><b>4</b> engines: ChatGPT, Claude, Gemini, Perplexity</span></div>"
    },
    {
      "id": "op-metric-cards",
      "title": "Metric cards (3-up, compact)",
      "type": "Data / Metric cards",
      "scope": "hf-op",
      "source": [
        "one-page"
      ],
      "tags": [
        "metric",
        "kpi",
        "cards",
        "data"
      ],
      "usage": "Compact print-sized KPI cards: label, value, two-line detail.",
      "html": "<div class=\"metrics\">\n      <div class=\"metric\"><p class=\"metric-label\">Discovered without being named</p><div class=\"metric-value\">37.5%</div><p class=\"metric-detail\">Mentioned in 72 of 192<br>non-branded answers</p></div>\n      <div class=\"metric\"><p class=\"metric-label\">Explicitly recommended</p><div class=\"metric-value\">25.0%</div><p class=\"metric-detail\">Recommended in 48 of 192<br>non-branded answers</p></div>\n      <div class=\"metric\"><p class=\"metric-label\">Competitors fill the gap</p><div class=\"metric-value\">71.7%</div><p class=\"metric-detail\">A competitor recommended in 86<br>of 120 answers missing Northstar</p></div>\n    </div>\n<p class=\"recognition\"><strong>Recognition is stronger than discovery.</strong><span>When the question names Northstar, it appears in 42 of 48 answers (87.5%).</span></p>"
    },
    {
      "id": "op-bar-table",
      "title": "Section with bar table",
      "type": "Data / Table with bars",
      "scope": "hf-op",
      "source": [
        "one-page"
      ],
      "tags": [
        "table",
        "data-viz",
        "bars",
        "section"
      ],
      "usage": "Numbered section heading (orange number) + note, 3-column table with inline orange bar and value, table footnote.",
      "html": "<section aria-labelledby=\"segments-heading\">\n      <div class=\"section-heading\"><h2 id=\"segments-heading\"><span class=\"section-number\">01</span>Where you make the shortlist</h2><p class=\"section-note\">Explicit recommendations · non-branded questions</p></div>\n      <table>\n        <caption>Illustrative recommendations by industry, with twelve questions and forty-eight answers per segment</caption>\n        <thead><tr><th scope=\"col\">Buyer need</th><th scope=\"col\">Northstar</th><th scope=\"col\">Observation</th></tr></thead>\n        <tbody><tr><td><span class=\"segment\">SaaS</span><span class=\"segment-note\">12 tested questions</span></td><td><div class=\"bar-line\"><span class=\"track\" aria-hidden=\"true\"><span class=\"fill\" style=\"display:block;width:37.5%\"></span></span><span class=\"bar-value\">18/48 · 37.5%</span></div></td><td><span class=\"competitor\">Highest coverage</span></td></tr><tr><td><span class=\"segment\">Retail</span><span class=\"segment-note\">12 tested questions</span></td><td><div class=\"bar-line\"><span class=\"track\" aria-hidden=\"true\"><span class=\"fill\" style=\"display:block;width:33.33333333333333%\"></span></span><span class=\"bar-value\">16/48 · 33.3%</span></div></td><td><span class=\"competitor\">One in three answers</span></td></tr><tr><td><span class=\"segment\">Professional services</span><span class=\"segment-note\">12 tested questions</span></td><td><div class=\"bar-line\"><span class=\"track\" aria-hidden=\"true\"><span class=\"fill\" style=\"display:block;width:20.833333333333336%\"></span></span><span class=\"bar-value\">10/48 · 20.8%</span></div></td><td><span class=\"competitor\">Less consistent inclusion</span></td></tr><tr><td><span class=\"segment\">Healthcare</span><span class=\"segment-note\">12 tested questions</span></td><td><div class=\"bar-line\"><span class=\"track\" aria-hidden=\"true\"><span class=\"fill\" style=\"display:block;width:8.333333333333332%\"></span></span><span class=\"bar-value\">4/48 · 8.3%</span></div></td><td><span class=\"competitor\">Largest observed gap</span></td></tr></tbody>\n      </table>\n      <p class=\"table-foot\">Each industry: 12 questions / 48 answers. Discovery metrics: 48 non-branded questions / 192 answers.</p>\n    </section>"
    },
    {
      "id": "op-evidence",
      "title": "Evidence block (2-column)",
      "type": "Callout / Evidence",
      "scope": "hf-op",
      "source": [
        "one-page"
      ],
      "tags": [
        "evidence",
        "quote",
        "callout",
        "section"
      ],
      "usage": "Question blockquote left, observed outcome + engines right, under a numbered section heading.",
      "html": "<section aria-labelledby=\"evidence-heading\">\n      <div class=\"section-heading\"><h2 id=\"evidence-heading\"><span class=\"section-number\">02</span>One question behind the gap</h2><p class=\"section-note\">Example evidence · fictional answer outcomes</p></div>\n      <div class=\"evidence\">\n        <div><p class=\"evidence-label\">Tracked buyer question</p><blockquote>“Which help desk platforms suit a healthcare team that needs SSO and audit logs?”</blockquote></div>\n        <div><p class=\"evidence-label\">Observed outcome in this sample</p><p class=\"outcome\"><strong>Northstar is absent from all four answers.</strong> In the fictional ChatGPT answer, ResolveWorks is recommended for access controls and auditability.</p><p class=\"engine-row\">ChatGPT · Claude · Gemini · Perplexity</p></div>\n      </div>\n    </section>"
    },
    {
      "id": "op-next-step",
      "title": "Next step + invitation panel",
      "type": "Callout / CTA",
      "scope": "hf-op",
      "source": [
        "one-page"
      ],
      "tags": [
        "cta",
        "callout",
        "dark",
        "emphasis"
      ],
      "usage": "Dark panel: proposed next step left, \"Go deeper\" invitation with orange link right.",
      "html": "<section class=\"next-step\" aria-labelledby=\"next-heading\">\n      <div><p class=\"label\">Proposed next step</p><h2 id=\"next-heading\">Investigate the healthcare gap.</h2><p>Check product fit, then inspect answer descriptions and cited sources for concrete inclusion gaps.</p></div>\n      <div class=\"invitation\"><p class=\"label\">Go deeper</p><strong>Request a comprehensive analysis →</strong><p>Explore the missing use cases, competitor positioning, and source evidence behind this snapshot.</p></div>\n    </section>"
    },
    {
      "id": "op-method-footer",
      "title": "Method note + footer",
      "type": "Layout / Footer",
      "scope": "hf-op",
      "source": [
        "one-page"
      ],
      "tags": [
        "footer",
        "methodology",
        "meta"
      ],
      "usage": "Fine-print method note followed by hairline footer with brand and page count.",
      "html": "<p class=\"method\">Illustrative data only; all brand names and outcomes are fictional. A real report would use one analyzed scan, with traceable prompt groups and answer evidence. Visibility measures presence in tested answers, not buyer demand, leads, or revenue.</p>\n<footer><span>HappyFox AEO</span><span>1 / 1</span></footer>"
    }
  ]
}
```

## Scoped stylesheet

```css
/* HappyFox AEO report components — generated from long-form.html (.hf-lf) and one-page.html (.hf-op).
   Wrap any snippet in <div class="hf-lf"> or <div class="hf-op"> and include these styles. */
.hf-lf,.hf-op{font-family:Inter,system-ui,sans-serif;}
.hf-lf,.hf-lf *{box-sizing: border-box;}
.hf-lf{margin: 0;font: 15px/1.55 var(--sans);}
.hf-lf button,.hf-lf select,.hf-lf a{touch-action: manipulation;}
.hf-lf button{cursor: pointer;}
.hf-lf a{color: var(--ink);}
.hf-lf .reviewbar{position: sticky;top: 0;z-index: 10;display: flex;align-items: center;flex-wrap: wrap;}
.hf-lf .reviewbar .label{letter-spacing: .1em;text-transform: uppercase;}
.hf-lf .reviewbar select{background: var(--s-raised);color: #fff;border: 1px solid var(--bd-3);padding: 8px 10px;border-radius: 4px;max-width: 100%;min-width: 0;}
.hf-lf .reviewbar button{border: 1px solid var(--bd-3);background: transparent;color: #fff;border-radius: 4px;padding: 8px 12px;}
.hf-lf .reviewbar .spacer{flex: 1;}
.hf-lf .intro{padding: 0 16px;display: flex;justify-content: space-between;gap: 16px;color: var(--ink2);}
.hf-lf .intro strong{color: var(--ink);}
.hf-lf .report{margin: 0 auto 60px;padding: 0 16px;}
.hf-lf .sheet{margin: 0 0 28px;scroll-margin-top: 94px;position: relative;}
.hf-lf .sheet[hidden]{display: none;}
.hf-lf .masthead{display: flex;align-items: center;justify-content: space-between;gap: 24px;border-bottom: 1px solid var(--bd-2);}
.hf-lf .brand{display: flex;align-items: center;gap: 11px;}
.hf-lf .brandmark{display: grid;place-items: center;font-size: 22px;}
.hf-lf .publisher{font-size: 17px;font-weight: 650;white-space: nowrap;}
.hf-lf .publisher span{color: var(--ink);font-weight: 450;margin-left: 5px;}
.hf-lf .sectiontag{text-transform: uppercase;letter-spacing: .13em;}
.hf-lf .kicker{letter-spacing: .14em;text-transform: uppercase;}
.hf-lf h1,.hf-lf h2,.hf-lf h3,.hf-lf p{margin: 0;}
.hf-lf h1{max-width: 790px;}
.hf-lf .dek{margin-top: 16px;}
.hf-lf .scope{color: var(--ink2);margin-top: 12px;}
.hf-lf .stats{display: grid;grid-template-columns: repeat(3,1fr);}
.hf-lf .stat .detail{color: var(--ink2);}
.hf-lf .split{display: grid;grid-template-columns: 1fr 1fr;}
.hf-lf .eyebrow{text-transform: uppercase;margin-bottom: 10px;}
.hf-lf .finding{padding: 2px 0 2px 16px;margin: 20px 0;}
.hf-lf .finding p{margin-top: 7px;color: var(--ink2);}
.hf-lf .actionpanel{margin-top: 27px;}
.hf-lf .actionpanel h3{margin-bottom: 8px;}
.hf-lf .actionpanel p{color: var(--emphasis-muted);}
.hf-lf .actionpanel .eyebrow{color: var(--emphasis-muted);}
.hf-lf .footer{display: flex;justify-content: space-between;align-items: flex-start;gap: 16px;border-top: 1px solid var(--bd-2);margin-top: 30px;padding-top: 13px;letter-spacing: .02em;}
.hf-lf .fine{font-size: 12px;color: var(--ink2);margin-top: 12px;}
.hf-lf .note{background: var(--s-raised);margin-top: 22px;}
.hf-lf .note strong{font-weight: 650;}
.hf-lf .caption{font-size: 12px;color: var(--ink2);margin: 10px 0;}
.hf-lf .tablewrap{overflow-x: auto;margin-top: 15px;}
.hf-lf table{width: 100%;border-collapse: collapse;text-align: left;}
.hf-lf th{color: var(--ink2);border-bottom: 1px solid var(--bd-2);vertical-align: bottom;}
.hf-lf td{border-bottom: 1px solid var(--bd-2);vertical-align: top;}
.hf-lf .num{text-align: right;font-variant-numeric: tabular-nums;}
.hf-lf .sub{display: block;color: var(--ink2);margin-top: 3px;}
.hf-lf .pill{display: inline-block;white-space: nowrap;}
.hf-lf .bars{margin-top: 15px;}
.hf-lf .barrow{display: grid;align-items: center;margin: 14px 0;}
.hf-lf .fill{height: 100%;background: var(--blue);}
.hf-lf .fill.own{background: var(--ink);}
.hf-lf .barvalue{text-align: right;font-variant-numeric: tabular-nums;}
.hf-lf .legend{display: flex;gap: 16px;flex-wrap: wrap;font-size: 11px;color: var(--ink2);margin-top: 10px;}
.hf-lf .swatch{display: inline-block;width: 8px;height: 8px;margin-right: 5px;}
.hf-lf .outcomebar{display: flex;height: 24px;margin: 17px 0 8px;gap: 2px;}
.hf-lf .outcomebar span{min-width: 0;}
.hf-lf .quote{margin: 12px 0 0;padding: 0;font: normal 20px/1.4 var(--sans);}
.hf-lf .quote.small{font-size: 18px;}
.hf-lf .evidence{border-top: 1px solid var(--bd-2);padding-top: 16px;}
.hf-lf .evidence .answer{color: var(--ink2);margin-top: 10px;}
.hf-lf .evidence .result{font-size: 12px;margin-top: 8px;}
.hf-lf .ref{font: 11px var(--sans);letter-spacing: .05em;color: var(--ink2);}
.hf-lf .linkbutton{font-size: 12px;text-decoration: underline;cursor: pointer;}
.hf-lf .journey{display: grid;grid-template-columns: repeat(6,1fr);gap: 6px;margin: 18px 0;}
.hf-lf .stage{background: var(--s-raised);}
.hf-lf .stage b{font-weight: 500;display: block;margin: 8px 0;}
.hf-lf .stage span{display: block;color: var(--ink2);}
.hf-lf .stage .stagelabel{min-height: 32px;color: var(--ink);}
.hf-lf .heat{display: inline-block;min-width: 54px;text-align: center;padding: 6px 8px;font-variant-numeric: tabular-nums;}
.hf-lf .source-title{font-weight: 600;}
.hf-lf .url{font-size: 11px;color: var(--ink2);overflow-wrap: anywhere;}
.hf-lf .factpair{display: grid;grid-template-columns: 1fr 1fr;gap: 20px;margin-top: 13px;}
.hf-lf .fact{padding: 15px;background: var(--s-raised);font-size: 13px;}
.hf-lf .fact .eyebrow{margin-bottom: 5px;}
.hf-lf .narrative{margin-top: 10px;}
.hf-lf .researchlabel{font-size: 11px;letter-spacing: .07em;text-transform: uppercase;}
.hf-lf .actionitem{display: grid;grid-template-columns: 38px 1fr;gap: 16px;padding: 22px 0;border-bottom: 1px solid var(--bd-2);}
.hf-lf .actionitem h3{margin-bottom: 7px;}
.hf-lf .actionmeta{display: flex;flex-wrap: wrap;gap: 8px;margin: 10px 0;}
.hf-lf .actionitem p{font-size: 13px;color: var(--ink2);margin-top: 7px;}
.hf-lf .actionitem p strong{color: var(--ink);font-weight: 600;}
.hf-lf .methodgrid{display: grid;grid-template-columns: 1fr 1fr;gap: 24px;margin-top: 23px;}
.hf-lf .methodgrid p,.hf-lf .methodgrid li{font-size: 13px;color: var(--ink2);}
.hf-lf ul{padding-left: 19px;margin: 10px 0;}
.hf-lf li{margin: 7px 0;}
.hf-lf details{border-top: 1px solid var(--bd-2);padding: 15px 0;}
.hf-lf summary{cursor: pointer;font-size: 13px;font-weight: 600;}
.hf-lf details p{font-size: 13px;color: var(--ink2);margin-top: 12px;}
.hf-lf .keyline{display: flex;justify-content: space-between;gap: 20px;border-bottom: 1px solid var(--bd-2);}
.hf-lf .sampleflag{color: var(--ink);font-size: 10px;text-transform: uppercase;letter-spacing: .08em;}
.hf-lf .printbutton{white-space: nowrap;}
@media (max-width:700px){
.hf-lf .split,.hf-lf .factpair,.hf-lf .methodgrid{grid-template-columns: 1fr;gap: 20px;}
.hf-lf .stats{gap: 8px;}
.hf-lf .barrow{gap: 7px;}
.hf-lf .journey{grid-template-columns: repeat(3,1fr);}
.hf-lf .sectiontag{display: none;}
.hf-lf .reviewbar{gap: 10px;}
.hf-lf .reviewbar .label,.hf-lf .reviewbar .spacer,.hf-lf .printbutton{display: none;}
.hf-lf .reviewbar select{flex: 1;}
.hf-lf .intro{flex-direction: column;gap: 3px;}
.hf-lf .publisher{font-size: 14px;}
.hf-lf .brand{font-size: 17px;}
.hf-lf .footer{font-size: 10px;}
}
@media (max-width:420px){
.hf-lf .report{padding: 0 8px;}
.hf-lf .stats{grid-template-columns: 1fr;}
.hf-lf .stat{grid-template-columns: 92px 1fr;column-gap: 12px;}
.hf-lf .stat .value{grid-row: 1/3;}
.hf-lf .stat .name{margin: 0;}
.hf-lf .stat .detail{margin-top: 4px;}
.hf-lf .brandmark{width: 24px;height: 24px;font-size: 18px;}
.hf-lf .masthead{gap: 10px;}
.hf-lf .reviewbar select{flex-basis: 100%;}
.hf-lf .reviewbar .counter{display: none;}
.hf-lf .actionpanel{padding: 20px;}
.hf-lf .footer{flex-wrap: wrap;}
.hf-lf .factpair{gap: 10px;}
}
@media print{
.hf-lf{font-size: 12px;}
.hf-lf .reviewbar,.hf-lf .intro,.hf-lf .linkbutton{display: none !important;}
.hf-lf .report{max-width: none;margin: 0;padding: 0;}
.hf-lf .sheet,.hf-lf .sheet[hidden]{display: block !important;margin: 0;box-shadow: none;min-height: 0;padding: 0;break-after: page;}
.hf-lf .sheet:last-child{break-after: auto;}
.hf-lf h1{font-size: 37px;}
.hf-lf h2{font-size: 32px;}
.hf-lf .block,.hf-lf .split,.hf-lf .actionitem,.hf-lf .evidence,.hf-lf .factpair,.hf-lf tr{break-inside: avoid;}
.hf-lf .sheet{print-color-adjust: exact;-webkit-print-color-adjust: exact;}
.hf-lf .footer{margin-top: 20px;}
.hf-lf .stats{margin: 20px 0;}
.hf-lf .stat{padding: 15px;}
}
.hf-lf{--s-page: #edeae5;--s-main: #ffffff;--s-raised: #faf9f5;--s-hover: #f0eee9;--s-hover2: #e9e6e1;--s-active: #eae7e1;--ink: #1f1e1d;--ink-prose: #3a3937;--ink2: #666666;--ink3: #999999;--ink4: #bbbbbb;--bd-1: rgba(31, 30, 29, 0.07);--bd-2: rgba(31, 30, 29, 0.1);--bd-3: rgba(31, 30, 29, 0.14);--bd-4: rgba(31, 30, 29, 0.22);--btn-bg: #1f1e1d;--btn-fg: #ffffff;--ok: #10b981;--danger: #ef4444;--rec: #ff5f57;--hdr: rgba(237, 234, 229, 0.86);--accent: #1f1e1d;--nav-active: var(--s-main);--logo-i: 0;--shadow-sm: 0 1px 2px rgba(31, 30, 29, 0.06);--shadow-md: 0 4px 12px rgba(31, 30, 29, 0.07);--shadow-xl: 0 24px 48px rgba(31, 30, 29, 0.12);color-scheme: light;}
.hf-lf{--green: #047857;--risk: #b42318;--signal-bg: #fcece9;--positive-bg: #e9f5ef;--emphasis-bg: #1f1e1d;--emphasis-ink: #ffffff;--emphasis-muted: #d2d0cd;--emphasis-line: #ffffff28;--sans: Inter,system-ui,sans-serif;--blue: #a06e51;--violet: #6e7d55;}
.hf-lf{background: var(--s-page);color: var(--ink);font-family: var(--sans);}
.hf-lf h1,.hf-lf h2,.hf-lf h3,.hf-lf blockquote,.hf-lf .quote,.hf-lf .ordinal{font-family: var(--sans);font-weight: 500;}
.hf-lf h1{line-height: 1.13;}
.hf-lf h2,.hf-lf h3{letter-spacing: -.025em;}
.hf-lf button,.hf-lf select{border: 1px solid var(--bd-3);border-radius: 8px;background: var(--s-main);color: var(--ink);font: 500 12px var(--sans);min-height: 30px;padding: 6px 10px;}
.hf-lf button:hover,.hf-lf select:hover{background: var(--s-hover);}
.hf-lf button:disabled{opacity: .4;cursor: default;}
.hf-lf button:focus-visible,.hf-lf select:focus-visible,.hf-lf a:focus-visible,.hf-lf summary:focus-visible{outline: 2px solid var(--ink);outline-offset: 3px;}
.hf-lf .sample,.hf-lf .sampleflag{color: var(--ink2);}
.hf-lf .preview-tools{display: flex;align-items: center;gap: 12px;flex-wrap: wrap;}
.hf-lf .hf-publisher{display: inline-flex;align-items: center;gap: 6px;color: var(--ink);font: 600 16px var(--sans);letter-spacing: -.04em;}
.hf-lf .hf-publisher svg{width: 18px;height: 18px;margin-right: 2px;}
.hf-lf .hf-publisher .aeo{font-size: 11px;font-weight: 500;letter-spacing: 0;color: var(--ink2);margin: 0;padding-left: 7px;border-left: 1px solid var(--bd-3);}
.hf-lf .track{background: var(--s-hover2);border-radius: 99px;overflow: hidden;}
.hf-lf .fill,.hf-lf .fill.own{background: var(--ink);border-radius: 99px;}
.hf-lf .fill:not(.own){background: var(--ink3);}
.hf-lf .swatch{background: var(--ink3);}
.hf-lf .swatch.own{background: var(--ink);}
.hf-lf .swatch.neutral{background: var(--s-hover2);}
.hf-lf .zero{color: var(--risk);}
.hf-lf .gain{color: var(--green);}
@media print{
.hf-lf{--s-page: #fff;--s-main: #fff;--s-raised: #faf9f5;--s-hover: #f0eee9;--s-hover2: #e9e6e1;--ink: #1f1e1d;--ink-prose: #3a3937;--ink2: #666;--ink3: #999;--bd-1: #1f1e1d12;--bd-2: #1f1e1d1a;--bd-3: #1f1e1d24;--green: #047857;--risk: #b42318;--signal-bg: #fcece9;--positive-bg: #e9f5ef;--emphasis-bg: #1f1e1d;--emphasis-ink: #fff;--emphasis-muted: #d2d0cd;--emphasis-line: #ffffff28;color-scheme: light;}
.hf-lf{background: #fff;}
}
.hf-lf .reviewbar{background: var(--s-page);color: var(--ink);box-shadow: none;border-bottom: 1px solid var(--bd-2);padding: 14px 24px;gap: 10px;}
.hf-lf .reviewbar .label{color: var(--ink2);font-size: 10px;font-weight: 500;}
.hf-lf .reviewbar select,.hf-lf .reviewbar button{background: var(--s-main);color: var(--ink);border: 1px solid var(--bd-3);border-radius: 8px;padding: 7px 10px;font-size: 12px;}
.hf-lf .reviewbar button[aria-pressed=true]{background: var(--ink);color: var(--s-main);}
.hf-lf .reviewbar .counter{color: var(--ink2);font-size: 11px;}
.hf-lf .report{max-width: 1040px;}
.hf-lf .intro{max-width: 1040px;font-size: 11px;margin: 22px auto 18px;}
.hf-lf .intro strong{font-weight: 500;}
.hf-lf .sheet{border-radius: 16px;padding: 34px 44px 28px;background: var(--s-main);box-shadow: 0 4px 24px #00000006;}
.hf-lf .masthead{padding-bottom: 16px;}
.hf-lf .brand{font-size: 17px;font-weight: 500;letter-spacing: -.035em;}
.hf-lf .brandmark{width: 27px;height: 27px;font: 500 12px var(--sans);background: var(--s-raised);color: var(--ink2);border: 1px solid var(--bd-2);border-radius: 8px;}
.hf-lf .sectiontag{font-size: 9px;color: var(--ink2);}
.hf-lf .kicker{color: var(--ink2);font-weight: 500;font-size: 10px;margin: 26px 0 12px;}
.hf-lf h1{font: 500 clamp(30px,4vw,40px)/1.13 var(--sans);letter-spacing: -.045em;}
.hf-lf h2{font: 500 clamp(27px,3.2vw,34px)/1.16 var(--sans);letter-spacing: -.04em;}
.hf-lf h3{font: 500 18px/1.3 var(--sans);letter-spacing: -.025em;margin-bottom: 12px;}
.hf-lf .dek{font-size: 14px;line-height: 1.6;color: var(--ink-prose);max-width: 780px;}
.hf-lf .scope{font-size: 11px;}
.hf-lf .stats{gap: 12px;margin: 24px 0;}
.hf-lf .stat{border-radius: 12px;border: 1px solid var(--bd-2);padding: 16px;background: var(--s-raised);display: flex;flex-direction: column;}
.hf-lf .stat .name{order: -1;color: var(--ink2);font-size: 10px;font-weight: 500;letter-spacing: .06em;text-transform: uppercase;margin: 0 0 12px;}
.hf-lf .stat .value{font: 500 36px/1.1 var(--sans);letter-spacing: -.04em;font-variant-numeric: tabular-nums;}
.hf-lf .stat .detail{font-size: 11px;line-height: 1.6;margin-top: 10px;}
.hf-lf .split{gap: 24px;margin-top: 24px;}
.hf-lf .split > div{min-width: 0;}
.hf-lf .block{margin-top: 26px;}
.hf-lf .caption,.hf-lf .fine{font-size: 11px;line-height: 1.6;}
.hf-lf .eyebrow{font-size: 10px;letter-spacing: .1em;color: var(--ink2);}
.hf-lf .barrow{font-size: 12px;grid-template-columns: 140px 1fr 53px;gap: 10px;}
.hf-lf .track{height: 7px;}
.hf-lf .narrative{font-size: 13px;color: var(--ink-prose);line-height: 1.7;}
.hf-lf .keyline{font-size: 12px;padding: 12px 0;}
.hf-lf .keyline strong{font-weight: 500;}
.hf-lf .evidence{border: 1px solid var(--bd-2);background: var(--s-raised);border-radius: 12px;padding: 18px;margin-top: 24px;}
.hf-lf .quote,.hf-lf .quote.small{font: 500 17px/1.5 var(--sans);letter-spacing: -.015em;}
.hf-lf .evidence .answer{font-size: 12px;line-height: 1.65;}
.hf-lf .evidence .result{color: var(--risk);font-weight: 500;}
.hf-lf .linkbutton{border: none;background: transparent;padding: 8px 0;font-weight: 500;color: var(--ink);}
.hf-lf .actionpanel{background: var(--emphasis-bg);color: var(--emphasis-ink);border-radius: 12px;padding: 22px;}
.hf-lf .actionpanel h3{color: var(--emphasis-ink);font-size: 18px;}
.hf-lf .actionpanel p,.hf-lf .actionpanel .eyebrow{color: var(--emphasis-muted);}
.hf-lf .actionpanel p{font-size: 13px;line-height: 1.7;}
.hf-lf .tablewrap{border: 1px solid var(--bd-2);border-radius: 12px;}
.hf-lf table{font-size: 12px;}
.hf-lf th{background: var(--s-raised);font-size: 9px;text-transform: uppercase;letter-spacing: .08em;font-weight: 500;padding: 12px;}
.hf-lf td{padding: 12px;border-color: var(--bd-1);}
.hf-lf th:first-child,.hf-lf td:first-child{padding-left: 12px;}
.hf-lf tbody tr:last-child td{border-bottom: 0;}
.hf-lf .subject{font-weight: 500;}
.hf-lf .sub{font-size: 10px;}
.hf-lf .highlight td{background: var(--s-raised);}
.hf-lf .highlight td:first-child{padding-left: 12px;}
.hf-lf .finding{border-left: 2px solid var(--ink3);padding-left: 16px;}
.hf-lf .finding strong{font-size: 15px;font-weight: 500;}
.hf-lf .finding p{font-size: 13px;line-height: 1.7;}
.hf-lf .note,.hf-lf .fact{border-radius: 12px;border: 1px solid var(--bd-2);background: var(--s-raised);}
.hf-lf .note{padding: 16px;font-size: 12px;line-height: 1.7;}
.hf-lf .fact.correct{background: var(--positive-bg);}
.hf-lf .pill{border: 1px solid var(--bd-2);border-radius: 99px;background: var(--s-raised);padding: 4px 8px;font-size: 10px;}
.hf-lf .pill.risk{background: var(--signal-bg);color: var(--risk);}
.hf-lf .pill.good{background: var(--positive-bg);color: var(--green);}
.hf-lf .stage{border: 1px solid var(--bd-2);border-radius: 10px;padding: 12px 9px;}
.hf-lf .stage b{font-variant-numeric: tabular-nums;font-size: 21px;letter-spacing: -.035em;}
.hf-lf .stage .stagelabel{font-size: 10px;}
.hf-lf .stage span{font-size: 9px;}
.hf-lf .heat{border-radius: 6px;font-size: 11px;}
.hf-lf .ordinal{font: 500 24px var(--sans);color: var(--ink3);}
.hf-lf .actionitem h3{font-size: 19px;}
.hf-lf .researchlabel{color: var(--ink2);}
.hf-lf .actionitem p,.hf-lf .methodgrid p,.hf-lf .methodgrid li{color: var(--ink-prose);line-height: 1.7;}
.hf-lf .methodgrid h3{font-size: 18px;}
.hf-lf .footer{color: var(--ink2);font-size: 9px;}
@media (min-width:900px){
.hf-lf .sheet{min-height: 1010px;}
}
@media (max-width:700px){
.hf-lf .sheet{padding: 26px 24px;}
.hf-lf .reviewbar{padding: 12px;}
.hf-lf .reviewbar .label{display: none;}
.hf-lf .stat{padding: 13px;}
.hf-lf .stat .value{font-size: 29px;}
.hf-lf .stat .name{font-size: 9px;}
.hf-lf .barrow{grid-template-columns: 120px 1fr 48px;}
.hf-lf .split{gap: 22px;}
}
@media (max-width:420px){
.hf-lf .sheet{padding: 24px 18px;}
.hf-lf .stat{display: flex;}
.hf-lf .stat .name{margin-bottom: 8px;}
.hf-lf .sectiontag{display: none;}
.hf-lf .barrow{grid-template-columns: 110px 1fr 45px;}
.hf-lf .hf-publisher{font-size: 13px;}
.hf-lf .hf-publisher svg{width: 15px;height: 15px;}
.hf-lf .hf-publisher .aeo{font-size: 9px;}
}
@media print{
.hf-lf .sheet,.hf-lf .sheet[hidden]{border-radius: 0;box-shadow: none;padding: 0;min-height: 0;}
.hf-lf .reviewbar{display: none;}
}
.hf-lf{--ink:#0a0a0a;--ink-prose:#3f3f3f;--ink2:#5c5c5c;--ink3:#a3a3a3;--bd-1:#efefed;--bd-2:#e7e7e5;--bd-3:#d9d9d6;--s-raised:#f8f8f7;--s-hover2:#ececea;--emphasis-bg:#0a0a0a;--hf-orange:#ff5a00;--hf-orange-dark:#c74600;--hf-orange-tint:#fff1e8;}
@media print{
.hf-lf{--ink:#0a0a0a;--ink2:#5c5c5c;--bd-2:#e7e7e5;--s-raised:#f8f8f7;--emphasis-bg:#0a0a0a;}
}
.hf-lf{-webkit-font-smoothing:antialiased;}
.hf-lf a:hover{color:var(--hf-orange);}
.hf-lf .hf-publisher{gap:10px;color:var(--ink);}
.hf-lf .hf-publisher svg.hf-wordmark{width:auto;height:20px;margin:0;display:block;}
.hf-lf .hf-publisher .aeo{font-size:11px;padding-left:10px;color:var(--ink2);}
.hf-lf{font-size:15px;line-height:1.6;}
.hf-lf .intro{margin:28px auto 22px;font-size:12px;}
.hf-lf .reviewbar{padding:16px 28px;gap:12px;}
.hf-lf .masthead{padding-bottom:22px;}
.hf-lf .kicker{display:flex;align-items:center;gap:10px;margin:56px 0 18px;font-size:11px;letter-spacing:.12em;}
.hf-lf .kicker::before{content:"";width:6px;height:6px;border-radius:2px;background:var(--hf-orange);flex:none;}
.hf-lf h1{font-size:clamp(32px,4.2vw,44px);line-height:1.1;}
.hf-lf h2{font-size:clamp(28px,3.4vw,36px);line-height:1.15;}
.hf-lf h3{font-size:19px;margin-bottom:18px;}
.hf-lf .dek{margin-top:22px;font-size:16px;line-height:1.65;max-width:720px;text-wrap:pretty;}
.hf-lf .scope{margin-top:18px;font-size:12px;}
.hf-lf .stats{gap:18px;margin:44px 0;}
.hf-lf .stat{padding:24px 22px;}
.hf-lf .stat .name{font-size:11px;margin-bottom:16px;}
.hf-lf .stat .value{font-size:40px;}
.hf-lf .stat .detail{font-size:12.5px;margin-top:14px;}
.hf-lf .split{gap:56px;margin-top:52px;}
.hf-lf .block{margin-top:56px;}
.hf-lf .bars{margin-top:20px;}
.hf-lf .barrow{margin:20px 0;font-size:13px;gap:14px;grid-template-columns:150px 1fr 56px;}
.hf-lf .track{height:8px;}
.hf-lf .fill.own{background:var(--hf-orange);}
.hf-lf .caption,.hf-lf .fine{font-size:12px;line-height:1.65;margin:14px 0;}
.hf-lf .narrative{font-size:14px;line-height:1.75;margin-top:16px;text-wrap:pretty;}
.hf-lf .keyline{font-size:13px;padding:16px 0;}
.hf-lf .evidence{padding:28px;margin-top:44px;}
.hf-lf .evidence .eyebrow{margin-bottom:14px;}
.hf-lf .quote,.hf-lf .quote.small{font-size:18px;line-height:1.55;margin-top:4px;}
.hf-lf .evidence .answer{font-size:13px;line-height:1.7;margin-top:14px;}
.hf-lf .evidence .result{font-size:13px;margin-top:12px;}
.hf-lf .evidence h3{margin-bottom:6px;}
.hf-lf .linkbutton{font-size:13px;margin-top:10px;}
.hf-lf .linkbutton:hover{color:var(--hf-orange);background:transparent;}
.hf-lf .actionpanel{margin-top:44px;padding:30px 32px;}
.hf-lf .actionpanel h3{font-size:20px;margin-bottom:12px;}
.hf-lf .actionpanel p{font-size:14px;line-height:1.75;}
.hf-lf .actionpanel .eyebrow{color:#ffb98f;margin-bottom:14px;}
.hf-lf .eyebrow{font-size:11px;margin-bottom:12px;}
.hf-lf .tablewrap{margin-top:28px;}
.hf-lf table{font-size:13px;}
.hf-lf th{font-size:10px;padding:14px 16px;}
.hf-lf td{padding:16px;}
.hf-lf th:first-child,.hf-lf td:first-child,.hf-lf .highlight td:first-child{padding-left:18px;}
.hf-lf .sub{font-size:11px;margin-top:4px;}
.hf-lf .highlight td{background:var(--hf-orange-tint);}
.hf-lf .finding{margin:40px 0;padding:4px 0 4px 20px;border-left:2px solid var(--hf-orange);}
.hf-lf .finding strong{font-size:16px;}
.hf-lf .finding p{font-size:14px;margin-top:10px;}
.hf-lf .note{margin-top:40px;padding:22px 24px;font-size:13px;line-height:1.75;}
.hf-lf .pill{padding:5px 10px;font-size:11px;}
.hf-lf .journey{gap:12px;margin:24px 0 16px;}
.hf-lf .stage{padding:16px 14px;}
.hf-lf .stage .stagelabel{font-size:11px;}
.hf-lf .stage b{font-size:23px;margin:10px 0;}
.hf-lf .stage span{font-size:10.5px;}
.hf-lf .heat{font-size:12px;padding:7px 10px;}
.hf-lf .factpair{gap:18px;margin-top:20px;}
.hf-lf .fact{padding:20px;font-size:14px;line-height:1.6;}
.hf-lf .fact .eyebrow{margin-bottom:8px;}
.hf-lf .outcomebar{margin:22px 0 12px;}
.hf-lf .researchlabel{font-size:11px;}
.hf-lf .actionitem{padding:36px 0;gap:22px;grid-template-columns:44px 1fr;}
.hf-lf .actionitem h3{font-size:20px;margin-bottom:10px;}
.hf-lf .actionmeta{margin:14px 0 16px;gap:8px;}
.hf-lf .actionitem p{font-size:14px;margin-top:12px;}
.hf-lf .ordinal{color:var(--hf-orange);}
.hf-lf .methodgrid{gap:48px;margin-top:40px;}
.hf-lf .methodgrid p,.hf-lf .methodgrid li{font-size:14px;}
.hf-lf li{margin:10px 0;}
.hf-lf ul{margin:14px 0;}
.hf-lf details{padding:20px 0;}
.hf-lf summary{font-size:14px;}
.hf-lf details p{font-size:14px;line-height:1.7;margin-top:14px;}
.hf-lf .footer{margin-top:64px;padding-top:18px;font-size:10.5px;}
@media screen{
.hf-lf .sheet{padding:52px 64px 40px;margin-bottom:36px;}
}
@media (max-width:700px){
.hf-lf .sheet{padding:32px 26px;}
.hf-lf .split,.hf-lf .methodgrid{gap:36px;}
.hf-lf .stats{gap:12px;}
.hf-lf .barrow{grid-template-columns:120px 1fr 48px;}
.hf-lf .journey{grid-template-columns:repeat(3,1fr);}
}
@media (max-width:420px){
.hf-lf .sheet{padding:26px 18px;}
.hf-lf .hf-publisher svg.hf-wordmark{height:16px;}
.hf-lf .kicker{margin-top:40px;}
}

.hf-op,.hf-op *{box-sizing: border-box;}
.hf-op{margin: 0;font: 14px/1.45 -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;-webkit-print-color-adjust: exact;print-color-adjust: exact;}
.hf-op .preview-bar{display: flex;align-items: center;justify-content: space-between;gap: 16px;color: var(--ink2);font-size: 12px;}
.hf-op .preview-bar span{display: block;}
.hf-op .preview-bar strong{color: var(--ink);}
.hf-op button{flex-shrink: 0;border: 1px solid var(--bd-3);border-radius: 6px;padding: 9px 14px;background: var(--s-main);color: var(--ink);font: inherit;cursor: pointer;}
.hf-op button:focus-visible{outline: 3px solid var(--ink);outline-offset: 3px;}
.hf-op .report{width: 816px;min-height: 1056px;margin: 0 auto 32px;background: var(--s-main);}
.hf-op .masthead{display: flex;align-items: center;justify-content: space-between;border-bottom: 1px solid var(--bd-2);}
.hf-op .brand span{display: block;margin-top: 3px;color: var(--ink2);letter-spacing: 1.3px;text-transform: uppercase;}
.hf-op .publisher{text-align: right;font-size: 20px;font-weight: 700;letter-spacing: -.8px;}
.hf-op .publisher .aeo{color: var(--ink);font-weight: 500;font-size: 13px;letter-spacing: 0;}
.hf-op .publisher small{display: block;letter-spacing: 1.2px;text-transform: uppercase;color: var(--ink2);}
.hf-op .eyebrow{display: flex;justify-content: space-between;gap: 16px;color: var(--ink2);letter-spacing: 1.3px;text-transform: uppercase;}
.hf-op .sample{color: var(--ink);}
.hf-op h1{margin: 0;font-weight: 400;}
.hf-op h1 em{font-style: normal;}
.hf-op .dek{margin: 10px 0 0;max-width: 640px;color: var(--ink2);}
.hf-op .scope{border-top: 1px solid var(--bd-2);border-bottom: 1px solid var(--bd-2);display: flex;flex-wrap: wrap;row-gap: 5px;color: var(--ink2);}
.hf-op .scope b{color: var(--ink);font-weight: 600;}
.hf-op .metrics{display: grid;grid-template-columns: repeat(3, 1fr);}
.hf-op .metric-label{margin: 0 0 4px;}
.hf-op .metric-value{line-height: 1.15;font-variant-numeric: tabular-nums;}
.hf-op .metric-detail{margin: 5px 0 0;color: var(--ink2);}
.hf-op .recognition{display: flex;gap: 8px;margin-bottom: 0;padding: 0 1px;color: var(--ink2);}
.hf-op .recognition strong{color: var(--ink);font-weight: 600;}
.hf-op .section-heading{display: flex;align-items: baseline;justify-content: space-between;gap: 12px;}
.hf-op h2{margin: 0;}
.hf-op .section-number{margin-right: 8px;font: 10px/1 -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;letter-spacing: .7px;}
.hf-op .section-note{margin: 0;color: var(--ink2);}
.hf-op table{width: 100%;border-collapse: collapse;table-layout: fixed;}
.hf-op caption{position: absolute;width: 1px;height: 1px;overflow: hidden;clip-path: inset(50%);}
.hf-op th{text-align: left;color: var(--ink2);text-transform: uppercase;padding: 7px 0;border-bottom: 1px solid var(--bd-2);vertical-align: bottom;}
.hf-op th:nth-child(1){width: 36%;}
.hf-op th:nth-child(2){width: 27%;}
.hf-op th:nth-child(3){width: 37%;padding-left: 18px;}
.hf-op td{border-bottom: 1px solid var(--bd-2);vertical-align: middle;}
.hf-op td:nth-child(3){padding-left: 18px;}
.hf-op .segment{display: block;}
.hf-op .segment-note{display: block;color: var(--ink2);font-size: 10px;margin-top: 1px;}
.hf-op .bar-line{display: flex;align-items: center;gap: 9px;}
.hf-op .track{height: 5px;flex: 1;}
.hf-op .fill{height: 100%;background: var(--green);}
.hf-op .bar-value{white-space: nowrap;font-variant-numeric: tabular-nums;}
.hf-op .competitor{font-weight: 500;}
.hf-op td small{display: block;color: var(--ink2);font-size: 10px;font-weight: 400;margin-top: 1px;}
.hf-op .table-foot{margin: 7px 0 0;color: var(--ink2);}
.hf-op .evidence{display: grid;grid-template-columns: 1.1fr 1fr;border-left: 3px solid var(--ink);}
.hf-op blockquote{margin: 0;}
.hf-op .evidence-label{margin: 0 0 5px;color: var(--ink2);text-transform: uppercase;}
.hf-op .outcome{margin: 0;}
.hf-op .outcome strong{font-weight: 600;}
.hf-op .engine-row{margin: 7px 0 0;color: var(--ink2);}
.hf-op .next-step{display: grid;grid-template-columns: 1.5fr 1fr;gap: 18px;}
.hf-op .next-step .label{color: var(--emphasis-muted);letter-spacing: 1.1px;text-transform: uppercase;margin: 0 0 6px;}
.hf-op .next-step p{margin: 6px 0 0;line-height: 1.5;color: var(--emphasis-muted);}
.hf-op .invitation{border-left: 1px solid var(--emphasis-line);}
.hf-op .invitation strong{display: block;font-weight: 600;}
.hf-op .method{margin: 10px 0 0;font-size: 9px;line-height: 1.5;color: var(--ink2);}
.hf-op footer{display: flex;justify-content: space-between;gap: 16px;border-top: 1px solid var(--bd-2);margin-top: 9px;padding-top: 9px;color: var(--ink2);font-size: 9px;}
@media screen and (max-width: 590px){
.hf-op .recognition span{display: block;margin-top: 3px;}
}
@media print{
.hf-op .preview-bar{display: none;}
.hf-op .report{width: 8.5in;min-height: 11in;margin: 0;box-shadow: none;}
.hf-op section,.hf-op .metrics,.hf-op .next-step{break-inside: avoid;}
}
@media screen and (max-width: 850px){
.hf-op .preview-bar{margin: 16px;}
.hf-op .report{width: calc(100% - 28px);padding: 30px;min-height: auto;}
}
@media screen and (max-width: 590px){
.hf-op .report{padding: 24px 20px;}
.hf-op h1{font-size: 33px;}
.hf-op .brand{font-size: 16px;}
.hf-op .publisher{font-size: 17px;}
.hf-op .eyebrow{flex-wrap: wrap;}
.hf-op .metrics{grid-template-columns: 1fr;gap: 8px;}
.hf-op .metric{display: grid;grid-template-columns: 1fr auto;align-items: center;gap: 0 12px;}
.hf-op .metric-value{grid-column: 2;grid-row: 1 / 3;font-size: 31px;}
.hf-op .metric-detail{margin: 0;}
.hf-op .recognition{display: block;}
.hf-op .section-heading{display: block;}
.hf-op .section-note{margin-top: 5px;}
.hf-op h2{font-size: 21px;}
.hf-op th{font-size: 8px;letter-spacing: .2px;}
.hf-op td{font-size: 10px;}
.hf-op th:nth-child(1){width: 33%;}
.hf-op th:nth-child(2){width: 30%;}
.hf-op th:nth-child(3){width: 37%;padding-left: 12px;}
.hf-op td:nth-child(3){padding-left: 12px;}
.hf-op .bar-line{flex-wrap: wrap;gap: 3px;}
.hf-op .bar-value{width: 100%;}
.hf-op .track{flex-basis: 100%;max-width: 75px;}
.hf-op .evidence,.hf-op .next-step{grid-template-columns: 1fr;gap: 16px;}
.hf-op .invitation{border-left: 0;border-top: 1px solid var(--emphasis-line);padding: 12px 0 0;}
.hf-op footer{flex-wrap: wrap;}
}
.hf-op{--s-page: #edeae5;--s-main: #ffffff;--s-raised: #faf9f5;--s-hover: #f0eee9;--s-hover2: #e9e6e1;--s-active: #eae7e1;--ink: #1f1e1d;--ink-prose: #3a3937;--ink2: #666666;--ink3: #999999;--ink4: #bbbbbb;--bd-1: rgba(31, 30, 29, 0.07);--bd-2: rgba(31, 30, 29, 0.1);--bd-3: rgba(31, 30, 29, 0.14);--bd-4: rgba(31, 30, 29, 0.22);--btn-bg: #1f1e1d;--btn-fg: #ffffff;--ok: #10b981;--danger: #ef4444;--rec: #ff5f57;--hdr: rgba(237, 234, 229, 0.86);--accent: #1f1e1d;--nav-active: var(--s-main);--logo-i: 0;--shadow-sm: 0 1px 2px rgba(31, 30, 29, 0.06);--shadow-md: 0 4px 12px rgba(31, 30, 29, 0.07);--shadow-xl: 0 24px 48px rgba(31, 30, 29, 0.12);color-scheme: light;}
.hf-op{--green: #047857;--risk: #b42318;--signal-bg: #fcece9;--positive-bg: #e9f5ef;--emphasis-bg: #1f1e1d;--emphasis-ink: #ffffff;--emphasis-muted: #d2d0cd;--emphasis-line: #ffffff28;--sans: Inter,system-ui,sans-serif;--blue: #a06e51;--violet: #6e7d55;}
.hf-op{background: var(--s-page);color: var(--ink);font-family: var(--sans);}
.hf-op h1,.hf-op h2,.hf-op h3,.hf-op blockquote,.hf-op .quote,.hf-op .ordinal{font-family: var(--sans);font-weight: 500;}
.hf-op h1{line-height: 1.13;}
.hf-op h2,.hf-op h3{letter-spacing: -.025em;}
.hf-op button,.hf-op select{border: 1px solid var(--bd-3);border-radius: 8px;background: var(--s-main);color: var(--ink);font: 500 12px var(--sans);min-height: 30px;padding: 6px 10px;}
.hf-op button:hover,.hf-op select:hover{background: var(--s-hover);}
.hf-op button:disabled{opacity: .4;cursor: default;}
.hf-op button:focus-visible,.hf-op select:focus-visible,.hf-op a:focus-visible,.hf-op summary:focus-visible{outline: 2px solid var(--ink);outline-offset: 3px;}
.hf-op .sample,.hf-op .sampleflag{color: var(--ink2);}
.hf-op .preview-tools{display: flex;align-items: center;gap: 12px;flex-wrap: wrap;}
.hf-op .hf-publisher{display: inline-flex;align-items: center;gap: 6px;color: var(--ink);font: 600 16px var(--sans);letter-spacing: -.04em;}
.hf-op .hf-publisher svg{width: 18px;height: 18px;margin-right: 2px;}
.hf-op .hf-publisher .aeo{font-size: 11px;font-weight: 500;letter-spacing: 0;color: var(--ink2);margin: 0;padding-left: 7px;border-left: 1px solid var(--bd-3);}
.hf-op .track{background: var(--s-hover2);border-radius: 99px;overflow: hidden;}
.hf-op .fill,.hf-op .fill.own{background: var(--ink);border-radius: 99px;}
.hf-op .fill:not(.own){background: var(--ink3);}
.hf-op .swatch{background: var(--ink3);}
.hf-op .swatch.own{background: var(--ink);}
.hf-op .swatch.neutral{background: var(--s-hover2);}
.hf-op .zero{color: var(--risk);}
.hf-op .gain{color: var(--green);}
@media print{
.hf-op{--s-page: #fff;--s-main: #fff;--s-raised: #faf9f5;--s-hover: #f0eee9;--s-hover2: #e9e6e1;--ink: #1f1e1d;--ink-prose: #3a3937;--ink2: #666;--ink3: #999;--bd-1: #1f1e1d12;--bd-2: #1f1e1d1a;--bd-3: #1f1e1d24;--green: #047857;--risk: #b42318;--signal-bg: #fcece9;--positive-bg: #e9f5ef;--emphasis-bg: #1f1e1d;--emphasis-ink: #fff;--emphasis-muted: #d2d0cd;--emphasis-line: #ffffff28;color-scheme: light;}
.hf-op{background: #fff;}
}
.hf-op .preview-bar{max-width: 880px;padding: 0 4px;flex-wrap: wrap;margin: 22px auto 18px;font: 12px/1.5 var(--sans);}
.hf-op .preview-bar strong{font-weight: 500;}
.hf-op .report{padding: 28px 36px 18px;border-radius: 16px;box-shadow: 0 4px 24px #00000006;}
.hf-op .masthead{padding-bottom: 13px;}
.hf-op .brand{font-weight: 500;font-size: 18px;letter-spacing: -.035em;}
.hf-op .brand span{font-size: 9px;font-weight: 500;}
.hf-op .publisher small{font-size: 9px;font-weight: 400;margin-top: 5px;}
.hf-op h1{font: 500 34px/1.12 var(--sans);letter-spacing: -.045em;max-width: 740px;}
.hf-op h1 em{color: var(--ink2);}
.hf-op .eyebrow{margin: 14px 0 10px;font-weight: 500;font-size: 9px;}
.hf-op .dek{font-size: 12px;line-height: 1.5;}
.hf-op .scope{font-size: 9px;padding: 8px 0;margin: 9px 0 12px;column-gap: 12px;}
.hf-op .metrics{gap: 10px;}
.hf-op .metric{border: 1px solid var(--bd-2);border-radius: 12px;padding: 13px 13px 12px;background: var(--s-raised);}
.hf-op .metric-label{font-size: 9px;color: var(--ink2);font-weight: 500;letter-spacing: .045em;text-transform: uppercase;margin-bottom: 9px;}
.hf-op .metric-value{font-size: 34px;font-weight: 500;letter-spacing: -.04em;}
.hf-op .metric-detail{font-size: 9px;line-height: 1.5;margin-top: 7px;}
.hf-op .recognition{font-size: 10px;line-height: 1.5;margin-top: 11px;}
.hf-op h2{font: 500 18px/1.25 var(--sans);letter-spacing: -.025em;}
.hf-op .section-number{color: var(--ink3);}
.hf-op .section-note{font-size: 9px;}
.hf-op th{font-size: 9px;letter-spacing: .08em;font-weight: 500;}
.hf-op td{padding: 9px 0;font-size: 10px;}
.hf-op .segment{font-weight: 500;}
.hf-op .segment-note,.hf-op td small{font-size: 9px;}
.hf-op .bar-value{font-size: 10px;min-width: 83px;}
.hf-op .table-foot{font-size: 8.5px;line-height: 1.45;}
.hf-op .evidence{background: var(--s-raised);border: 1px solid var(--bd-2);border-radius: 12px;padding: 13px 14px;gap: 18px;}
.hf-op .evidence-label{font-size: 8px;letter-spacing: .09em;}
.hf-op blockquote{font: 500 14px/1.45 var(--sans);letter-spacing: -.015em;}
.hf-op .outcome{font-size: 10px;line-height: 1.55;}
.hf-op .engine-row{font-size: 8px;}
.hf-op .next-step{border-radius: 12px;padding: 15px 17px;background: var(--emphasis-bg);color: var(--emphasis-ink);}
.hf-op .next-step h2{color: var(--emphasis-ink);font-size: 17px;}
.hf-op .next-step .label,.hf-op .next-step p{color: var(--emphasis-muted);}
.hf-op .next-step p{font-size: 9px;}
.hf-op .next-step .label{font-size: 8px;}
.hf-op .invitation{border-color: var(--emphasis-line);padding-left: 17px;}
.hf-op .invitation strong{font-size: 11px;}
.hf-op .method,.hf-op footer{font-size: 8px;line-height: 1.45;}
@media screen and (max-width:590px){
.hf-op h1{font-size: 29px;}
.hf-op .preview-bar{margin: 16px;}
.hf-op .report{padding: 24px 20px;}
.hf-op .metric-label{margin-bottom: 4px;}
.hf-op .evidence,.hf-op .next-step{gap: 13px;}
.hf-op .invitation{border-top-color: var(--emphasis-line);padding-left: 0;}
}
@media print{
.hf-op .report{border-radius: 0;padding: 28px 36px 18px;}
}
.hf-op .bar-line .fill{background: var(--ink);}
.hf-op td{padding-top: 6px;padding-bottom: 6px;}
.hf-op section{margin-top: 12px;}
.hf-op .next-step{margin-top: 12px;}
.hf-op .section-heading{margin-bottom: 8px;}
.hf-op{--ink:#0a0a0a;--ink-prose:#3f3f3f;--ink2:#5c5c5c;--ink3:#a3a3a3;--bd-1:#efefed;--bd-2:#e7e7e5;--bd-3:#d9d9d6;--s-raised:#f8f8f7;--s-hover2:#ececea;--emphasis-bg:#0a0a0a;--hf-orange:#ff5a00;--hf-orange-dark:#c74600;--hf-orange-tint:#fff1e8;}
@media print{
.hf-op{--ink:#0a0a0a;--ink2:#5c5c5c;--bd-2:#e7e7e5;--s-raised:#f8f8f7;--emphasis-bg:#0a0a0a;}
}
.hf-op{-webkit-font-smoothing:antialiased;}
.hf-op a:hover{color:var(--hf-orange);}
.hf-op .hf-publisher{gap:10px;color:var(--ink);}
.hf-op .hf-publisher svg.hf-wordmark{width:auto;height:20px;margin:0;display:block;}
.hf-op .hf-publisher .aeo{font-size:11px;padding-left:10px;color:var(--ink2);}
.hf-op .preview-bar{margin:28px auto 20px;}
.hf-op .report{padding:30px 40px 18px;}
.hf-op .masthead{padding-bottom:12px;align-items:flex-end;}
.hf-op .publisher{display:flex;flex-direction:column;align-items:flex-end;}
.hf-op .publisher small{font-size:9px;margin-top:6px;}
.hf-op .brand span{font-size:9px;margin-top:4px;}
.hf-op .eyebrow{margin:16px 0 10px;font-size:9.5px;}
.hf-op h1{font-size:31px;line-height:1.1;}
.hf-op .dek{font-size:12px;line-height:1.55;margin-top:10px;}
.hf-op .scope{font-size:9.5px;padding:7px 0;margin:10px 0 12px;column-gap:16px;}
.hf-op .scope span{white-space:nowrap;}
.hf-op .metrics{gap:12px;}
.hf-op .metric{padding:13px 15px 12px;}
.hf-op .metric-label{font-size:9px;margin-bottom:8px;}
.hf-op .metric-value{font-size:30px;}
.hf-op .metric-detail{font-size:9.5px;line-height:1.45;margin-top:6px;}
.hf-op .recognition{font-size:10.5px;margin-top:12px;}
.hf-op section{margin-top:16px;}
.hf-op .section-heading{margin-bottom:8px;}
.hf-op .section-number{color:var(--hf-orange);font-weight:600;margin-right:9px;}
.hf-op .section-note{font-size:9.5px;}
.hf-op td{font-size:10.5px;padding-top:5px;padding-bottom:5px;}
.hf-op .segment-note,.hf-op td small{font-size:9px;}
.hf-op .bar-line{gap:10px;}
.hf-op .bar-line .fill{background:var(--hf-orange);}
.hf-op .bar-value{font-size:10.5px;min-width:88px;}
.hf-op .table-foot{font-size:9px;margin-top:8px;}
.hf-op .evidence{padding:14px 18px;gap:22px;}
.hf-op .evidence-label{font-size:8.5px;margin-bottom:6px;}
.hf-op .outcome{font-size:10px;line-height:1.55;}
.hf-op .engine-row{font-size:9px;}
.hf-op .next-step{margin-top:16px;padding:14px 18px;gap:22px;}
.hf-op .next-step .label{font-size:8.5px;}
.hf-op .next-step p{font-size:9px;line-height:1.5;}
.hf-op .invitation{padding-left:20px;}
.hf-op .invitation strong{font-size:11.5px;color:#ff8a3d;}
.hf-op .method{font-size:8.5px;line-height:1.4;margin-top:10px;}
.hf-op footer{font-size:8.5px;margin-top:9px;padding-top:9px;}
@media print{
.hf-op .report{padding:30px 40px 18px;}
}
@media screen and (max-width:590px){
.hf-op .report{padding:26px 20px;}
.hf-op h1{font-size:29px;}
.hf-op .hf-publisher svg.hf-wordmark{height:16px;}
.hf-op .publisher{align-items:flex-start;}
}

/* library preview fixes */
.hf-lf,.hf-op{background:transparent!important;}
.hf-lf .reviewbar{position:static;}

.hf-lf #outcome-legend .keyline > span:first-child{display:inline-flex;align-items:center;gap:10px;}
.hf-lf #outcome-legend .keyline > span:first-child::before{content:"";width:10px;height:10px;border-radius:3px;flex:none;background:var(--ink);}
.hf-lf #outcome-legend .keyline:nth-child(2) > span:first-child::before{background:var(--blue);}
.hf-lf #outcome-legend .keyline:nth-child(3) > span:first-child::before{background:var(--ink3);}
.hf-lf #outcome-legend .keyline:nth-child(4) > span:first-child::before{background:var(--s-hover2);box-shadow:inset 0 0 0 1px var(--bd-3);}
```
