# Slide Templates (Autonomee Style)

Reference for all available slide types. Editorial, minimal, serif headlines.

---

## 1. Title / Cover Slide

```html
<section>
  <div class="slide slide--section slide--center">
    <div class="content flex-center" style="flex-direction: column; text-align: center;">
      <p class="kicker" style="justify-content: center;">Kicker Text</p>
      <h1>Main Headline<br><span class="accent-text">Accent Words</span></h1>
      <p class="lead" style="max-width: 600px; margin: 0 auto;">
        A compelling subtitle that explains the value proposition in one or two sentences.
      </p>
      <div style="margin-top: 40px; display: flex; gap: 16px;">
        <a href="#" class="btn">Get Started</a>
        <a href="#" class="btn btn--accent">Learn More</a>
      </div>
    </div>
  </div>
</section>
```

---

## 2. Section Divider

```html
<section>
  <div class="slide slide--section slide--center">
    <p class="kicker" style="justify-content: center;">01 // Section Label</p>
    <h2>Section Title</h2>
    <p class="lead muted">Optional description for this section</p>
  </div>
</section>
```

---

## 3. Split Layout (Text + Image)

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="layers"></i>
        Brand Name
      </div>
    </div>
    <div class="split">
      <div>
        <p class="kicker">02 // Topic</p>
        <h2>Headline for<br>This Slide</h2>
        <p class="lead">Supporting text that explains the main point of this slide in detail.</p>
        <a href="#" class="btn" style="margin-top: 24px;">Learn More</a>
      </div>
      <div class="image-container">
        <img src="https://placehold.co/600x400/0a0a0a/7b8fa8?text=Image" alt="Description">
      </div>
    </div>
  </div>
</section>
```

---

## 4. Feature Cards (2x2 Grid)

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="layers"></i>
        Brand Name
      </div>
    </div>
    <div class="content">
      <p class="kicker">03 // Features</p>
      <h2>What We Offer</h2>
      <div class="grid-2" style="margin-top: 32px;">
        <div class="card fragment fade-up">
          <div class="card__icon"><i data-lucide="zap"></i></div>
          <h4 class="card__title">Feature One</h4>
          <p class="card__text">Brief description of this feature and its benefits.</p>
        </div>
        <div class="card fragment fade-up">
          <div class="card__icon"><i data-lucide="shield"></i></div>
          <h4 class="card__title">Feature Two</h4>
          <p class="card__text">Brief description of this feature and its benefits.</p>
        </div>
        <div class="card fragment fade-up">
          <div class="card__icon"><i data-lucide="trending-up"></i></div>
          <h4 class="card__title">Feature Three</h4>
          <p class="card__text">Brief description of this feature and its benefits.</p>
        </div>
        <div class="card fragment fade-up">
          <div class="card__icon"><i data-lucide="users"></i></div>
          <h4 class="card__title">Feature Four</h4>
          <p class="card__text">Brief description of this feature and its benefits.</p>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

## 5. Metrics / Stats Row

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="layers"></i>
        Brand Name
      </div>
    </div>
    <div class="content">
      <p class="kicker">04 // Traction</p>
      <h2>Growth Metrics</h2>
      <div class="metrics" style="margin-top: 48px;">
        <div class="metric fragment">
          <div class="metric__value">250K+</div>
          <div class="metric__label">Active Users</div>
        </div>
        <div class="metric fragment">
          <div class="metric__value">$3.2M</div>
          <div class="metric__label">Revenue</div>
        </div>
        <div class="metric fragment">
          <div class="metric__value">92%</div>
          <div class="metric__label">Retention</div>
        </div>
        <div class="metric fragment">
          <div class="metric__value">4.9</div>
          <div class="metric__label">Rating</div>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

## 6. Comparison (3 Columns)

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="layers"></i>
        Brand Name
      </div>
    </div>
    <div class="content">
      <h2>Three Approaches</h2>
      <div class="grid-3" style="margin-top: 32px;">
        <div class="card">
          <h4 class="card__title">Option A</h4>
          <p class="muted" style="margin-bottom: 16px;">Basic approach</p>
          <ul class="list">
            <li>Feature one</li>
            <li>Feature two</li>
            <li>Feature three</li>
          </ul>
        </div>
        <div class="card card--featured">
          <span class="badge" style="margin-bottom: 12px;">Recommended</span>
          <h4 class="card__title">Option B</h4>
          <p class="muted" style="margin-bottom: 16px;">Best choice</p>
          <ul class="list">
            <li>Feature one</li>
            <li>Feature two</li>
            <li>Feature three</li>
          </ul>
        </div>
        <div class="card">
          <h4 class="card__title">Option C</h4>
          <p class="muted" style="margin-bottom: 16px;">Advanced</p>
          <ul class="list">
            <li>Feature one</li>
            <li>Feature two</li>
            <li>Feature three</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

## 7. Numbered List (The Challenge / Problem)

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="layers"></i>
        Brand Name
      </div>
    </div>
    <div class="split">
      <div>
        <p class="kicker">05 // The Problem</p>
        <h2>The Challenge</h2>
        <p class="lead">Understanding the pain points we solve.</p>
      </div>
      <div>
        <ul class="list list--numbered">
          <li class="fragment">
            <strong>Pain Point One</strong><br>
            <span class="muted">Description of this challenge and its impact.</span>
          </li>
          <li class="fragment">
            <strong>Pain Point Two</strong><br>
            <span class="muted">Description of this challenge and its impact.</span>
          </li>
          <li class="fragment">
            <strong>Pain Point Three</strong><br>
            <span class="muted">Description of this challenge and its impact.</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</section>
```

---

## 8. Timeline / Roadmap

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="layers"></i>
        Brand Name
      </div>
    </div>
    <div class="content">
      <h2>Our Roadmap</h2>
      <div class="timeline" style="margin-top: 48px;">
        <div class="timeline__item fragment">
          <div class="timeline__year">2023</div>
          <div class="timeline__dot"></div>
          <div class="timeline__content">Product Launch & Initial Traction</div>
        </div>
        <div class="timeline__item fragment">
          <div class="timeline__year">2024</div>
          <div class="timeline__dot"></div>
          <div class="timeline__content">Scale Operations & Series A</div>
        </div>
        <div class="timeline__item fragment">
          <div class="timeline__year">2025</div>
          <div class="timeline__dot"></div>
          <div class="timeline__content">International Expansion</div>
        </div>
        <div class="timeline__item fragment">
          <div class="timeline__year">2026</div>
          <div class="timeline__dot"></div>
          <div class="timeline__content">Market Leadership</div>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

## 9. Pricing Table

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="layers"></i>
        Brand Name
      </div>
    </div>
    <div class="content">
      <h2 style="text-align: center;">Subscription Packages</h2>
      <div class="pricing" style="margin-top: 32px;">
        <div class="pricing__card fragment">
          <div class="pricing__name">Starter</div>
          <div class="pricing__price">$29</div>
          <div class="pricing__period">per month</div>
          <ul class="pricing__features">
            <li>Up to 5 users</li>
            <li>Basic features</li>
            <li>Email support</li>
          </ul>
          <a href="#" class="btn" style="width: 100%;">Choose Plan</a>
        </div>
        <div class="pricing__card pricing__card--featured fragment">
          <span class="badge" style="margin-bottom: 12px;">Most Popular</span>
          <div class="pricing__name">Growth</div>
          <div class="pricing__price">$79</div>
          <div class="pricing__period">per month</div>
          <ul class="pricing__features">
            <li>Up to 25 users</li>
            <li>Advanced features</li>
            <li>Priority support</li>
          </ul>
          <a href="#" class="btn btn--accent" style="width: 100%;">Choose Plan</a>
        </div>
        <div class="pricing__card fragment">
          <div class="pricing__name">Enterprise</div>
          <div class="pricing__price">$199</div>
          <div class="pricing__period">per month</div>
          <ul class="pricing__features">
            <li>Unlimited users</li>
            <li>All features</li>
            <li>Dedicated support</li>
          </ul>
          <a href="#" class="btn" style="width: 100%;">Choose Plan</a>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

## 10. Testimonials

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="layers"></i>
        Brand Name
      </div>
    </div>
    <div class="split">
      <div>
        <p class="kicker">06 // Testimonials</p>
        <h2>From Idea<br>to Success</h2>
        <p class="lead">See how our customers transformed their businesses.</p>
      </div>
      <div>
        <div class="testimonial" style="margin-bottom: 16px;">
          <div class="testimonial__avatar">
            <img src="https://placehold.co/60x60/7b8fa8/f5f4f0?text=JD" alt="Avatar">
          </div>
          <div class="testimonial__content">
            <p class="testimonial__text">"This product completely changed how we operate. Highly recommended."</p>
            <div class="testimonial__author">Jane Doe</div>
            <div class="testimonial__role">CEO, TechCorp</div>
          </div>
        </div>
        <div class="testimonial">
          <div class="testimonial__avatar">
            <img src="https://placehold.co/60x60/9bb0c9/0a0a0a?text=JS" alt="Avatar">
          </div>
          <div class="testimonial__content">
            <p class="testimonial__text">"The ROI we've seen has been incredible. A game-changer for our team."</p>
            <div class="testimonial__author">John Smith</div>
            <div class="testimonial__role">CTO, StartupXYZ</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

## 11. Checklist / Recognition

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="layers"></i>
        Brand Name
      </div>
    </div>
    <div class="split">
      <div>
        <ul class="list list--check">
          <li class="fragment"><strong>Best Startup 2025</strong> - Tech Awards</li>
          <li class="fragment"><strong>Innovation Excellence</strong> - Industry Summit</li>
          <li class="fragment"><strong>Top 10 to Watch</strong> - Forbes</li>
          <li class="fragment"><strong>Sustainability Award</strong> - Green Tech</li>
        </ul>
      </div>
      <div>
        <p class="kicker">07 // Recognition</p>
        <h2>Press &<br>Recognition</h2>
        <p class="lead">Awards and accolades from industry leaders.</p>
      </div>
    </div>
  </div>
</section>
```

---

## 12. CTA / Closing Slide

```html
<section>
  <div class="slide slide--section slide--center">
    <div class="content flex-center" style="flex-direction: column;">
      <h1>Let's Build the<br><span class="accent-text">Future Together</span></h1>
      <p class="lead" style="margin-bottom: 40px;">Ready to transform your workflow?</p>
      <div class="contact-grid" style="width: 100%; max-width: 600px;">
        <div class="contact-item">
          <div class="contact-item__label">Email</div>
          <div class="contact-item__value">hello@company.com</div>
        </div>
        <div class="contact-item">
          <div class="contact-item__label">Website</div>
          <div class="contact-item__value">company.com</div>
        </div>
        <div class="contact-item">
          <div class="contact-item__label">LinkedIn</div>
          <div class="contact-item__value">@company</div>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

## 13. Code / Command Slide

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="terminal"></i>
        Technical Guide
      </div>
    </div>
    <div class="split--60-40">
      <div>
        <p class="kicker">08 // Commands</p>
        <h2>Getting Started</h2>
        <div style="margin-top: 24px;">
          <div class="command fragment">
            <span class="command__prompt">$</span>
            <span class="command__text">npm install package</span>
            <span class="command__desc">Install dependencies</span>
          </div>
          <div class="command fragment">
            <span class="command__prompt">$</span>
            <span class="command__text">npm run dev</span>
            <span class="command__desc">Start development</span>
          </div>
          <div class="command fragment">
            <span class="command__prompt">$</span>
            <span class="command__text">npm run build</span>
            <span class="command__desc">Build for production</span>
          </div>
        </div>
      </div>
      <div>
        <pre><code>// Example code
const config = {
  theme: 'autonomee',
  dark: true,
  accent: '#7b8fa8'
};</code></pre>
      </div>
    </div>
  </div>
</section>
```

---

## 14. Workflow Diagram

```html
<section>
  <div class="slide">
    <div class="header">
      <div class="header__logo">
        <i data-lucide="git-branch"></i>
        Process
      </div>
    </div>
    <div class="content">
      <p class="kicker">09 // Workflow</p>
      <h2>How It Works</h2>
      <div class="workflow" style="margin-top: 48px;">
        <div class="workflow__step fragment">
          <div class="workflow__box">
            <div class="workflow__label">Step 1</div>
            <div class="workflow__sublabel">Input</div>
          </div>
        </div>
        <div class="workflow__arrow">→</div>
        <div class="workflow__step fragment">
          <div class="workflow__box">
            <div class="workflow__label">Step 2</div>
            <div class="workflow__sublabel">Process</div>
          </div>
        </div>
        <div class="workflow__arrow">→</div>
        <div class="workflow__step fragment">
          <div class="workflow__box">
            <div class="workflow__label">Step 3</div>
            <div class="workflow__sublabel">Output</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

## Icon Reference (Lucide)

Common icons to use with `<i data-lucide="icon-name"></i>`:

| Category | Icons |
|----------|-------|
| **Actions** | `zap`, `rocket`, `target`, `check`, `plus`, `arrow-right` |
| **Tech** | `cpu`, `database`, `cloud`, `code`, `terminal`, `globe` |
| **Business** | `briefcase`, `trending-up`, `bar-chart`, `pie-chart`, `dollar-sign` |
| **People** | `users`, `user`, `user-check`, `user-plus` |
| **Security** | `shield`, `lock`, `key`, `eye`, `eye-off` |
| **Communication** | `mail`, `message-circle`, `phone`, `video` |
| **Files** | `file`, `folder`, `image`, `download`, `upload` |
| **Brand** | `layers`, `hexagon`, `box`, `grid` |

Full list: https://lucide.dev/icons
