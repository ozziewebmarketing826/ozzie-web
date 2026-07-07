# ozzie-web
Ozzie web &amp; marketing
import { useState } from "react";

const SECTIONS = [
  { id: "offer", label: "💰 The Offer" },
  { id: "pricing", label: "🏷️ Pricing" },
  { id: "website", label: "🌐 Your Sales Page" },
  { id: "scripts", label: "📞 Sales Scripts" },
  { id: "dms", label: "📲 DM Templates" },
  { id: "followup", label: "🔁 Follow-Ups" },
  { id: "delivery", label: "✅ Delivery Checklist" },
  { id: "ai", label: "🤖 AI Sales Assistant" },
];

const offerData = {
  headline: "\"Your Business Online in 48 Hours\" — The One-Page Website Package",
  tagline: "Sell fast. Deliver fast. Get paid.",
  targets: [
    "Mobile Notaries", "General Contractors", "Mobile Detailers",
    "Handymen", "House Cleaners", "Landscapers",
    "Lash Techs / Hair Stylists", "Personal Trainers", "Food Trucks", "Tutors"
  ],
  painPoints: [
    "They have no website, or a bad one built in 2015",
    "They're losing customers to competitors who look more professional",
    "They don't know how to build one or can't afford a big agency",
    "They need something fast — not a 6-week project"
  ],
  promise: "A clean, mobile-ready, professional one-page website — live in 48 hours — for a flat, affordable rate.",
  deliverables: [
    { item: "1-Page Professional Website", detail: "Mobile-first HTML, fully responsive, ready to deploy", value: "$300" },
    { item: "Google Business Profile Setup Guide", detail: "Step-by-step PDF so they show up on Google Maps", value: "$75" },
    { item: "3 Social Media Bio Rewrites", detail: "Instagram, Facebook, TikTok — optimized to convert", value: "$75" },
    { item: "Custom Promo Flyer (Canva)", detail: "Shareable digital flyer for their services", value: "$50" },
    { item: "1 Month Email Support", detail: "Minor edits, questions answered within 24 hrs", value: "$50" },
  ]
};

const pricingData = [
  {
    tier: "Starter",
    price: "$297",
    badge: "Best for first clients",
    color: "#2563eb",
    includes: [
      "1-Page Website (5 sections)",
      "Google Business Setup Guide",
      "1 Social Bio Rewrite",
      "48-Hour Delivery",
      "1 Round of Revisions"
    ],
    pitch: "Perfect intro offer. Gets you paid and gets them live."
  },
  {
    tier: "Pro",
    price: "$497",
    badge: "Most Popular",
    color: "#7c3aed",
    includes: [
      "1-Page Website (7 sections)",
      "Google Business Setup Guide",
      "3 Social Bio Rewrites",
      "Custom Promo Flyer",
      "48-Hour Delivery",
      "2 Rounds of Revisions",
      "1 Month Email Support"
    ],
    pitch: "Your main offer. Full value, great margin."
  },
  {
    tier: "Premium",
    price: "$797",
    badge: "Highest Value",
    color: "#059669",
    includes: [
      "Everything in Pro",
      "Monthly Social Content (4 posts)",
      "Basic SEO Setup",
      "Review Generation Script",
      "Priority 24-Hour Delivery",
      "3 Months Email Support"
    ],
    pitch: "Recurring income. Turn one client into monthly revenue."
  }
];

const websiteCopy = {
  hero: {
    headline: "Your Business Deserves a Real Website.",
    sub: "Get a professional, mobile-ready website live in 48 hours — flat rate, no surprises.",
    cta: "Claim Your Spot →"
  },
  pain: {
    heading: "Still sending customers to your Facebook page?",
    points: [
      "You're losing jobs to competitors who look more professional online",
      "Customers Google you and find nothing — so they call someone else",
      "You've been meaning to get a website for months (or years)",
      "You don't have time to learn website builders or pay agency prices"
    ]
  },
  solution: {
    heading: "I build it for you. You're live in 48 hours.",
    body: "I'm a local LA-based web designer specializing in one-page websites for service businesses. Clean, fast, professional — and affordable. You focus on your work. I handle everything else."
  },
  includes: [
    "✅ Professional 1-page website, mobile-friendly",
    "✅ Your services, photos, contact info, and booking link",
    "✅ Google Business Profile setup guide",
    "✅ Social media bios rewritten to attract customers",
    "✅ Custom promo flyer to share online",
    "✅ 48-hour turnaround — guaranteed"
  ],
  pricing: "Starting at $297. Flat rate. No monthly fees. No surprises.",
  cta: {
    heading: "Ready to get online?",
    sub: "I'm only taking 5 clients this week. Text or DM me to grab your spot.",
    button: "Text Me Now"
  },
  proof: "I built the Give Us a Sign Notary website — a local LA business now showing up on Google and booking clients online. Yours can be next."
};

const salesScripts = [
  {
    title: "Cold Phone / Intro Call Script",
    scenario: "You call or get on a call with a local business owner",
    script: `"Hey [Name], my name is Ozzie — I'm a local web designer based in the Commerce/LA area. I specialize in building professional one-page websites for service businesses like yours. I can have you live online in 48 hours for a flat rate.

Quick question — do you currently have a website, or are customers just finding you on Facebook or Yelp?

[If no website:]
Perfect. That's exactly who I help. A lot of my clients were in the same spot — good business, no online presence. I built them a clean professional site and they started getting calls from Google within weeks.

My intro package is $297 — one-time, no monthly fees, you own it. I do all the work. You just send me your info and I handle the rest.

Can I send you a couple examples of sites I've built so you can see what it looks like?"`,
    tips: ["Don't pitch the price until they express interest", "Ask questions first — listen for the pain", "Always offer to show examples — have 1-2 ready"]
  },
  {
    title: "Objection: 'I don't need a website'",
    scenario: "Prospect pushes back",
    script: `"I totally get that — a lot of my clients said the same thing before. Here's the thing: your customers ARE looking you up online, even if they heard about you from a friend. If they Google your name and nothing comes up, or they see a messy Facebook page, some of them move on.

A simple one-page site with your services, your photo, and a contact button just makes you look legit. It builds trust before they even call you.

And at $297 one-time — if it gets you even one extra job, it's already paid for itself. Want me to show you what it would look like for your business specifically?"`,
    tips: ["Reframe 'need' to 'trust'", "Use the ROI of one extra client", "Offer a custom mockup concept to close"]
  },
  {
    title: "Objection: 'That's too expensive'",
    scenario: "Price resistance",
    script: `"I hear you — money is real. Can I ask what you were expecting to invest?

[Listen to their number]

Here's where I'm coming from: most web designers charge $1,000–$3,000 for this type of work, and it takes weeks. I've streamlined my process so I can do it faster and pass those savings on to early clients.

At $297, that's less than one job for most service businesses. And you keep the site forever — no monthly fees.

If budget is tight right now, I do have a $197 bare-bones version — just the website, no extras. Would that work better for you?"`,
    tips: ["Always have a lower-tier option ready", "Anchor against the $1,000+ industry price", "Never argue — redirect to value"]
  }
];

const dmTemplates = [
  {
    platform: "Instagram DM — Cold Outreach",
    target: "Local business with no website in bio",
    message: `Hey [Name]! 👋 I came across your page and love what you're doing with [their service/business].

I help local service businesses get a professional website live in 48 hours — flat rate, no monthly fees. Something that makes customers trust you before they even call.

I'm running an intro special right now and only have a few spots open this week. Would you be open to seeing what it would look like for your business? 🙌`,
    note: "Like 2-3 of their posts first. Wait 10 min. Then DM. Response rate goes up significantly."
  },
  {
    platform: "Facebook DM — Warm (Someone You Know)",
    target: "Acquaintance, neighbor, old contact who runs a business",
    message: `Hey [Name]! It's Ozzie 👋 Hope you're doing great!

I'm doing something new — helping local business owners get a professional website up fast. 48-hour turnaround, flat rate of $297, no monthly fees. You own it.

Figured you might know someone who could use it — or maybe even yourself? I'm only taking a few clients this week at the intro price.

Lmk if you want me to send you the details! 🙏`,
    note: "Warm messages convert 3x better. Start here before cold outreach."
  },
  {
    platform: "Facebook Group Post",
    target: "Local business groups, community boards, city groups",
    message: `📢 Does your business have a professional website?

I'm a local LA-based web designer helping service businesses get online FAST.

✅ 1-page professional website
✅ Mobile-friendly & ready to share
✅ 48-hour turnaround
✅ Flat rate starting at $297 (no monthly fees)

Perfect for: notaries, contractors, detailers, cleaners, stylists, handymen, trainers, and more.

Drop a 💻 below or DM me — only 5 intro spots this week.`,
    note: "Post in 5-10 groups daily. Don't spam — add value in the group first when possible."
  },
  {
    platform: "Nextdoor / Community Board",
    target: "Local neighborhood platforms",
    message: `Local Web Design — 48-Hour Turnaround, Starting at $297

Hi neighbors! I'm Ozzie, based in Commerce/LA, and I help local service businesses get a professional website live fast.

One-time flat rate. No monthly fees. You own your site forever.

If you or someone you know runs a service business without a website (or with a bad one), I'd love to help.

Text me at [YOUR NUMBER] or visit [YOUR LINK] to see examples and grab a spot. Limited availability this week.`,
    note: "Nextdoor works extremely well for local service businesses. High trust environment."
  }
];

const followUps = [
  {
    day: "Day 1 — 24 Hours After First Message",
    trigger: "No response",
    message: `Hey [Name] — just following up on my message from yesterday! I know things get busy.

I only have 2 spots left at the $297 intro price this week. Wanted to make sure you had a chance to grab one before I open them up.

Totally fine if it's not the right time — just wanted to check in! 🙏`,
    tip: "Keep it short. No pressure. Just a nudge."
  },
  {
    day: "Day 3 — Value Drop Follow-Up",
    trigger: "Still no response",
    message: `Hey [Name]! Ozzie here — not trying to bug you, just wanted to share something quick.

I just finished a site for a [notary/contractor/detailer — use their industry] in the area and it looked really sharp. Made me think of you.

Here's what I built: [share screenshot or link]

Still have one intro spot open at $297 if you want in. Just reply here or text me. No hard feelings either way! 😊`,
    tip: "Show, don't tell. Attach a screenshot of a recent site you built."
  },
  {
    day: "Day 7 — Final Follow-Up / Breakup Message",
    trigger: "No response after 3 touches",
    message: `Hey [Name] — I won't keep bugging you after this, I promise 😄

I'm closing out my intro pricing at $297 this week and moving to my regular rate of $497. Wanted to give you a last shot before that happens.

If the timing's ever right down the road, I'm always around. Wishing you the best with [their business]! 🙌`,
    tip: "Breakup messages often get the highest reply rate. Creates urgency + removes pressure."
  },
  {
    day: "Day 30 — Long-Term Nurture",
    trigger: "They said 'maybe later'",
    message: `Hey [Name]! It's been a few weeks — just checking in on you and [their business name].

I had a client similar to you just launch their new site and they're already getting inquiries from Google. Made me think of you!

My schedule opened back up if you're still interested. Same deal I offered before. Just reply here if you want to get started 🚀`,
    tip: "Don't give up on maybes. 30-day follow-up converts surprisingly often."
  }
];

const deliveryChecklist = [
  {
    phase: "Phase 1 — Intake (Day 0, After Payment)",
    color: "#2563eb",
    steps: [
      { task: "Send intake form / collect info", detail: "Business name, tagline, services, phone, email, address, booking link, photos" },
      { task: "Collect payment", detail: "Zelle, Venmo, or PayPal (Zelle = no fees)" },
      { task: "Confirm 48-hour delivery window", detail: "Send confirmation text: 'Got your payment! I'll have your site ready by [DATE/TIME].'" },
      { task: "Review their existing social profiles", detail: "Screenshot their current Instagram/Facebook for reference" },
    ]
  },
  {
    phase: "Phase 2 — Build (Day 1)",
    color: "#7c3aed",
    steps: [
      { task: "Open Claude and prompt the website build", detail: "Use Claude to generate the full HTML single-page site with their info" },
      { task: "Customize hero section", detail: "Name, tagline, CTA button, services list" },
      { task: "Add services grid", detail: "List each service with brief description" },
      { task: "Build contact/booking section", detail: "Phone, email, address, booking link" },
      { task: "Add Google Maps embed", detail: "Optional but adds trust and local SEO" },
      { task: "Test mobile responsiveness", detail: "Check on phone — 70%+ of traffic is mobile" },
      { task: "Screenshot for preview", detail: "Take 3-4 screenshots to send client for approval" },
    ]
  },
  {
    phase: "Phase 3 — Deliver (Day 2)",
    color: "#059669",
    steps: [
      { task: "Send preview screenshots for approval", detail: "Text or DM: 'Here's your preview! Let me know if you want any changes.'" },
      { task: "Deploy to GitHub Pages (free)", detail: "Upload HTML file to GitHub repo, enable Pages" },
      { task: "Send live URL to client", detail: "'Your site is LIVE! Here's your link: [URL]'" },
      { task: "Deliver Google Business PDF guide", detail: "Send the setup guide so they can add their listing" },
      { task: "Send rewritten social bios", detail: "Deliver IG, FB, TikTok bio rewrites as a text doc" },
      { task: "Deliver promo flyer (if Pro tier)", detail: "Export from Canva as PNG/PDF and send" },
    ]
  },
  {
    phase: "Phase 4 — Retention (Day 3+)",
    color: "#d97706",
    steps: [
      { task: "Request a review", detail: "'If you loved the work, would you drop me a quick Google review? Here's the link: [URL]'" },
      { task: "Ask for referrals", detail: "'If you know anyone else who needs a site, I'd love the intro — I'll give them $50 off!'" },
      { task: "Offer monthly social content upsell", detail: "'I also do 4 social posts/month for $97/mo — want me to keep your pages active?'" },
      { task: "Add to your portfolio", detail: "Screenshot the site, add to your portfolio page and social media" },
      { task: "Follow up in 30 days", detail: "'Hey! How's the site working for you? Getting any new customers from it?'" },
    ]
  }
];

// ─── AI ASSISTANT ────────────────────────────────────────────────
async function askAgent(prompt, context) {
  const systemPrompt = `You are Ozzie's AI Sales Agent for his one-page website business. 
Your job is to help him sell, script, and close deals with local service businesses.

CONTEXT ABOUT THE BUSINESS:
- Service: One-page websites built in 48 hours
- Price: $297 (Starter), $497 (Pro), $797 (Premium)
- Target: Local service businesses in LA/Commerce area — notaries, contractors, detailers, cleaners, stylists, etc.
- Ozzie's background: Construction coordination, e-commerce (Luxury Beauty Empire LLC), notary business (Give Us a Sign), web design
- Tone: Friendly, direct, professional, no fluff

When generating scripts, DMs, or copy — make it conversational, not salesy. Real talk, not corporate speak.
When giving strategy — be tactical and specific. No vague advice.
Format your response cleanly. Use bullet points where helpful. Keep it actionable.`;

  const response = await fetch("https://api.anthropic.com/v1/messages", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({
      model: "claude-sonnet-4-6",
      max_tokens: 1000,
      system: systemPrompt,
      messages: [{ role: "user", content: prompt }]
    })
  });
  const data = await response.json();
  return data.content?.[0]?.text || "No response received.";
}

// ─── COMPONENTS ──────────────────────────────────────────────────

function CopyButton({ text }) {
  const [copied, setCopied] = useState(false);
  const copy = () => {
    navigator.clipboard.writeText(text);
    setCopied(true);
    setTimeout(() => setCopied(false), 2000);
  };
  return (
    <button onClick={copy} style={{
      background: copied ? "#059669" : "#1e293b",
      color: "#fff", border: "none", borderRadius: 6,
      padding: "5px 12px", fontSize: 12, cursor: "pointer",
      fontFamily: "inherit", transition: "background 0.2s"
    }}>
      {copied ? "✓ Copied!" : "Copy"}
    </button>
  );
}

function Badge({ text, color }) {
  return (
    <span style={{
      background: color + "22", color, border: `1px solid ${color}44`,
      borderRadius: 20, padding: "2px 10px", fontSize: 11, fontWeight: 700,
      letterSpacing: 0.5, textTransform: "uppercase"
    }}>{text}</span>
  );
}

function Section({ title, children }) {
  return (
    <div style={{ marginBottom: 32 }}>
      <h2 style={{ fontSize: 20, fontWeight: 800, color: "#0f172a", marginBottom: 16, borderBottom: "2px solid #e2e8f0", paddingBottom: 8 }}>{title}</h2>
      {children}
    </div>
  );
}

function Card({ children, style = {} }) {
  return (
    <div style={{
      background: "#fff", border: "1px solid #e2e8f0", borderRadius: 12,
      padding: 20, marginBottom: 16, ...style
    }}>{children}</div>
  );
}

// ─── TAB PANELS ──────────────────────────────────────────────────

function OfferPanel() {
  return (
    <div>
      <Card style={{ background: "linear-gradient(135deg, #0f172a 0%, #1e3a5f 100%)", color: "#fff", border: "none" }}>
        <div style={{ fontSize: 22, fontWeight: 900, marginBottom: 6 }}>{offerData.headline}</div>
        <div style={{ color: "#94a3b8", fontSize: 14 }}>{offerData.tagline}</div>
      </Card>

      <Section title="🎯 Best Prospect Types">
        <div style={{ display: "flex", flexWrap: "wrap", gap: 8 }}>
          {offerData.targets.map(t => (
            <span key={t} style={{ background: "#eff6ff", color: "#2563eb", border: "1px solid #bfdbfe", borderRadius: 20, padding: "4px 14px", fontSize: 13, fontWeight: 600 }}>{t}</span>
          ))}
        </div>
      </Section>

      <Section title="😤 Their Pain Points">
        {offerData.painPoints.map((p, i) => (
          <div key={i} style={{ display: "flex", gap: 10, marginBottom: 10, alignItems: "flex-start" }}>
            <span style={{ color: "#ef4444", fontWeight: 800, marginTop: 1 }}>✗</span>
            <span style={{ color: "#374151", fontSize: 14 }}>{p}</span>
          </div>
        ))}
      </Section>

      <Section title="✅ What You Deliver">
        <Card style={{ background: "#f0fdf4", border: "1px solid #bbf7d0" }}>
          <div style={{ fontWeight: 700, color: "#059669", marginBottom: 12, fontSize: 15 }}>Your Core Promise:</div>
          <div style={{ color: "#166534", fontSize: 14, lineHeight: 1.6 }}>{offerData.promise}</div>
        </Card>
        {offerData.deliverables.map((d, i) => (
          <div key={i} style={{ display: "flex", justifyContent: "space-between", alignItems: "center", padding: "10px 0", borderBottom: i < offerData.deliverables.length - 1 ? "1px solid #f1f5f9" : "none" }}>
            <div>
              <div style={{ fontWeight: 700, color: "#0f172a", fontSize: 14 }}>{d.item}</div>
              <div style={{ color: "#64748b", fontSize: 12 }}>{d.detail}</div>
            </div>
            <span style={{ color: "#059669", fontWeight: 800, fontSize: 14, whiteSpace: "nowrap", marginLeft: 12 }}>{d.value}</span>
          </div>
        ))}
        <div style={{ display: "flex", justifyContent: "space-between", marginTop: 12, paddingTop: 12, borderTop: "2px solid #e2e8f0" }}>
          <span style={{ fontWeight: 800, color: "#0f172a" }}>Total Value</span>
          <span style={{ fontWeight: 900, color: "#7c3aed", fontSize: 18 }}>$550</span>
        </div>
        <div style={{ display: "flex", justifyContent: "space-between", marginTop: 6 }}>
          <span style={{ fontWeight: 800, color: "#0f172a" }}>Your Price (Pro)</span>
          <span style={{ fontWeight: 900, color: "#2563eb", fontSize: 18 }}>$497</span>
        </div>
      </Section>
    </div>
  );
}

function PricingPanel() {
  return (
    <div>
      <div style={{ color: "#64748b", fontSize: 14, marginBottom: 20 }}>
        Three tiers gives you flexibility to close any client — budget-conscious to premium.
      </div>
      {pricingData.map((tier, i) => (
        <Card key={i} style={{ border: `2px solid ${tier.color}33`, position: "relative", overflow: "hidden" }}>
          <div style={{ position: "absolute", top: 0, left: 0, right: 0, height: 4, background: tier.color }} />
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 12 }}>
            <div>
              <div style={{ fontWeight: 900, fontSize: 20, color: "#0f172a" }}>{tier.tier}</div>
              <Badge text={tier.badge} color={tier.color} />
            </div>
            <div style={{ fontSize: 32, fontWeight: 900, color: tier.color }}>{tier.price}</div>
          </div>
          <div style={{ color: "#475569", fontSize: 13, marginBottom: 12, fontStyle: "italic" }}>{tier.pitch}</div>
          {tier.includes.map((item, j) => (
            <div key={j} style={{ fontSize: 13, color: "#374151", padding: "3px 0", display: "flex", gap: 8 }}>
              <span style={{ color: tier.color }}>✓</span> {item}
            </div>
          ))}
        </Card>
      ))}
      <Card style={{ background: "#fefce8", border: "1px solid #fde68a" }}>
        <div style={{ fontWeight: 700, color: "#92400e", marginBottom: 8 }}>💡 Pricing Strategy</div>
        <div style={{ fontSize: 13, color: "#78350f", lineHeight: 1.6 }}>
          Lead with $297 to get your first 3 clients fast. Once you have 2 testimonials, move to $497 as your standard. 
          Use $797 for clients who ask about ongoing social media. Never discount below $247 — it signals low quality.
        </div>
      </Card>
    </div>
  );
}

function WebsitePanel() {
  const fullCopy = `HEADLINE: ${websiteCopy.hero.headline}
SUBHEADLINE: ${websiteCopy.hero.sub}
CTA: ${websiteCopy.hero.cta}

--- PAIN SECTION ---
${websiteCopy.pain.heading}
${websiteCopy.pain.points.map(p => "• " + p).join("\n")}

--- SOLUTION ---
${websiteCopy.solution.heading}
${websiteCopy.solution.body}

--- WHAT'S INCLUDED ---
${websiteCopy.includes.join("\n")}

--- PRICING ---
${websiteCopy.pricing}

--- SOCIAL PROOF ---
${websiteCopy.proof}

--- FINAL CTA ---
${websiteCopy.cta.heading}
${websiteCopy.cta.sub}`;

  return (
    <div>
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 16 }}>
        <div style={{ color: "#64748b", fontSize: 14 }}>Copy-and-paste ready for Carrd.co, Google Sites, or any page builder.</div>
        <CopyButton text={fullCopy} />
      </div>

      {[
        { label: "🦸 Hero Section", content: (
          <div>
            <div style={{ fontSize: 22, fontWeight: 900, color: "#0f172a", marginBottom: 6 }}>{websiteCopy.hero.headline}</div>
            <div style={{ color: "#64748b", marginBottom: 10 }}>{websiteCopy.hero.sub}</div>
            <span style={{ background: "#2563eb", color: "#fff", padding: "8px 20px", borderRadius: 8, fontWeight: 700, fontSize: 14 }}>{websiteCopy.hero.cta}</span>
          </div>
        )},
        { label: "😤 Pain Section", content: (
          <div>
            <div style={{ fontWeight: 700, color: "#dc2626", marginBottom: 10 }}>{websiteCopy.pain.heading}</div>
            {websiteCopy.pain.points.map((p, i) => <div key={i} style={{ color: "#374151", fontSize: 14, marginBottom: 6 }}>✗ {p}</div>)}
          </div>
        )},
        { label: "💡 Solution", content: (
          <div>
            <div style={{ fontWeight: 700, color: "#059669", marginBottom: 8 }}>{websiteCopy.solution.heading}</div>
            <div style={{ color: "#374151", fontSize: 14, lineHeight: 1.6 }}>{websiteCopy.solution.body}</div>
          </div>
        )},
        { label: "✅ Includes List", content: (
          <div>{websiteCopy.includes.map((item, i) => <div key={i} style={{ color: "#374151", fontSize: 14, marginBottom: 4 }}>{item}</div>)}</div>
        )},
        { label: "🏷️ Pricing Line", content: (
          <div style={{ fontWeight: 700, color: "#7c3aed", fontSize: 16 }}>{websiteCopy.pricing}</div>
        )},
        { label: "⭐ Social Proof", content: (
          <div style={{ color: "#374151", fontSize: 14, fontStyle: "italic", lineHeight: 1.6 }}>{websiteCopy.proof}</div>
        )},
        { label: "📣 Final CTA", content: (
          <div>
            <div style={{ fontWeight: 800, fontSize: 18, color: "#0f172a", marginBottom: 4 }}>{websiteCopy.cta.heading}</div>
            <div style={{ color: "#64748b", marginBottom: 10 }}>{websiteCopy.cta.sub}</div>
            <span style={{ background: "#059669", color: "#fff", padding: "8px 20px", borderRadius: 8, fontWeight: 700, fontSize: 14 }}>{websiteCopy.cta.button}</span>
          </div>
        )},
      ].map((block, i) => (
        <Card key={i}>
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 12 }}>
            <div style={{ fontWeight: 700, color: "#0f172a", fontSize: 13, textTransform: "uppercase", letterSpacing: 0.5 }}>{block.label}</div>
          </div>
          {block.content}
        </Card>
      ))}
    </div>
  );
}

function ScriptsPanel() {
  return (
    <div>
      {salesScripts.map((script, i) => (
        <Card key={i}>
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 8 }}>
            <div>
              <div style={{ fontWeight: 800, color: "#0f172a", fontSize: 15 }}>{script.title}</div>
              <div style={{ color: "#94a3b8", fontSize: 12, marginTop: 2 }}>Scenario: {script.scenario}</div>
            </div>
            <CopyButton text={script.script} />
          </div>
          <div style={{ background: "#f8fafc", borderRadius: 8, padding: 14, marginBottom: 12, border: "1px solid #e2e8f0" }}>
            <pre style={{ margin: 0, fontFamily: "inherit", fontSize: 13, color: "#374151", whiteSpace: "pre-wrap", lineHeight: 1.7 }}>{script.script}</pre>
          </div>
          <div style={{ display: "flex", flexWrap: "wrap", gap: 6 }}>
            {script.tips.map((tip, j) => (
              <span key={j} style={{ background: "#fef9c3", color: "#854d0e", fontSize: 11, padding: "3px 10px", borderRadius: 20, border: "1px solid #fde68a" }}>💡 {tip}</span>
            ))}
          </div>
        </Card>
      ))}
    </div>
  );
}

function DMPanel() {
  return (
    <div>
      {dmTemplates.map((dm, i) => (
        <Card key={i}>
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 6 }}>
            <div>
              <div style={{ fontWeight: 800, color: "#0f172a", fontSize: 15 }}>{dm.platform}</div>
              <div style={{ color: "#94a3b8", fontSize: 12 }}>Best for: {dm.target}</div>
            </div>
            <CopyButton text={dm.message} />
          </div>
          <div style={{ background: "#f0f9ff", border: "1px solid #bae6fd", borderRadius: 8, padding: 14, marginBottom: 10 }}>
            <pre style={{ margin: 0, fontFamily: "inherit", fontSize: 13, color: "#0c4a6e", whiteSpace: "pre-wrap", lineHeight: 1.7 }}>{dm.message}</pre>
          </div>
          <div style={{ background: "#fefce8", border: "1px solid #fde68a", borderRadius: 6, padding: "6px 12px", fontSize: 12, color: "#713f12" }}>
            📌 Pro tip: {dm.note}
          </div>
        </Card>
      ))}
    </div>
  );
}

function FollowUpPanel() {
  return (
    <div>
      {followUps.map((f, i) => (
        <Card key={i} style={{ borderLeft: "4px solid #7c3aed" }}>
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 6 }}>
            <div>
              <div style={{ fontWeight: 800, color: "#7c3aed", fontSize: 14 }}>{f.day}</div>
              <div style={{ color: "#94a3b8", fontSize: 12 }}>Trigger: {f.trigger}</div>
            </div>
            <CopyButton text={f.message} />
          </div>
          <div style={{ background: "#faf5ff", border: "1px solid #e9d5ff", borderRadius: 8, padding: 14, marginBottom: 10 }}>
            <pre style={{ margin: 0, fontFamily: "inherit", fontSize: 13, color: "#3b0764", whiteSpace: "pre-wrap", lineHeight: 1.7 }}>{f.message}</pre>
          </div>
          <div style={{ fontSize: 12, color: "#7c3aed", fontStyle: "italic" }}>💡 {f.tip}</div>
        </Card>
      ))}
    </div>
  );
}

function DeliveryPanel() {
  const [checked, setChecked] = useState({});
  const toggle = (key) => setChecked(prev => ({ ...prev, [key]: !prev[key] }));

  return (
    <div>
      <Card style={{ background: "#f0fdf4", border: "1px solid #bbf7d0" }}>
        <div style={{ fontWeight: 700, color: "#166534", marginBottom: 4 }}>📋 Complete this checklist for every client.</div>
        <div style={{ color: "#15803d", fontSize: 13 }}>Every checked box = a happier client, fewer refund requests, and more referrals.</div>
      </Card>
      {deliveryChecklist.map((phase, pi) => (
        <Card key={pi} style={{ borderTop: `4px solid ${phase.color}` }}>
          <div style={{ fontWeight: 800, color: phase.color, fontSize: 15, marginBottom: 14 }}>{phase.phase}</div>
          {phase.steps.map((step, si) => {
            const key = `${pi}-${si}`;
            return (
              <div key={si} onClick={() => toggle(key)} style={{
                display: "flex", gap: 12, alignItems: "flex-start", padding: "8px 0",
                borderBottom: si < phase.steps.length - 1 ? "1px solid #f1f5f9" : "none",
                cursor: "pointer", opacity: checked[key] ? 0.5 : 1
              }}>
                <div style={{
                  width: 20, height: 20, borderRadius: 4, border: `2px solid ${phase.color}`,
                  background: checked[key] ? phase.color : "transparent", flexShrink: 0,
                  display: "flex", alignItems: "center", justifyContent: "center", marginTop: 1
                }}>
                  {checked[key] && <span style={{ color: "#fff", fontSize: 12, fontWeight: 900 }}>✓</span>}
                </div>
                <div>
                  <div style={{ fontWeight: 700, color: "#0f172a", fontSize: 14, textDecoration: checked[key] ? "line-through" : "none" }}>{step.task}</div>
                  <div style={{ color: "#64748b", fontSize: 12 }}>{step.detail}</div>
                </div>
              </div>
            );
          })}
        </Card>
      ))}
    </div>
  );
}

function AIPanel() {
  const [input, setInput] = useState("");
  const [response, setResponse] = useState("");
  const [loading, setLoading] = useState(false);

  const quickPrompts = [
    "Write me a DM for a mobile detailer with no website",
    "Give me 3 objection responses for 'I already have someone building my site'",
    "Write a 30-second Instagram Reel script selling my website service",
    "Give me 10 local businesses to cold DM today in the LA area",
    "Write a referral ask message for after I deliver a site",
    "Create a subject line and email for cold outreach to contractors"
  ];

  const ask = async (prompt) => {
    const q = prompt || input;
    if (!q.trim()) return;
    setLoading(true);
    setResponse("");
    const result = await askAgent(q);
    setResponse(result);
    setLoading(false);
  };

  return (
    <div>
      <Card style={{ background: "linear-gradient(135deg, #1e1b4b 0%, #312e81 100%)", color: "#fff", border: "none" }}>
        <div style={{ fontWeight: 800, fontSize: 16, marginBottom: 4 }}>🤖 AI Sales Assistant</div>
        <div style={{ color: "#a5b4fc", fontSize: 13 }}>Ask anything about selling, scripting, or closing your website clients. Powered by Claude.</div>
      </Card>

      <div style={{ marginBottom: 16 }}>
        <div style={{ fontWeight: 700, color: "#0f172a", fontSize: 13, marginBottom: 8 }}>Quick Prompts:</div>
        <div style={{ display: "flex", flexWrap: "wrap", gap: 6 }}>
          {quickPrompts.map((p, i) => (
            <button key={i} onClick={() => { setInput(p); ask(p); }} style={{
              background: "#eff6ff", color: "#2563eb", border: "1px solid #bfdbfe",
              borderRadius: 20, padding: "5px 12px", fontSize: 12, cursor: "pointer",
              fontFamily: "inherit", fontWeight: 600
            }}>{p}</button>
          ))}
        </div>
      </div>

      <div style={{ display: "flex", gap: 8, marginBottom: 16 }}>
        <textarea
          value={input}
          onChange={e => setInput(e.target.value)}
          onKeyDown={e => e.key === "Enter" && !e.shiftKey && (e.preventDefault(), ask())}
          placeholder="Ask your sales agent anything... (e.g. 'Write a closing message for a notary who said she needs to think about it')"
          style={{
            flex: 1, padding: 12, borderRadius: 8, border: "1px solid #e2e8f0",
            fontFamily: "inherit", fontSize: 13, resize: "vertical", minHeight: 80,
            outline: "none", color: "#0f172a"
          }}
        />
        <button onClick={() => ask()} disabled={loading} style={{
          background: loading ? "#94a3b8" : "#2563eb", color: "#fff", border: "none",
          borderRadius: 8, padding: "0 20px", cursor: loading ? "not-allowed" : "pointer",
          fontFamily: "inherit", fontWeight: 700, fontSize: 14, alignSelf: "stretch"
        }}>
          {loading ? "..." : "Ask"}
        </button>
      </div>

      {loading && (
        <Card style={{ textAlign: "center", color: "#64748b" }}>
          <div style={{ fontSize: 24, marginBottom: 8 }}>🤖</div>
          <div>Your sales agent is thinking...</div>
        </Card>
      )}

      {response && (
        <Card style={{ background: "#f8fafc", border: "1px solid #e2e8f0" }}>
          <div style={{ display: "flex", justifyContent: "space-between", marginBottom: 10 }}>
            <div style={{ fontWeight: 700, color: "#0f172a", fontSize: 13 }}>Agent Response:</div>
            <CopyButton text={response} />
          </div>
          <div style={{ color: "#374151", fontSize: 14, lineHeight: 1.7, whiteSpace: "pre-wrap" }}>{response}</div>
        </Card>
      )}
    </div>
  );
}

// ─── MAIN APP ────────────────────────────────────────────────────

export default function App() {
  const [activeTab, setActiveTab] = useState("offer");

  const panels = {
    offer: <OfferPanel />,
    pricing: <PricingPanel />,
    website: <WebsitePanel />,
    scripts: <ScriptsPanel />,
    dms: <DMPanel />,
    followup: <FollowUpPanel />,
    delivery: <DeliveryPanel />,
    ai: <AIPanel />,
  };

  return (
    <div style={{ fontFamily: "'Inter', system-ui, sans-serif", background: "#f1f5f9", minHeight: "100vh" }}>
      {/* Header */}
      <div style={{ background: "linear-gradient(135deg, #0f172a 0%, #1e3a5f 100%)", color: "#fff", padding: "24px 20px 20px" }}>
        <div style={{ maxWidth: 680, margin: "0 auto" }}>
          <div style={{ fontSize: 11, letterSpacing: 2, color: "#38bdf8", fontWeight: 700, textTransform: "uppercase", marginBottom: 6 }}>Million Dollar Agent Builder</div>
          <div style={{ fontSize: 24, fontWeight: 900, marginBottom: 4 }}>Website Sales Agent</div>
          <div style={{ color: "#94a3b8", fontSize: 14 }}>Complete playbook to sell one-page websites to local businesses — offer, scripts, DMs, follow-ups & delivery.</div>
        </div>
      </div>

      {/* Tabs */}
      <div style={{ background: "#fff", borderBottom: "1px solid #e2e8f0", overflowX: "auto" }}>
        <div style={{ maxWidth: 680, margin: "0 auto", display: "flex", gap: 0, padding: "0 16px" }}>
          {SECTIONS.map(s => (
            <button key={s.id} onClick={() => setActiveTab(s.id)} style={{
              background: "none", border: "none", borderBottom: activeTab === s.id ? "3px solid #2563eb" : "3px solid transparent",
              padding: "12px 10px", cursor: "pointer", fontFamily: "inherit", fontSize: 12,
              fontWeight: activeTab === s.id ? 700 : 500, color: activeTab === s.id ? "#2563eb" : "#64748b",
              whiteSpace: "nowrap", transition: "all 0.15s"
            }}>{s.label}</button>
          ))}
        </div>
      </div>

      {/* Content */}
      <div style={{ maxWidth: 680, margin: "0 auto", padding: "24px 16px 60px" }}>
        {panels[activeTab]}
      </div>
    </div>
  );
}
